# ITISAQ — مجموعة التطوير: مراجعة الحالات

45 سيناريو × لغتين. الإجابات مقترحة من الذكاء الاصطناعي، ومراجعتها البشرية المستقلة لم تتم بعد. هذا الملف للمراجعة فقط ولا يرسل للنموذج. تفترض الحالات فحص صلاحية مُصدر القرار مسبقًا؛ المطلوب مقارنة محتوى المقترح بالقاعدة المعطاة، لا اتخاذ قرار إداري نهائي.

## DEV-0001 — temporary cache versus persistent production writes

التصنيف المقترح: **no_conflict** — مرجع التأليف: S025

### ar

**السياق:** العملية المقترحة تعرض معاينة وتكتب في ذاكرة مؤقتة داخل جهاز الاختبار فقط. لا تغير قاعدة الإنتاج أو أي تخزين دائم.

**القاعدة القائمة:** يحظر تغيير البيانات الدائمة في الإنتاج أثناء التجميد. المعاينات التي تستخدم الذاكرة المؤقتة فقط مسموحة.

**المقترح:** تنفذ المعاينة الموصوفة أثناء التجميد.

**التفسير:** العملية معاينة مؤقتة مستثناة صراحة، وليست تغييرًا دائمًا في الإنتاج.

### en

**Context:** The proposed operation displays a preview and writes only to temporary memory on the test device. It does not change the production database or any persistent storage.

**Existing rule:** Changes to persistent production data are prohibited during the freeze. Previews using only temporary memory are allowed.

**Proposal:** Run the described preview during the freeze.

**Reason:** The operation is an explicitly permitted temporary preview, not a persistent production change.

## DEV-0002 — preferred target versus mandatory deadline

التصنيف المقترح: **no_conflict** — مرجع التأليف: S021

### ar

**السياق:** أُرسل الرد بعد عشر ساعات بالضبط من استلام الطلب، ولا توجد مهلة خاصة بهذا الطلب.

**القاعدة القائمة:** الرد خلال ثماني ساعات هدف مفضل غير ملزم؛ الحد الإلزامي هو اثنتا عشرة ساعة.

**المقترح:** يسجل الرد على أنه استوفى الحد الإلزامي رغم عدم تحقيق الهدف المفضل.

**التفسير:** عشر ساعات تتجاوز الهدف المفضل فقط، ولا تتجاوز الحد الإلزامي.

### en

**Context:** The response was sent exactly ten hours after receipt of the request, with no special deadline for this request.

**Existing rule:** Responding within eight hours is a preferred, nonmandatory target; the mandatory limit is twelve hours.

**Proposal:** Record that the response met the mandatory limit despite missing the preferred target.

**Reason:** Ten hours exceeds only the preferred target, not the mandatory limit.

## DEV-0003 — specialist vote identity missing

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S034

### ar

**السياق:** اللجنة خمسة أعضاء أحدهم مسؤول السلامة. وافق أربعة ورفض واحد، لكن السجل لا يربط الأصوات بأسماء الأعضاء أو أدوارهم.

**القاعدة القائمة:** اعتماد الخطة يتطلب ثلاثة أصوات موافقة على الأقل، منها موافقة مسؤول السلامة تحديدًا.

**المقترح:** تعتمد الخطة بناءً على التصويت المسجل.

**التفسير:** العدد كافٍ، لكن لا يعرف هل مسؤول السلامة ضمن الموافقين.

افتراضيًا: مسؤول السلامة من الأربعة الموافقين.

افتراضيًا: مسؤول السلامة هو العضو الوحيد الرافض.

### en

**Context:** The committee has five members, including the safety officer. Four voted yes and one voted no, but the record does not link votes to members or roles.

**Existing rule:** Plan approval requires at least three yes votes, including a yes vote specifically from the safety officer.

**Proposal:** Approve the plan based on the recorded vote.

**Reason:** The count is sufficient, but it is unknown whether the safety officer voted yes.

Hypothetically: the safety officer is among the four yes voters.

Hypothetically: the safety officer is the sole no voter.

## DEV-0004 — small-cell disclosure restriction

التصنيف المقترح: **conflict** — مرجع التأليف: S002

### ar

**السياق:** جدول نتائج الاستبيان سيُنشر خارج المنظمة. إحدى الخلايا تلخص إجابات ثلاثة أشخاص. لا ترد أسماء المشاركين، وهوية كاتب التقرير غير مذكورة.

**القاعدة القائمة:** عند النشر الخارجي يجب حجب قيمة أي خلية تضم أقل من خمسة مشاركين، حتى لو حذفت الأسماء.

**المقترح:** تُنشر قيمة الخلية الخاصة بالمشاركين الثلاثة كما هي لأن الجدول لا يحتوي أسماء.

**التفسير:** عدد المشاركين ثلاثة وأقل من خمسة؛ حذف الأسماء لا يستثني الخلية من الحجب.

### en

**Context:** A survey-results table will be published outside the organization. One cell summarizes three people's responses. Participant names are absent, and the report writer's identity is not stated.

**Existing rule:** For external publication, the value of any cell containing fewer than five participants must be suppressed, even if names are removed.

**Proposal:** Publish the three-participant cell's value unchanged because the table contains no names.

**Reason:** Three participants is fewer than five; removing names does not exempt the cell from suppression.

## DEV-0005 — duplicate request identity versus document numbers

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S037

### ar

**السياق:** وردت استمارتان بأرقام مستندات مختلفة لنفس العميل والخدمة. حقل معرف طلب الخدمة الأصلي غير موجود في النسختين.

**القاعدة القائمة:** لكل طلب خدمة أصلي رسم واحد فقط؛ إعادة إرسال الاستمارة لا تنشئ رسمًا جديدًا. طلبان أصليان منفصلان يستحقان رسمين.

**المقترح:** يفرض رسمان، واحد لكل استمارة.

**التفسير:** اختلاف رقم المستند لا يثبت اختلاف طلب الخدمة الأصلي.

افتراضيًا: الاستمارتان تخصان طلبي خدمة أصليين منفصلين.

افتراضيًا: الثانية إعادة إرسال للطلب الأصلي نفسه.

### en

**Context:** Two forms with different document numbers were received for the same customer and service. Neither copy contains the original service-request identifier.

**Existing rule:** Each original service request incurs one fee only; resubmitting its form creates no new fee. Two separate original requests incur two fees.

**Proposal:** Charge two fees, one for each form.

**Reason:** Different document numbers do not establish different original service requests.

Hypothetically: the forms represent two separate original service requests.

Hypothetically: the second form resubmits the same original request.

## DEV-0006 — marginal price bands

التصنيف المقترح: **conflict** — مرجع التأليف: S005

### ar

**السياق:** الطلب 15 وحدة مقبولة بالكامل، ولا ضرائب أو خصومات إضافية. أول 10 وحدات سعر كل منها 100، والوحدات الزائدة سعر كل منها 80.

**القاعدة القائمة:** يجب دفع قيمة الطلب وفق التسعير الشرائحي؛ سعر الشريحة الثانية يطبق على الوحدات الزائدة فقط.

**المقترح:** تُسدد قيمة الطلب كاملة بمبلغ 1200، باستخدام سعر 80 لكل الوحدات الخمس عشرة.

**التفسير:** القيمة الواجبة 10×100 + 5×80 = 1400، وليس 1200.

### en

**Context:** The order contains 15 fully accepted units, with no taxes or additional discounts. Each of the first 10 units costs 100; each additional unit costs 80.

**Existing rule:** The order must be paid according to marginal tier pricing; the second-tier price applies only to additional units.

**Proposal:** Settle the entire order for 1200 by applying the price of 80 to all fifteen units.

**Reason:** The payable amount is 10×100 + 5×80 = 1400, not 1200.

## DEV-0007 — rolling window with excluded left boundary

التصنيف المقترح: **no_conflict** — مرجع التأليف: S027

### ar

**السياق:** أرسلت تنبيهات عند 10:00 و10:10 و10:20 و10:30 و10:40 اليوم، ولا تنبيهات أخرى. المقترح إرسال تنبيه عند 11:00 بالضبط.

**القاعدة القائمة:** يسمح بخمسة تنبيهات كحد أقصى في نافذة الستين دقيقة، شاملة التنبيه الجديد. النافذة تستبعد ما أرسل قبل ستين دقيقة بالضبط وتشمل الوقت الحالي.

**المقترح:** يرسل التنبيه الجديد عند 11:00.

**التفسير:** تنبيه 10:00 مستبعد؛ الأربعة اللاحقة مع الجديد تساوي خمسة ضمن الحد.

### en

**Context:** Alerts were sent today at 10:00, 10:10, 10:20, 10:30 and 10:40, with no others. One alert is proposed at exactly 11:00.

**Existing rule:** At most five alerts are allowed in the sixty-minute window, including the new alert. The window excludes an alert sent exactly sixty minutes earlier and includes the current time.

**Proposal:** Send the new alert at 11:00.

**Reason:** The 10:00 alert is excluded; the four later alerts plus the new one total five, within the limit.

## DEV-0008 — sensor uncertainty interval relative to acceptance band

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S045

### ar

**السياق:** قراءة حساس الشحنة 5 درجات مئوية. شهادة معايرته موجودة لكن قيمة هامش الخطأ غير مذكورة في البيانات المتاحة.

**القاعدة القائمة:** لقبول الشحنة يجب أن يقع كامل مجال القراءة زائدًا وناقصًا هامش الخطأ المعتمد ضمن المجال من 2 إلى 8 درجات، شاملًا الطرفين.

**المقترح:** تقبل الشحنة من حيث شرط درجة الحرارة.

**التفسير:** القراءة المركزية وحدها لا تكفي؛ الهامش قد يبقي كامل المجال داخل الحدود أو يجعله يتجاوزها.

افتراضيًا: الهامش درجة واحدة، فيكون المجال من 4 إلى 6.

افتراضيًا: الهامش أربع درجات، فيكون المجال من 1 إلى 9.

### en

**Context:** The shipment sensor reads 5 degrees Celsius. Its calibration certificate exists, but the error-margin value is absent from the available data.

**Existing rule:** For acceptance, the entire interval formed by the reading plus or minus the certified error margin must lie within 2 to 8 degrees, inclusive.

**Proposal:** Accept the shipment as meeting the temperature condition.

**Reason:** The central reading alone is insufficient; the margin could keep the entire interval inside the bounds or extend it outside them.

Hypothetically: the margin is one degree, giving an interval from 4 to 6.

Hypothetically: the margin is four degrees, giving an interval from 1 to 9.

## DEV-0009 — separately permitted tables cannot be joined

التصنيف المقترح: **conflict** — مرجع التأليف: S014

### ar

**السياق:** يسمح للفريق بقراءة جدول الموظفين وجدول الاستبيان كلًا على حدة. يحتوي كلاهما رمز الربط J.

**القاعدة القائمة:** يحظر ربط سجلات الاستبيان بسجلات الموظفين باستخدام J، حتى لمن يسمح له بقراءة الجدولين منفصلين.

**المقترح:** يُنشأ جدول موحد بربط الجدولين على J للاستفادة من صلاحية قراءة كل منهما.

**التفسير:** القراءة المنفصلة مسموحة لكن عملية الربط نفسها ممنوعة صراحة.

### en

**Context:** The team may read the employee table and survey table separately. Both contain join key J.

**Existing rule:** Joining survey records to employee records using J is prohibited, even for someone allowed to read the tables separately.

**Proposal:** Create a combined table by joining the two tables on J, relying on permission to read each one.

**Reason:** Separate reading is allowed, but the join operation itself is explicitly prohibited.

## DEV-0010 — translation attestation depends on controlling version

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S043

### ar

**السياق:** للنموذج نسخة عربية وإنجليزية، ولا تحدد الحزمة أيهما النسخة الملزمة وأيهما ترجمة مساعدة. النسخة الإنجليزية لم تخضع لاعتماد ترجمة.

**القاعدة القائمة:** الترجمة المساعدة تتطلب اعتماد ترجمة قبل التوزيع. النسخة الملزمة الأصلية لا تتطلب اعتماد ترجمة.

**المقترح:** توزع النسخة الإنجليزية الآن دون اعتماد ترجمة.

**التفسير:** لا يعرف هل الإنجليزية هي الأصل المستثنى أم ترجمة يلزم اعتمادها.

افتراضيًا: الإنجليزية هي النسخة الأصلية الملزمة.

افتراضيًا: الإنجليزية ترجمة مساعدة للأصل العربي.

### en

**Context:** The form has Arabic and English versions, but the package does not identify which is controlling and which is a supporting translation. The English version has no translation certification.

**Existing rule:** A supporting translation requires translation certification before distribution. The original controlling version does not require translation certification.

**Proposal:** Distribute the English version now without translation certification.

**Reason:** It is unknown whether English is the exempt original or a translation requiring certification.

Hypothetically: English is the original controlling version.

Hypothetically: English is a supporting translation of the Arabic original.

## DEV-0011 — revocation and previously produced aggregates

التصنيف المقترح: **no_conflict** — مرجع التأليف: S024

### ar

**السياق:** سحب مشارك موافقته اليوم. أنتجت قبل السحب إحصاءات مجمعة لا يمكن إرجاعها إلى أفراد، ولا تتضمن بياناته الخام.

**القاعدة القائمة:** بعد السحب يجب وقف أي استخدام جديد للبيانات الخام، ويجوز الاحتفاظ بالإحصاءات المجمعة غير القابلة للإرجاع إلى أفراد إذا أنتجت قبل السحب.

**المقترح:** يوقف استخدام البيانات الخام مستقبلًا، ويحتفظ بالإحصاءات المجمعة السابقة فقط.

**التفسير:** المقترح يوقف الاستخدام المطلوب إيقافه ويقتصر احتفاظه على الاستثناء المسموح صراحة.

### en

**Context:** A participant withdrew consent today. Irreversible aggregate statistics were produced before withdrawal and contain no raw individual data.

**Existing rule:** After withdrawal, all new use of raw data must stop; irreversible aggregate statistics produced before withdrawal may be retained.

**Proposal:** Stop future use of raw data and retain only the earlier aggregate statistics.

**Reason:** The proposal stops the required use and limits retention to the explicitly allowed exception.

## DEV-0012 — alternative validation routes

التصنيف المقترح: **no_conflict** — مرجع التأليف: S019

### ar

**السياق:** حزمة التحديث اجتازت فحص التوقيع الآلي بنجاح. لم تجر مراجعة يدوية.

**القاعدة القائمة:** يكفي لاعتماد سلامة الحزمة أحد مسارين: نجاح فحص التوقيع الآلي أو توقيع المراجع اليدوي. لا يلزم الجمع بينهما.

**المقترح:** تُعد الحزمة مستوفية لفحص السلامة اعتمادًا على نجاح الفحص الآلي وحده.

**التفسير:** تحقق أحد المسارين الكافيين؛ غياب المسار الآخر لا ينقض الاستيفاء.

### en

**Context:** The update package passed automated signature validation. No manual review was performed.

**Existing rule:** Either route suffices to validate the package: successful automated signature validation or a manual reviewer's sign-off. Both are not required.

**Proposal:** Treat the package as satisfying the integrity check based on successful automated validation alone.

**Reason:** One sufficient route is satisfied; absence of the other does not invalidate compliance.

## DEV-0013 — asset ownership determines redistribution condition

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S033

### ar

**السياق:** يراد نشر الرسم K ضمن دليل عام. الملف لا يحدد هل الرسم مملوك للمنظمة أم مرخص من طرف خارجي. لم يطلب إذن خارجي للنشر.

**القاعدة القائمة:** يجوز نشر الرسوم المملوكة للمنظمة مباشرة. الرسوم المرخصة من طرف خارجي تتطلب إذنًا مكتوبًا منه قبل النشر.

**المقترح:** ينشر الرسم K الآن دون الحصول على إذن خارجي.

**التفسير:** مصدر حقوق الرسم يحدد الحاجة إلى الإذن، وهو غير معلوم.

افتراضيًا: المنظمة تملك الرسم، فلا يلزم الإذن الخارجي.

افتراضيًا: الرسم مرخص خارجيًا، فيلزم الإذن الغائب.

### en

**Context:** Illustration K is to be published in a public guide. The file does not establish whether the organization owns it or licenses it from an external party. No external publication permission was requested.

**Existing rule:** Organization-owned illustrations may be published directly. Externally licensed illustrations require written permission from the licensor before publication.

**Proposal:** Publish illustration K now without obtaining external permission.

**Reason:** Ownership determines whether permission is required, and it is unknown.

Hypothetically: the organization owns the illustration, so no external permission is needed.

Hypothetically: the illustration is externally licensed, so the missing permission is required.

## DEV-0014 — normalization of record identifiers

التصنيف المقترح: **no_conflict** — مرجع التأليف: S030

### ar

**السياق:** السجل يحمل المعرف AB-120، والمعاملة تشير إلى ab120. لا اختلاف آخر بين المعرفين.

**القاعدة القائمة:** عند مطابقة المعرفات، تهمل حالة الأحرف والشرطات فقط.

**المقترح:** تربط المعاملة بالسجل باعتبار المعرفين متطابقين.

**التفسير:** بعد التطبيع المحدد يصبح المعرفان AB120، فلا يوجد اختلاف مؤثر.

### en

**Context:** The record identifier is AB-120 and the transaction refers to ab120. There is no other difference between the identifiers.

**Existing rule:** When matching identifiers, ignore letter case and hyphens only.

**Proposal:** Link the transaction to the record, treating the identifiers as matching.

**Reason:** After the specified normalization, both identifiers become AB120, with no material difference.

## DEV-0015 — receipt indicator versus explicit acceptance

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S038

### ar

**السياق:** تعرض لوحة المتابعة حالة «تم التأكيد» للرسالة المرسلة إلى الشريك. لا توضح اللوحة هل المقصود إيصال وصول آلي أم قبول صريح من الشريك، ولا يوجد سجل آخر للتأكيد.

**القاعدة القائمة:** تبدأ الخدمة بعد قبول صريح من الشريك؛ إيصال الوصول الآلي وحده لا يكفي.

**المقترح:** تبدأ الخدمة اعتمادًا على حالة «تم التأكيد» وحدها.

**التفسير:** معنى الحالة غير محدد، وقد تمثل قبولًا كافيًا أو مجرد وصول غير كافٍ.

افتراضيًا: الحالة تسجل قبولًا صريحًا أرسله الشريك.

افتراضيًا: الحالة ناتجة فقط عن إيصال وصول آلي دون قبول.

### en

**Context:** The dashboard shows 'confirmed' for the message sent to the partner. It does not indicate whether this means an automated delivery receipt or explicit acceptance from the partner, and there is no other confirmation record.

**Existing rule:** The service starts after explicit acceptance from the partner; an automated delivery receipt alone is insufficient.

**Proposal:** Start the service based solely on the 'confirmed' status.

**Reason:** The status meaning is unspecified; it could represent sufficient acceptance or insufficient delivery confirmation.

Hypothetically: the status records explicit acceptance sent by the partner.

Hypothetically: the status comes only from an automated receipt, with no acceptance.

## DEV-0016 — voluntary participation with no penalty

التصنيف المقترح: **conflict** — مرجع التأليف: S015

### ar

**السياق:** الاستبيان اختياري لجميع الموظفين. الموظفة N مستحقة للمكافأة وفق جميع شروطها الأخرى وقررت عدم المشاركة في الاستبيان.

**القاعدة القائمة:** يجوز رفض المشاركة دون أي أثر على المكافأة؛ لا يجوز حرمان الموظف منها بسبب عدم المشاركة.

**المقترح:** تُحجب مكافأة N بسبب عدم مشاركتها في الاستبيان وحده.

**التفسير:** الحرمان سببه عدم المشاركة، وهو الأثر الذي تمنعه القاعدة صراحة.

### en

**Context:** The survey is voluntary for all employees. Employee N meets every other bonus condition and chose not to participate in the survey.

**Existing rule:** Employees may decline participation without any effect on the bonus; the bonus must not be withheld because of nonparticipation.

**Proposal:** Withhold N's bonus solely because she did not participate in the survey.

**Reason:** The bonus is withheld because of nonparticipation, precisely the consequence prohibited by the rule.

## DEV-0017 — internal transfer preserves aggregate allocation

التصنيف المقترح: **no_conflict** — مرجع التأليف: S023

### ar

**السياق:** خصصت 7000 وحدة للمسار A و3000 للمسار B. النقل بينهما مسموح، ولا توجد حدود منفصلة لكل مسار.

**القاعدة القائمة:** يجب ألا يتجاوز مجموع تخصيصات المسارين 10000 وحدة.

**المقترح:** تنقل 500 وحدة من A إلى B، لتصبح التخصيصات 6500 و3500 على الترتيب.

**التفسير:** المجموع يبقى 10000؛ النقل لا ينشئ زيادة في التخصيص الكلي.

### en

**Context:** Track A has 7000 units allocated and track B has 3000. Transfers between them are allowed, with no separate track limits.

**Existing rule:** The combined allocation to the two tracks must not exceed 10000 units.

**Proposal:** Transfer 500 units from A to B, making allocations 6500 and 3500 respectively.

**Reason:** The total remains 10000; the transfer does not increase the combined allocation.

## DEV-0018 — amendment permission restricted to named fields

التصنيف المقترح: **conflict** — مرجع التأليف: S013

### ar

**السياق:** أُقر تعديل عنوان تسليم الطلب فقط. بند السعر ينص على 70 وحدة للقطعة، ولا يوجد تعديل سعر معتمد.

**القاعدة القائمة:** يبقى كل بند غير مذكور في التعديل على حاله؛ موافقة تعديل العنوان لا تغير سعر القطعة.

**المقترح:** يُطبق سعر 75 للوحدة ضمن تنفيذ تعديل العنوان نفسه.

**التفسير:** التعديل المعتمد خاص بالعنوان؛ تغيير 70 إلى 75 يناقض بقاء بند السعر.

### en

**Context:** Only an amendment to the order's delivery address was approved. The price clause states 70 units per item, and no price amendment was approved.

**Existing rule:** Every clause not named in the amendment remains unchanged; approval of an address amendment does not change the unit price.

**Proposal:** Apply a unit price of 75 as part of implementing the address amendment.

**Reason:** The approved amendment concerns the address; changing 70 to 75 contradicts the unchanged price clause.

## DEV-0019 — signature validity does not establish signer's role

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S036

### ar

**السياق:** نموذج القبول يحمل توقيعًا رقميًا صحيحًا للشخص Z. لدى العميل ومقاول التنفيذ موظفون مخولون بالتوقيع، لكن السجل لا يبين لأي طرف ينتمي Z.

**القاعدة القائمة:** لا تغلق مرحلة التسليم إلا بتوقيع قبول من ممثل العميل؛ توقيع مقاول التنفيذ وحده لا يكفي.

**المقترح:** تغلق المرحلة اعتمادًا على توقيع Z وحده.

**التفسير:** صحة التوقيع لا تحدد هل صدر عن ممثل العميل المطلوب.

افتراضيًا: Z ممثل العميل المخول.

افتراضيًا: Z ممثل مقاول التنفيذ وحده.

### en

**Context:** The acceptance form carries a valid digital signature from Z. Both the customer and implementation contractor have authorized signatories, but the record does not identify which party Z belongs to.

**Existing rule:** The delivery stage may close only with acceptance signed by the customer's representative; the implementation contractor's signature alone is insufficient.

**Proposal:** Close the stage based solely on Z's signature.

**Reason:** Signature validity does not establish whether it came from the required customer representative.

Hypothetically: Z is the customer's authorized representative.

Hypothetically: Z represents only the implementation contractor.

## DEV-0020 — contract category not established by job title

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S032

### ar

**السياق:** تعمل R منسقة للمشروع. لا يحدد الملف إن كانت موظفة دائمة أو متعاقدة مستقلة.

**القاعدة القائمة:** الاشتراك في برنامج الادخار إلزامي للموظفين الدائمين، واختياري للمتعاقدين المستقلين.

**المقترح:** تسمح المنظمة لـR باختيار عدم الاشتراك.

**التفسير:** المسمى الوظيفي لا يحدد فئة العقد التي يتوقف عليها الإلزام.

افتراضيًا: R متعاقدة مستقلة، فيجوز لها عدم الاشتراك.

افتراضيًا: R موظفة دائمة، فيلزم اشتراكها.

### en

**Context:** R works as a project coordinator. The file does not establish whether she is a permanent employee or an independent contractor.

**Existing rule:** Enrollment in the savings program is mandatory for permanent employees and optional for independent contractors.

**Proposal:** Allow R to choose not to enroll.

**Reason:** The job title does not establish the contract category that determines whether enrollment is mandatory.

Hypothetically: R is an independent contractor, so opting out is allowed.

Hypothetically: R is a permanent employee, so enrollment is required.

## DEV-0021 — concurrent seats rather than registered accounts

التصنيف المقترح: **no_conflict** — مرجع التأليف: S018

### ar

**السياق:** يوجد 18 حسابًا مسجلًا، وثلاث جلسات نشطة. سيبدأ مستخدم رابع جلسة واحدة؛ لا جلسات أخرى ستبدأ خلال المراجعة. أسماء المستخدمين غير مذكورة.

**القاعدة القائمة:** الحد هو خمس جلسات متزامنة، وليس خمسة حسابات مسجلة.

**المقترح:** تُفتح جلسة المستخدم الرابع مع إبقاء الحسابات المسجلة كما هي.

**التفسير:** تصبح الجلسات المتزامنة أربعًا، دون الحد؛ عدد الحسابات والأسماء لا يغيران ذلك.

### en

**Context:** There are 18 registered accounts and three active sessions. A fourth user will start one session; no other sessions will start during the review. User names are not stated.

**Existing rule:** The limit is five concurrent sessions, not five registered accounts.

**Proposal:** Open the fourth user's session while leaving registered accounts unchanged.

**Reason:** Concurrent sessions become four, below the limit; account count and names do not change that.

## DEV-0022 — conditional exposure assessment

التصنيف المقترح: **no_conflict** — مرجع التأليف: S026

### ar

**السياق:** الزيارة محصورة في مكتب منفصل ولا تتضمن أي تعرض لمواد كيميائية. عمر الزائر غير مذكور.

**القاعدة القائمة:** يجب إجراء تقييم التعرض الكيميائي قبل الزيارات التي تتضمن تعرضًا كيميائيًا فقط؛ لا يلزم هذا التقييم لزيارة مكتبية دون تعرض.

**المقترح:** تتم الزيارة المكتبية الموصوفة دون تقييم تعرض كيميائي.

**التفسير:** شرط التعرض غير متحقق، والعمر غير مؤثر وفق القاعدة المقدمة.

### en

**Context:** The visit is confined to a separate office and involves no chemical exposure. The visitor's age is not stated.

**Existing rule:** A chemical-exposure assessment is required only before visits involving chemical exposure; it is not required for an office visit without exposure.

**Proposal:** Proceed with the described office visit without a chemical-exposure assessment.

**Reason:** The exposure condition is absent, and age is irrelevant under the supplied rule.

## DEV-0023 — silence is not renewal acceptance

التصنيف المقترح: **conflict** — مرجع التأليف: S003

### ar

**السياق:** أُرسل إلى العميل إشعار التجديد ولم يرد عليه خلال المهلة. لم يقدم أي قبول مكتوب آخر.

**القاعدة القائمة:** لا يجدد الاشتراك إلا بقبول مكتوب من العميل؛ عدم الرد لا يعد قبولًا.

**المقترح:** يُجدد الاشتراك تلقائيًا لأن العميل لم يعترض خلال المهلة.

**التفسير:** عدم الاعتراض هو عدم الرد نفسه، والقبول المكتوب منفي صراحة في السياق.

### en

**Context:** The customer was sent a renewal notice and did not respond within the deadline. They provided no other written acceptance.

**Existing rule:** A subscription may be renewed only with the customer's written acceptance; silence does not count as acceptance.

**Proposal:** Renew the subscription automatically because the customer did not object within the deadline.

**Reason:** Lack of objection is silence, and written acceptance is explicitly absent in the context.

## DEV-0024 — purpose limitation despite access authorization

التصنيف المقترح: **conflict** — مرجع التأليف: S004

### ar

**السياق:** الفريق مخول بقراءة النسخة الاحتياطية. المشروع المقترح دراسة تسويقية وليس استعادة لخدمة متوقفة.

**القاعدة القائمة:** يقتصر استخدام بيانات هذه النسخة الاحتياطية على استعادة الخدمة؛ صلاحية القراءة لا تمنح حق استعمالها لأغراض أخرى.

**المقترح:** تُستخدم بيانات النسخة لتقسيم العملاء إلى شرائح تسويقية اعتمادًا على صلاحية الفريق في قراءتها.

**التفسير:** الغرض التسويقي خارج غرض الاستعادة المسموح، حتى مع تحقق صلاحية القراءة.

### en

**Context:** The team is authorized to read the backup. The proposed project is a marketing study, not recovery of a failed service.

**Existing rule:** Use of this backup's data is restricted to service recovery; read access does not authorize use for other purposes.

**Proposal:** Use the backup data to segment customers for marketing based on the team's read access.

**Reason:** Marketing is outside the permitted recovery purpose, even though read access is authorized.

## DEV-0025 — per-branch threshold cannot be replaced by average

التصنيف المقترح: **conflict** — مرجع التأليف: S010

### ar

**السياق:** تساوت أوزان الفرعين في التقرير: إتاحة الفرع East تساوي 98% وإتاحة West تساوي 100% للفترة نفسها.

**القاعدة القائمة:** لا يجوز إعلان استيفاء معيار الإتاحة إلا إذا بلغ كل فرع 99% على الأقل؛ متوسط الفروع لا يحل محل الشرط الفردي.

**المقترح:** يُعلن استيفاء الفرعين للمعيار لأن متوسطهما 99%.

**التفسير:** East أقل من 99%؛ المتوسط لا يحقق شرط كل فرع.

### en

**Context:** The report weights the branches equally: East had 98% availability and West had 100% for the same period.

**Existing rule:** Compliance with the availability standard may be declared only if every branch reaches at least 99%; a branch average does not replace the individual requirement.

**Proposal:** Declare both branches compliant because their average is 99%.

**Reason:** East is below 99%; the average does not satisfy the per-branch requirement.

## DEV-0026 — mandatory versus optional cost breakdown

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S039

### ar

**السياق:** سعر الحزمة الإجمالي 1200 وحدة ويجمع مكونات أساسية وإضافات اختيارية. لا يوجد تفصيل يحدد تكلفة كل نوع.

**القاعدة القائمة:** يجب ألا تتجاوز تكلفة المكونات الأساسية 1000 وحدة؛ تستبعد الإضافات الاختيارية من هذا الحد.

**المقترح:** تصنف الحزمة على أنها مستوفية لحد تكلفة المكونات الأساسية.

**التفسير:** إجمالي الحزمة لا يكشف تكلفة الجزء الخاضع للحد.

افتراضيًا: الأساسية 900 والاختيارية 300.

افتراضيًا: الأساسية 1100 والاختيارية 100.

### en

**Context:** The package totals 1200 units and includes essential components and optional add-ons. No breakdown identifies the cost of each type.

**Existing rule:** Essential components must cost at most 1000 units; optional add-ons are excluded from this limit.

**Proposal:** Classify the package as meeting the essential-component cost limit.

**Reason:** The package total does not reveal the cost of the portion subject to the limit.

Hypothetically: essential components cost 900 and optional add-ons cost 300.

Hypothetically: essential components cost 1100 and optional add-ons cost 100.

## DEV-0027 — execution mode distinguishes preview from modification

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S042

### ar

**السياق:** سيشغّل المسؤول أمرًا اسمه apply. يمكن للأمر العمل في وضع المعاينة دون تعديل أو وضع التنفيذ الفعلي، ولم تحدد إعدادات هذه العملية. لن تؤخذ نسخة استرجاع قبل التشغيل.

**القاعدة القائمة:** تلزم نسخة استرجاع قبل التنفيذ الذي يعدل بيانات الإنتاج. المعاينة التي لا تعدل شيئًا لا تتطلبها.

**المقترح:** يشغل الأمر بالإعدادات غير المبينة دون نسخة استرجاع.

**التفسير:** اسم الأمر لا يكشف وضع التنفيذ الذي يحدد الحاجة إلى النسخة.

افتراضيًا: الإعدادات تختار معاينة بلا أي تعديل.

افتراضيًا: الإعدادات تختار تعديل بيانات الإنتاج فعليًا.

### en

**Context:** The administrator will run a command named apply. It can run in preview mode without changes or in actual execution mode, and this operation's settings are unspecified. No recovery snapshot will be taken before running it.

**Existing rule:** A recovery snapshot is required before execution that modifies production data. A preview that changes nothing does not require one.

**Proposal:** Run the command with the unspecified settings without a recovery snapshot.

**Reason:** The command name does not reveal the execution mode that determines whether a snapshot is required.

Hypothetically: the settings select a preview with no changes.

Hypothetically: the settings select actual modification of production data.

## DEV-0028 — round after summing line values

التصنيف المقترح: **conflict** — مرجع التأليف: S001

### ar

**السياق:** فاتورة خدمة فيها بندان، قيمة كل منهما 0.335 وحدة. التقريب إلى منزلتين يكون برفع النصف، ولا رسوم أخرى.

**القاعدة القائمة:** يجب جمع قيم البنود الدقيقة أولًا ثم تقريب المجموع مرة واحدة لتحديد المبلغ الواجب دفعه.

**المقترح:** يُدفع 0.68 وحدة، بعد تقريب كل بند إلى 0.34 ثم جمعهما.

**التفسير:** المجموع الدقيق 0.670 ويقرب إلى 0.67؛ طريقة الحساب والمبلغ المقترحان يخالفان القاعدة.

### en

**Context:** A service invoice has two lines, each worth 0.335 units. Rounding to two decimal places uses round-half-up, with no other charges.

**Existing rule:** Exact line values must first be added, then the total rounded once to determine the amount payable.

**Proposal:** Pay 0.68 units by rounding each line to 0.34 and then adding them.

**Reason:** The exact total is 0.670, which rounds to 0.67; the proposed method and amount violate the rule.

## DEV-0029 — continuous service during staged migration

التصنيف المقترح: **no_conflict** — مرجع التأليف: S016

### ar

**السياق:** الخدمة لها نقطتا اتصال A وB تعملان الآن. يمكن لكل واحدة تشغيل الخدمة وحدها.

**القاعدة القائمة:** يجب أن تبقى نقطة اتصال واحدة على الأقل عاملة طوال الترحيل.

**المقترح:** توقف A بينما تستمر B. بعد التأكد من عودة A للعمل، توقف B مع استمرار A.

**التفسير:** في كل مرحلة توجد نقطة عاملة؛ لا تتطلب القاعدة استمرار النقطتين معًا.

### en

**Context:** The service has two endpoints, A and B, both currently working. Either endpoint can serve the service alone.

**Existing rule:** At least one endpoint must remain operational throughout migration.

**Proposal:** Stop A while B continues serving. After confirming A is operational again, stop B while A continues serving.

**Reason:** An endpoint remains operational at every stage; the rule does not require both simultaneously.

## DEV-0030 — rolling interval does not reset at midnight

التصنيف المقترح: **conflict** — مرجع التأليف: S008

### ar

**السياق:** نُفذ آخر تغيير إعدادات الساعة 23:30 يوم الاثنين. التغيير التالي لنفس المورد مقترح الساعة 00:30 يوم الثلاثاء، بالتوقيت نفسه.

**القاعدة القائمة:** يجب الفصل بين تغييرين متتاليين للمورد بـ24 ساعة كاملة على الأقل؛ بداية يوم تقويمي جديد لا تعيد حساب المهلة.

**المقترح:** يُنفذ التغيير التالي في موعده المقترح لأن التاريخ أصبح يوم الثلاثاء.

**التفسير:** مرّت ساعة واحدة فقط بين التغييرين، لا 24 ساعة.

### en

**Context:** The last configuration change occurred at 23:30 on Monday. The next change to the same resource is proposed for 00:30 on Tuesday, in the same time zone.

**Existing rule:** Consecutive changes to the resource must be separated by at least 24 full hours; a new calendar day does not reset the interval.

**Proposal:** Execute the next change at the proposed time because the date has become Tuesday.

**Reason:** Only one hour has elapsed between the changes, not 24 hours.

## DEV-0031 — supplier credit reduces reimbursable amount

التصنيف المقترح: **conflict** — مرجع التأليف: S012

### ar

**السياق:** دفع الموظف 400 وحدة لمورد، ثم أعاد المورد له 50 وحدة عن العملية نفسها قبل التعويض. لا مصروفات أخرى ضمن الطلب.

**القاعدة القائمة:** يعوض الموظف عن صافي ما تحمله فقط بعد طرح أي مبالغ أعادها المورد عن العملية.

**المقترح:** يُعوض الموظف بـ400 وحدة لأن هذا هو مبلغ الدفع الأصلي.

**التفسير:** صافي ما تحمله 400 - 50 = 350؛ تعويض 400 يتجاوز الصافي.

### en

**Context:** An employee paid a supplier 400 units, then received a 50-unit refund for the same transaction before reimbursement. The claim contains no other expenses.

**Existing rule:** The employee must be reimbursed only for the net amount borne after deducting any supplier refunds for that transaction.

**Proposal:** Reimburse the employee 400 units because that was the original payment amount.

**Reason:** The net amount borne is 400 - 50 = 350; reimbursing 400 exceeds it.

## DEV-0032 — billing period of quoted rate missing

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S040

### ar

**السياق:** عرض المورد يذكر سعرًا قدره 200 وحدة للاشتراك دون تحديد هل هو شهري أو سنوي. المقترح التزام لمدة سنة كاملة، ولا رسوم أخرى.

**القاعدة القائمة:** يجب ألا يزيد الالتزام المالي للسنة الكاملة على 1000 وحدة.

**المقترح:** يعتمد الاشتراك السنوي بالسعر المذكور باعتباره ضمن الحد.

**التفسير:** 200 سنويًا ضمن الحد، بينما 200 شهريًا تعني 2400 للسنة؛ فترة التسعير غير معلومة.

افتراضيًا: السعر 200 للسنة كاملة.

افتراضيًا: السعر 200 لكل شهر من الأشهر الاثني عشر.

### en

**Context:** The supplier quote states a subscription price of 200 units without specifying whether it is monthly or annual. A full-year commitment is proposed, with no other charges.

**Existing rule:** The financial commitment for the full year must not exceed 1000 units.

**Proposal:** Approve the year-long subscription at the quoted rate as being within the limit.

**Reason:** 200 annually is within the limit, whereas 200 monthly means 2400 for the year; the billing period is unknown.

Hypothetically: the price is 200 for the entire year.

Hypothetically: the price is 200 for each of the twelve months.

## DEV-0033 — excluded amounts in percentage fee base

التصنيف المقترح: **no_conflict** — مرجع التأليف: S017

### ar

**السياق:** إجمالي الفاتورة 1200 وحدة، منها منحة معفاة مقدارها 200. لا استثناءات أو رسوم أخرى.

**القاعدة القائمة:** تحسب رسوم الخدمة بنسبة 5% من مبلغ الفاتورة بعد استبعاد المنحة.

**المقترح:** تُحدد رسوم الخدمة بـ50 وحدة.

**التفسير:** الوعاء 1200 - 200 = 1000، ورسومه 5% تساوي 50.

### en

**Context:** The invoice total is 1200 units, including an exempt grant of 200. There are no other exceptions or charges.

**Existing rule:** The service fee is calculated at 5% of the invoice amount after excluding the grant.

**Proposal:** Set the service fee at 50 units.

**Reason:** The base is 1200 - 200 = 1000, and 5% of it is 50.

## DEV-0034 — settlement date selects exchange rate

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S035

### ar

**السياق:** المبلغ 100 وحدة أجنبية. السعر الداخلي المعتمد 3 وحدات محلية لكل أجنبية يوم الاثنين، و4 يوم الثلاثاء. التسوية في أحد اليومين، ولا يحدد السجل أيهما. لا رسوم أخرى.

**القاعدة القائمة:** يسجل المبلغ المحلي باستخدام السعر المعتمد في يوم التسوية الفعلي.

**المقترح:** يسجل المبلغ بـ300 وحدة محلية.

**التفسير:** 300 صحيح بسعر الاثنين، لكنه يختلف عن 400 اللازمة إن كانت التسوية الثلاثاء.

افتراضيًا: تمت التسوية يوم الاثنين.

افتراضيًا: تمت التسوية يوم الثلاثاء.

### en

**Context:** The amount is 100 foreign units. The approved internal rate is 3 local units per foreign unit on Monday and 4 on Tuesday. Settlement occurred on one of those days, but the record does not identify which. There are no other charges.

**Existing rule:** Record the local amount using the approved rate on the actual settlement day.

**Proposal:** Record the amount as 300 local units.

**Reason:** 300 is correct at Monday's rate, but differs from the required 400 if settlement was on Tuesday.

Hypothetically: settlement occurred on Monday.

Hypothetically: settlement occurred on Tuesday.

## DEV-0035 — chronological order across time zones

التصنيف المقترح: **conflict** — مرجع التأليف: S009

### ar

**السياق:** الطلبان متساويان في الأولوية وجاهزان. وصل R الساعة 09:00 UTC، ووصل S الساعة 11:30 بتوقيت UTC+03. فرق التوقيت ثابت ولا تغيير صيفي.

**القاعدة القائمة:** يجب معالجة الأسبق وصولًا أولًا عند تساوي الأولوية، بعد تحويل الطوابع الزمنية إلى توقيت موحد.

**المقترح:** يُعالج R قبل S لأن 09:00 أسبق من 11:30 عند قراءة الساعتين كما هما.

**التفسير:** وصول S يساوي 08:30 UTC، فيسبق R الذي وصل 09:00 UTC.

### en

**Context:** Both requests have equal priority and are ready. R arrived at 09:00 UTC; S arrived at 11:30 in UTC+03. The offset is fixed, with no daylight-saving change.

**Existing rule:** For equal-priority requests, the earlier arrival must be processed first after converting timestamps to a common time zone.

**Proposal:** Process R before S because 09:00 appears earlier than 11:30 when the clock readings are compared directly.

**Reason:** S arrived at 08:30 UTC, before R's arrival at 09:00 UTC.

## DEV-0036 — weighted voting rather than head count

التصنيف المقترح: **no_conflict** — مرجع التأليف: S028

### ar

**السياق:** وزن صوت الرئيس نقطتان، وصوت كل عضو آخر نقطة واحدة. وافق الرئيس وعضوان آخران، ولا يوجد شرط نصاب إضافي.

**القاعدة القائمة:** يمر المقترح عند جمع أربع نقاط موافقة على الأقل.

**المقترح:** يسجل المقترح على أنه اجتاز التصويت.

**التفسير:** نقاط الموافقة 2 + 1 + 1 = 4؛ عدد الأشخاص الثلاثة ليس معيار القاعدة.

### en

**Context:** The chair's vote has weight two; each other member's vote has weight one. The chair and two other members voted yes, with no additional quorum requirement.

**Existing rule:** A proposal passes with at least four approval points.

**Proposal:** Record the proposal as having passed the vote.

**Reason:** Approval points are 2 + 1 + 1 = 4; the three-person head count is not the rule's criterion.

## DEV-0037 — training credit depends on participation role

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S041

### ar

**السياق:** يظهر اسم الموظف M في سجل ورشة مدتها أربع ساعات. يضم السجل أسماء المدربين والمتدربين دون تحديد دور M، وقد حضر المدة كاملة.

**القاعدة القائمة:** تحتسب ساعات التطوير الشخصي للمشاركة كمتدرب فقط؛ تقديم الورشة كمدرب لا يضاف إلى هذا الرصيد.

**المقترح:** تضاف أربع ساعات إلى رصيد التطوير الشخصي لـM عن هذه الورشة.

**التفسير:** مدة الحضور معلومة لكن الدور الذي يحدد احتساب الساعات غير معلوم.

افتراضيًا: M شارك كمتدرب فقط.

افتراضيًا: M قدم الورشة كمدرب فقط.

### en

**Context:** Employee M appears in the register for a four-hour workshop. The register lists trainers and trainees without identifying M's role, and M attended the full duration.

**Existing rule:** Personal-development hours count only for participation as a trainee; delivering the workshop as a trainer does not add to this balance.

**Proposal:** Add four personal-development hours to M's balance for this workshop.

**Reason:** Attendance duration is known, but the role determining whether the hours count is unknown.

Hypothetically: M participated only as a trainee.

Hypothetically: M delivered the workshop only as a trainer.

## DEV-0038 — deadline comparison across time zones

التصنيف المقترح: **no_conflict** — مرجع التأليف: S020

### ar

**السياق:** آخر وقت لاستلام الطلب هو 15:00 بتوقيت UTC اليوم. استلم النظام الطلب اليوم في 17:30 بتوقيت UTC+03:00.

**القاعدة القائمة:** تقبل الطلبات المستلمة عند الموعد النهائي أو قبله بعد توحيد المنطقة الزمنية.

**المقترح:** يصنف الطلب على أنه وصل ضمن المهلة.

**التفسير:** 17:30 في UTC+03:00 تساوي 14:30 UTC، قبل 15:00.

### en

**Context:** The submission deadline is 15:00 UTC today. The system received the submission today at 17:30 UTC+03:00.

**Existing rule:** Submissions received at or before the deadline are accepted after converting times to the same time zone.

**Proposal:** Classify the submission as received within the deadline.

**Reason:** 17:30 UTC+03:00 equals 14:30 UTC, before 15:00.

## DEV-0039 — gross weight including packaging

التصنيف المقترح: **no_conflict** — مرجع التأليف: S029

### ar

**السياق:** وزن البضاعة 460 كيلوجرامًا، ووزن جميع مواد تغليفها 30 كيلوجرامًا. لا توجد أي حمولة أخرى.

**القاعدة القائمة:** يجب ألا يزيد الوزن الإجمالي، شاملًا التغليف، على 500 كيلوجرام.

**المقترح:** تعتمد الشحنة الموصوفة من حيث حد الوزن.

**التفسير:** الوزن الإجمالي 490، وهو أقل من 500.

### en

**Context:** The goods weigh 460 kilograms and all their packaging weighs 30 kilograms. There is no other load.

**Existing rule:** Gross weight, including packaging, must not exceed 500 kilograms.

**Proposal:** Accept the described shipment as meeting the weight limit.

**Reason:** Gross weight is 490, below 500.

## DEV-0040 — revocation propagates to derivative credentials

التصنيف المقترح: **conflict** — مرجع التأليف: S011

### ar

**السياق:** التفويض D ألغي اليوم. الرمز T مشتق من D، وتاريخ انتهاء T المطبوع بعد أسبوع.

**القاعدة القائمة:** إلغاء التفويض يبطل فورًا جميع الرموز المشتقة منه، حتى لو لم يحل تاريخ انتهاء الرمز.

**المقترح:** يستمر قبول T حتى تاريخ انتهائه المطبوع رغم إلغاء D.

**التفسير:** إلغاء D يبطل T فورًا وفق النص، فلا يبقى صالحًا إلى موعده المطبوع.

### en

**Context:** Delegation D was revoked today. Token T derives from D, and T's printed expiry date is one week later.

**Existing rule:** Revoking a delegation immediately invalidates all tokens derived from it, even if a token's expiry date has not been reached.

**Proposal:** Continue accepting T until its printed expiry date despite D's revocation.

**Reason:** D's revocation immediately invalidates T under the rule; it does not remain valid until the printed date.

## DEV-0041 — suppression count uses unique people rather than rows

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S044

### ar

**السياق:** جدول عينة يحتوي ستة صفوف. يمكن أن يحتوي عدة صفوف للشخص نفسه، ومعرفات الأشخاص غير متاحة في النسخة المقدمة.

**القاعدة القائمة:** لا يجوز نشر متوسط العينة إلا إذا كان مبنيًا على خمسة أشخاص مختلفين على الأقل؛ عدد الصفوف ليس معيارًا بديلًا.

**المقترح:** ينشر متوسط العينة ذات الصفوف الستة.

**التفسير:** ستة صفوف قد تمثل ستة أشخاص أو أقل من خمسة؛ عدد الأشخاص المختلفين غير معلوم.

افتراضيًا: كل صف لشخص مختلف، فيكون العدد ستة.

افتراضيًا: الصفوف الستة تخص ثلاثة أشخاص فقط.

### en

**Context:** A sample table contains six rows. Multiple rows may belong to the same person, and person identifiers are unavailable in the supplied copy.

**Existing rule:** The sample mean may be published only if based on at least five distinct people; row count is not a substitute.

**Proposal:** Publish the mean of the six-row sample.

**Reason:** Six rows could represent six people or fewer than five; the distinct-person count is unknown.

Hypothetically: each row belongs to a different person, giving six people.

Hypothetically: the six rows belong to only three people.

## DEV-0042 — pilot-only obligation

التصنيف المقترح: **no_conflict** — مرجع التأليف: S022

### ar

**السياق:** العميل P ليس ضمن برنامج التجربة. العرض الجديد خاص بـP وحده ولا يغير عروض عملاء التجربة.

**القاعدة القائمة:** لعملاء برنامج التجربة فقط، يجب تضمين جلسة تهيئة مجانية؛ لا تفرض هذه القاعدة الجلسة على بقية العملاء.

**المقترح:** يقدم العرض إلى P دون جلسة تهيئة مجانية.

**التفسير:** P خارج التغطية الفعلية للالتزام؛ لا يوجد تعارض مع القاعدة المقدمة.

### en

**Context:** Customer P is not in the pilot program. The new offer is only for P and does not change pilot customers' offers.

**Existing rule:** For pilot-program customers only, a free onboarding session must be included; this rule does not require the session for other customers.

**Proposal:** Offer P a package without a free onboarding session.

**Reason:** P is outside the obligation's actual coverage; there is no conflict with the supplied rule.

## DEV-0043 — correction by append rather than replacement

التصنيف المقترح: **conflict** — مرجع التأليف: S006

### ar

**السياق:** القيد L في سجل التدقيق به خطأ إملائي. صاحب القيد معروف، لكن لون شاشة العرض غير محدد.

**القاعدة القائمة:** تصحح أخطاء سجل التدقيق بإضافة قيد تصحيح مرتبط بالأصل؛ يمنع تعديل القيد الأصلي أو استبداله، مهما صغر الخطأ.

**المقترح:** يستبدل نص L بالنص المصحح في المكان نفسه دون إبقاء النص السابق.

**التفسير:** الاستبدال ممنوع صراحة، ولا يستثني الخطأ الإملائي الصغير.

### en

**Context:** Entry L in the audit log has a spelling error. The entry's author is known, but the display screen's color is unspecified.

**Existing rule:** Audit-log errors must be corrected by appending a correction linked to the original; modifying or replacing the original entry is prohibited, however small the error.

**Proposal:** Replace L's text with the corrected text in the same location without retaining the previous text.

**Reason:** Replacement is explicitly prohibited, with no exception for a small spelling error.

## DEV-0044 — exception names a service rather than its owner

التصنيف المقترح: **conflict** — مرجع التأليف: S007

### ar

**السياق:** الخدمتان Search وPay يملكهما الفريق نفسه، لكنهما خدمتان مستقلتان. الاستثناء الموثق يسمي Search فقط، وفترة تجميد التغييرات ما زالت سارية.

**القاعدة القائمة:** يمنع تغيير أي خدمة خلال التجميد، إلا الخدمة المذكورة بالاسم في الاستثناء. لا يمتد الاستثناء إلى بقية خدمات الفريق.

**المقترح:** تُحدث Pay أثناء التجميد باستخدام الاستثناء الخاص بـSearch لأن المالك واحد.

**التفسير:** الاستثناء خاص بخدمة Search، والقرار يستهدف Pay.

### en

**Context:** Search and Pay are owned by the same team but are separate services. The documented exception names only Search, and the change-freeze period is still active.

**Existing rule:** Changes to any service are prohibited during the freeze except for the service named in the exception. The exception does not extend to the team's other services.

**Proposal:** Update Pay during the freeze using Search's exception because the owner is the same.

**Reason:** The exception is specific to Search, while the proposal targets Pay.

## DEV-0045 — active service time with unknown pause duration

التصنيف المقترح: **insufficient_information** — مرجع التأليف: S031

### ar

**السياق:** فتح الطلب عند 09:00 وأغلق عند 14:00 في اليوم نفسه. توقف العمل فترة واحدة لانتظار العميل، لكن مدة التوقف غير مذكورة.

**القاعدة القائمة:** الحد الأقصى ثلاث ساعات عمل فعلي؛ تخصم مدة انتظار العميل بالكامل من الزمن المنقضي.

**المقترح:** يسجل الطلب على أنه استوفى حد الثلاث ساعات.

**التفسير:** الزمن المنقضي خمس ساعات، ولا يعرف هل التوقف ساعتان على الأقل ليصبح العمل الفعلي ثلاث ساعات أو أقل.

افتراضيًا: استمر التوقف ساعتين؛ العمل الفعلي ثلاث ساعات.

افتراضيًا: استمر التوقف ساعة واحدة؛ العمل الفعلي أربع ساعات.

### en

**Context:** The request opened at 09:00 and closed at 14:00 the same day. Work paused once while waiting for the customer, but the pause duration is not stated.

**Existing rule:** The maximum is three active working hours; all customer-waiting time is subtracted from elapsed time.

**Proposal:** Record the request as meeting the three-hour limit.

**Reason:** Elapsed time is five hours; it is unknown whether the pause was at least two hours, making active time at most three hours.

Hypothetically: the pause lasted two hours, leaving three active hours.

Hypothetically: the pause lasted one hour, leaving four active hours.
