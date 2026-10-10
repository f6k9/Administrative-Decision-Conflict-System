# ITISAQ — مراجعة 300 سيناريو إداري ثنائي اللغة

مسودة اصطناعية بإجابات مقترحة بعد مراجعة AI ذاتية. تحتاج مراجعة بشرية مستقلة قبل اعتمادها بحثيًا. اقرأ README_AR.md لتعريف المهمة وافتراضاتها وحدودها. لا ترسل هذا الملف للنماذج المرشحة لأنه يحتوي الإجابات.

صلاحيات المصدر ونطاقه المسموح مفترضان متحققين؛ المطلوب مقارنة معنى القرارين وتغطيتهما الفعلية. كل سيناريو مستقل عن بقية السيناريوهات، ولا تطبق قواعد خارج النص.

## ADM-0001 — payroll / proportional allowance

عائلة المراجعة: F087 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: البدل الكامل 800 وحدة، والموظف يعمل بنصف دوام طوال الشهر.
- القرار السابق: يُصرف البدل بنسبة الدوام فقط؛ نصف الدوام يستحق نصف البدل الكامل.
- القرار الجديد: يُصرف لموظف آخر بدل 600 وحدة، ونسبة دوامه غير مذكورة.
- سبب الإجابة المقترحة: يلزم نسبة دوام الموظف الآخر لحساب استحقاقه.

### English

- Context: The full allowance is 800 units, and the employee works half-time throughout the month.
- Existing decision: The allowance is paid strictly in proportion to working fraction; half-time receives half the full allowance.
- New decision: Another employee receives an allowance of 600 units, and their working fraction is unspecified.
- Proposed answer rationale: The other employee's working fraction is needed to calculate entitlement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0002 — meetings / minutes status

عائلة المراجعة: F054 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المحضر M مسودة لم تعتمد بعد. السماح بالتداول الداخلي للمراجعة لا يعد نشرًا نهائيًا.
- القرار السابق: يُمنع نشر المحضر بوصفه نهائيًا قبل اعتماده، ويُسمح بتداوله داخليًا كمسودة للمراجعة.
- القرار الجديد: يُنشر M الآن بوصفه المحضر النهائي المعتمد.
- سبب الإجابة المقترحة: المسودة غير المعتمدة نُشرت بوصفها نهائية.

### English

- Context: Minutes M are an unapproved draft. Internal circulation for review does not count as final publication.
- Existing decision: Minutes must not be published as final before approval; internal circulation as a review draft is allowed.
- New decision: M is published now as the final approved minutes.
- Proposed answer rationale: The unapproved draft is published as final.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0003 — payroll / non-cumulative alternatives

عائلة المراجعة: F088 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: البدلان A وB يغطيان الغرض نفسه، ويمكن اختيار أحدهما خلال الشهر.
- القرار السابق: يجوز صرف A أو B للموظف في الشهر، ويُمنع الجمع بينهما في الشهر نفسه.
- القرار الجديد: يُصرف A عن مارس وB عن أبريل دون صرف البدل الآخر في أي منهما.
- سبب الإجابة المقترحة: البدلان لفترتين منفصلتين دون جمع شهري.

### English

- Context: Allowances A and B cover the same purpose, and one may be chosen for the month.
- Existing decision: An employee may receive A or B for a month, but must not receive both for that same month.
- New decision: A is paid for March and B for April, with no other allowance paid in either month.
- Proposed answer rationale: The allowances concern separate periods with no monthly combination.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0004 — facilities / emergency access

عائلة المراجعة: F050 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: ممر E مخرج الطوارئ الوحيد. المخزن S منفصل ولا يدخل في مسار الإخلاء.
- القرار السابق: يجب بقاء ممر E خاليًا من أي صناديق طوال الوقت.
- القرار الجديد: توضع صناديق في ممر E لمدة عشر دقائق.
- سبب الإجابة المقترحة: المنع يشمل حتى التخزين المؤقت.

### English

- Context: Passage E is the only emergency exit route. Store S is separate and outside the evacuation route.
- Existing decision: Passage E must remain free of boxes at all times.
- New decision: Boxes are placed in passage E for ten minutes.
- Proposed answer rationale: The prohibition includes temporary storage.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0005 — it_access / read versus write

عائلة المراجعة: F026 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحساب C حساب متعاقد. تنزيل نسخة محلية يعد قراءة، وتعديل الأصل يعد كتابة.
- القرار السابق: يسمح لحسابات المتعاقدين بقراءة المجلد المشترك فقط، وتُمنع الكتابة فيه.
- القرار الجديد: يُمنح الحساب C دور Contributor، ولا تتوفر تفاصيل صلاحيات هذا الدور.
- سبب الإجابة المقترحة: اسم الدور لا يوضح إن كان يسمح بالكتابة.

### English

- Context: Account C is a contractor account. Downloading a local copy counts as reading; changing the original counts as writing.
- Existing decision: Contractor accounts may only read the shared folder; writing to it is prohibited.
- New decision: Account C receives the Contributor role, whose permissions are unavailable.
- Proposed answer rationale: The role name does not establish whether it allows writing.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0006 — recruitment / vacancy approval

عائلة المراجعة: F081 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الشاغر V1 معتمد وممول، والشاغر V2 مقترح ولم يعتمد. حالة V3 غير متاحة.
- القرار السابق: لا يُعلن توظيف إلا لشاغر معتمد وممول معًا.
- القرار الجديد: يُنشر إعلان توظيف للشاغر V3.
- سبب الإجابة المقترحة: يلزم التحقق من اعتماد V3 وتمويله.

### English

- Context: Vacancy V1 is approved and funded; V2 is proposed and unapproved. V3's status is unavailable.
- Existing decision: Recruitment may be advertised only for a vacancy that is both approved and funded.
- New decision: A recruitment advertisement is published for V3.
- Proposed answer rationale: V3's approval and funding status must be established.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0007 — payroll / bank detail change confirmation

عائلة المراجعة: F090 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: التأكيد المستقل اتصال موثق بالموظف باستخدام رقم معروف سابقًا. رسالة طلب التغيير وحدها ليست تأكيدًا مستقلًا.
- القرار السابق: لا يُفعّل تغيير الحساب البنكي في الرواتب قبل التأكيد المستقل.
- القرار الجديد: يُفعّل التغيير بعد وضع علامة تم التحقق، دون وصف طريقة التحقق.
- سبب الإجابة المقترحة: يلزم معرفة هل التحقق مستقل بالطريقة المحددة.

### English

- Context: Independent confirmation is a documented call to the employee using a previously known number. The change-request message alone is not independent confirmation.
- Existing decision: A bank-account change in payroll must not be activated before independent confirmation.
- New decision: The change is activated after marking it Verified, without describing the verification method.
- Proposed answer rationale: It is necessary to know whether verification was independent in the specified way.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0008 — logistics / unit conversion

عائلة المراجعة: F092 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: كل صندوق يحتوي 12 وحدة. أمر التسليم يتطلب كمية محددة دون زيادة أو نقص.
- القرار السابق: يجب تسليم 120 وحدة بالضبط للعميل.
- القرار الجديد: يُغلق أمر التسليم بعد تسليم عشرة صناديق.
- سبب الإجابة المقترحة: عشرة صناديق تساوي 120 وحدة.

### English

- Context: Each box contains 12 units. The delivery order requires an exact quantity with no excess or shortage.
- Existing decision: Exactly 120 units must be delivered to the customer.
- New decision: The delivery order is closed after ten boxes are delivered.
- Proposed answer rationale: Ten boxes equal 120 units.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0009 — records / destruction witnesses

عائلة المراجعة: F040 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: إتلاف السجلات يتطلب حضور شهود فعليين، وتوقيع غائب لا يعد حضورًا.
- القرار السابق: يجب حضور شاهدين على الأقل عند إتلاف السجلات.
- القرار الجديد: يتم الإتلاف بحضور شاهد واحد، ويوقع شاهد ثانٍ غائب لاحقًا.
- سبب الإجابة المقترحة: الحضور الفعلي أقل من شاهدين.

### English

- Context: Record destruction requires witnesses to be physically present; an absent person's signature does not count as attendance.
- Existing decision: At least two witnesses must be present during record destruction.
- New decision: Destruction occurs with one witness present, and a second absent witness signs later.
- Proposed answer rationale: Fewer than two witnesses are physically present.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0010 — inventory / asset traceability

عائلة المراجعة: F079 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: جميع الأجهزة في هذه الحالة أصول مرقمة. التسجيل يجب أن يربط رقم الجهاز بمستلمه.
- القرار السابق: لا يُسلم جهاز إلا بعد تسجيل رقمه التسلسلي واسم مستلمه معًا.
- القرار الجديد: يُسلم الجهاز بعد تسجيل اسم المستلم فقط دون الرقم التسلسلي.
- سبب الإجابة المقترحة: أحد حقلي التتبع الإلزاميين مفقود.

### English

- Context: All devices in this case are numbered assets. Registration must link the device number to its recipient.
- Existing decision: A device must not be handed over until both its serial number and recipient's name are recorded.
- New decision: The device is handed over after recording only the recipient's name without the serial number.
- Proposed answer rationale: One of the mandatory tracking fields is missing.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0011 — projects / aggregate staff allocation

عائلة المراجعة: F099 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الموظف E متاح 30 ساعة للمشاريع خلال الأسبوع، ولا يسمح بتجاوز هذه الطاقة.
- القرار السابق: يجب ألا يتجاوز مجموع ساعات تكليف E في جميع المشاريع 30 ساعة لهذا الأسبوع.
- القرار الجديد: يُكلف E بعشرين ساعة في A وعشر ساعات في B، ولا تكليفات أخرى هذا الأسبوع.
- سبب الإجابة المقترحة: إجمالي التكليف 30 ساعة ضمن الطاقة.

### English

- Context: Employee E has 30 hours available for projects during the week, and this capacity must not be exceeded.
- Existing decision: E's total assigned hours across all projects must not exceed 30 this week.
- New decision: E is assigned twenty hours to A and ten to B, with no other assignments this week.
- Proposed answer rationale: The total assignment is 30 hours, within capacity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0012 — customer_service / response versus resolution

عائلة المراجعة: F066 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الرد الأول والتسوية النهائية إجراءان مختلفان. الوقت محسوب من تسجيل الشكوى.
- القرار السابق: يجب إرسال رد أول خلال أربع ساعات، وإتمام التسوية النهائية خلال خمسة أيام.
- القرار الجديد: تُنجز التسوية في اليوم الرابع، وتوقيت الرد الأول غير موضح.
- سبب الإجابة المقترحة: يلزم توقيت الرد الأول لتقييم الشرطين معًا.

### English

- Context: An initial response and final resolution are different actions. Time is measured from complaint registration.
- Existing decision: An initial response must be sent within four hours, and final resolution completed within five days.
- New decision: Resolution is completed on day four, and the initial-response timing is unspecified.
- Proposed answer rationale: The initial-response timing is needed to assess both conditions.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0013 — training / certificate validity

عائلة المراجعة: F057 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: تاريخ انتهاء الشهادة مشمول بصلاحيتها. يلزم أن تكون صالحة طوال تشغيل الجهاز.
- القرار السابق: لا يُكلف موظف بتشغيل الجهاز دون شهادة صالحة وقت التشغيل.
- القرار الجديد: يشغل الموظف الجهاز يوم 2030-11-02 بشهادة انتهت في 2030-10-31.
- سبب الإجابة المقترحة: الشهادة منتهية وقت التشغيل.

### English

- Context: The certificate's expiry date is included in its validity. It must remain valid throughout equipment operation.
- Existing decision: An employee must not be assigned to operate the equipment without a certificate valid at the time of operation.
- New decision: The employee operates the equipment on 2030-11-02 with a certificate that expired on 2030-10-31.
- Proposed answer rationale: The certificate is expired at operation time.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0014 — inventory / asset traceability

عائلة المراجعة: F079 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: جميع الأجهزة في هذه الحالة أصول مرقمة. التسجيل يجب أن يربط رقم الجهاز بمستلمه.
- القرار السابق: لا يُسلم جهاز إلا بعد تسجيل رقمه التسلسلي واسم مستلمه معًا.
- القرار الجديد: يُسلم الجهاز بعد تسجيل رقمه التسلسلي واسم المستلم في السجل نفسه.
- سبب الإجابة المقترحة: الحقول المطلوبة مسجلة ومترابطة.

### English

- Context: All devices in this case are numbered assets. Registration must link the device number to its recipient.
- Existing decision: A device must not be handed over until both its serial number and recipient's name are recorded.
- New decision: The device is handed over after its serial number and recipient's name are recorded together.
- Proposed answer rationale: The required fields are recorded and linked.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0015 — training / certificate validity

عائلة المراجعة: F057 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: تاريخ انتهاء الشهادة مشمول بصلاحيتها. يلزم أن تكون صالحة طوال تشغيل الجهاز.
- القرار السابق: لا يُكلف موظف بتشغيل الجهاز دون شهادة صالحة وقت التشغيل.
- القرار الجديد: يشغل الموظف الجهاز اليوم، وتاريخ انتهاء شهادته غير معلوم.
- سبب الإجابة المقترحة: يلزم تاريخ الانتهاء للتحقق من الصلاحية.

### English

- Context: The certificate's expiry date is included in its validity. It must remain valid throughout equipment operation.
- Existing decision: An employee must not be assigned to operate the equipment without a certificate valid at the time of operation.
- New decision: The employee operates the equipment today, and the certificate expiry date is unknown.
- Proposed answer rationale: The expiry date is needed to verify validity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0016 — communications / approval covers exact text

عائلة المراجعة: F063 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الموافقة الإعلامية مرتبطة بالنص الذي روجع تحديدًا. تعديل الحقائق يتطلب موافقة جديدة.
- القرار السابق: لا يُنشر بيان إعلامي إلا إذا اعتمدت نسخة النص المنشورة نفسها.
- القرار الجديد: يُنشر البيان بعد تغيير قيمة مالية فيه، دون مراجعة جديدة، اعتمادًا على موافقة النسخة القديمة.
- سبب الإجابة المقترحة: الموافقة السابقة لا تشمل النص المعدل.

### English

- Context: Media approval covers the exact reviewed text. Changing factual content requires new approval.
- Existing decision: A media statement may be published only if the exact published text version has been approved.
- New decision: The statement is published after changing a financial figure, without a new review, using the old version's approval.
- Proposed answer rationale: The prior approval does not cover the revised text.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0017 — attendance / weekly ceiling

عائلة المراجعة: F003 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: جميع الساعات المذكورة ساعات عمل فعلية لنفس الموظف في الأسبوع نفسه.
- القرار السابق: لا يجوز أن يتجاوز عمل الموظف 40 ساعة في الأسبوع.
- القرار الجديد: تضاف خمس ساعات عمل هذا الأسبوع، ولا يُذكر مجموع الساعات الأخرى.
- سبب الإجابة المقترحة: يلزم مجموع الساعات قبل الإضافة.

### English

- Context: All stated hours are actual working hours for the same employee in the same week.
- Existing decision: The employee must not work more than 40 hours per week.
- New decision: Five working hours are added this week, but the total of the other hours is unspecified.
- Proposed answer rationale: The total hours before the addition are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0018 — finance / reporting period scope

عائلة المراجعة: F044 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: بند Q1 يخص الربع الأول وبند Q2 الربع الثاني، والفترتان غير متداخلتين.
- القرار السابق: تُمنع أي مصروفات جديدة على بند Q1 بعد إقفاله.
- القرار الجديد: يُسجل مصروف جديد على Q1 بعد الإقفال.
- سبب الإجابة المقترحة: المصروف يخص البند المقفل بعد إقفاله.

### English

- Context: Budget line Q1 covers the first quarter and Q2 the second quarter; the periods do not overlap.
- Existing decision: New expenses against Q1 are prohibited after it is closed.
- New decision: A new expense is posted against Q1 after closure.
- Proposed answer rationale: The expense is against the closed line after closure.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0019 — training / delivery modality exception

عائلة المراجعة: F059 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الوحدة P عملية وتتطلب معدات فعلية، والوحدة T نظرية. نوع الوحدة X غير موثق.
- القرار السابق: تُقدم الوحدات العملية حضوريًا فقط، ويجوز تقديم الوحدات النظرية عن بعد.
- القرار الجديد: تُقدم الوحدة T كاملة عن بعد.
- سبب الإجابة المقترحة: التقديم عن بعد مسموح للوحدة النظرية.

### English

- Context: Module P is practical and requires physical equipment; module T is theoretical. Module X's type is undocumented.
- Existing decision: Practical modules must be delivered in person only; theoretical modules may be delivered remotely.
- New decision: Module T is delivered entirely remotely.
- Proposed answer rationale: Remote delivery is allowed for the theoretical module.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0020 — recruitment / anonymous screening stage

عائلة المراجعة: F084 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الفرز الأولي يسبق المقابلات. أسماء المرشحين محجوبة في الفرز ومسموحة للمقابلين عند المقابلة.
- القرار السابق: تُحجب أسماء المرشحين عن المقيمين أثناء الفرز الأولي فقط.
- القرار الجديد: تُعرض الأسماء على فريق التقييم دون تحديد مرحلة العملية.
- سبب الإجابة المقترحة: يلزم تحديد هل التقييم فرز أولي أم مقابلة.

### English

- Context: Initial screening precedes interviews. Candidate names are hidden during screening and available to interviewers at interview time.
- Existing decision: Candidate names must be hidden from assessors during initial screening only.
- New decision: Names are shown to the assessment team without identifying the process stage.
- Proposed answer rationale: It is necessary to know whether assessment means initial screening or interview.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0021 — quality / all versus most

عائلة المراجعة: F073 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: يوجد عشرة عيوب حرجة في الإصدار. إغلاق العيب يعني التحقق من إصلاحه.
- القرار السابق: لا يُطلق الإصدار إلا بعد إغلاق جميع العيوب الحرجة.
- القرار الجديد: يُطلق الإصدار بعد إعلان الفريق اكتمال الإصلاحات، دون بيان حالة التحقق أو إغلاق العيوب.
- سبب الإجابة المقترحة: إكمال الإصلاح المعلن لا يثبت الإغلاق المتحقق منه.

### English

- Context: The release has ten critical defects. Closing a defect means its repair has been verified.
- Existing decision: The release must not be launched until all critical defects are closed.
- New decision: The release is launched after the team announces repairs are complete, without stating verification or defect-closure status.
- Proposed answer rationale: Reported repair completion does not establish verified closure.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0022 — finance / budget balance

عائلة المراجعة: F041 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المتبقي المتاح في بند الصيانة 7000 وحدة، ولا يسمح بتحويل مبالغ إليه ضمن هذه الحالات.
- القرار السابق: يُمنع اعتماد التزامات مالية تتجاوز الرصيد المتاح للبند.
- القرار الجديد: يُعتمد التزام صيانة جديد بقيمة 7500 وحدة من هذا البند.
- سبب الإجابة المقترحة: الالتزام أكبر من الرصيد المتاح.

### English

- Context: The maintenance budget has 7000 units available, and no transfers into it are permitted in these cases.
- Existing decision: Financial commitments exceeding the budget line's available balance must not be approved.
- New decision: A new maintenance commitment of 7500 units is approved against this budget line.
- Proposed answer rationale: The commitment exceeds the available balance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0023 — communications / recommendation versus prohibition

عائلة المراجعة: F064 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: القناة A مفضلة لكنها ليست إلزامية، والقناتان A وB معتمدتان ومتاحتان لهذه الرسائل.
- القرار السابق: يُنصح باستخدام A عند الإمكان، ويظل استخدام B مسموحًا دون موافقة إضافية. يُمنع استخدام أي قناة غير معتمدة.
- القرار الجديد: تُرسل الرسالة عبر القناة البديلة، دون تحديد هل المقصود A أو B أو قناة غير معتمدة.
- سبب الإجابة المقترحة: يلزم تعريف القناة والحكم الذي يسري عليها.

### English

- Context: Channel A is preferred but not mandatory; channels A and B are both approved and available for these messages.
- Existing decision: Use of A is recommended when possible, while B remains allowed without additional approval. Use of any unapproved channel is prohibited.
- New decision: The message is sent through the alternative channel, without identifying whether it means A, B, or an unapproved channel.
- Proposed answer rationale: The channel and the rule applicable to it must be identified.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0024 — attendance / mandatory location

عائلة المراجعة: F001 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الموظفون المقصودون هم موظفو القسم A يوم 2030-04-07، ولا يوجد استثناء للعمل عن بعد.
- القرار السابق: يجب على موظفي القسم A أداء دوام ذلك اليوم كاملًا في المكتب.
- القرار الجديد: يؤدي هؤلاء الموظفون دوام ذلك اليوم كاملًا في الموقع X، دون بيان عنوانه.
- سبب الإجابة المقترحة: يلزم معرفة هل الموقع X هو المكتب أم موقع آخر.

### English

- Context: The people concerned are Department A employees on 2030-04-07. No remote-work exception applies.
- Existing decision: Department A employees must work that entire day in the office.
- New decision: These employees must work that entire day at site X, whose address is unspecified.
- Proposed answer rationale: It is necessary to know whether site X is the office or a different location.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0025 — projects / explicit authority does not erase conflict

عائلة المراجعة: F100 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: كلا المصدرين مخول بإصدار توجيهات للمشروع P. التوجيه الجديد صادر من جهة أعلى، لكنه لا يتضمن إلغاءً أو استثناءً للتوجيه الساري. نقيّم تعارض المتطلبات، لا أولوية التنفيذ.
- القرار السابق: يجب على المشروع P الاحتفاظ بسجلات الاختبار حتى إقفاله، ويُمنع حذفها قبل الإقفال. هذا التوجيه لا يفرض الاحتفاظ بعد الإقفال.
- القرار الجديد: تأمر الجهة الأعلى بإنشاء نسخة احتياطية لسجلات P مع الاحتفاظ بالأصل حتى الإقفال.
- سبب الإجابة المقترحة: إنشاء النسخة مع إبقاء الأصل ينسجم مع الاحتفاظ.

### English

- Context: Both issuers are authorized to direct project P. The new directive comes from a higher authority but contains no repeal or exception to the effective directive. Assess requirement conflict, not implementation priority.
- Existing decision: Project P must retain its test records until closure, and deletion before closure is prohibited. This directive imposes no retention requirement after closure.
- New decision: The higher authority orders a backup of P's records while retaining the originals until closure.
- Proposed answer rationale: Creating a backup while keeping the originals is compatible with retention.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0026 — payroll / aggregate deduction ceiling

عائلة المراجعة: F089 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: هذه قاعدة داخلية افتراضية للاختبار. الراتب الأساسي 5000 وحدة، والحد يشمل مجموع الخصومات المذكورة.
- القرار السابق: لا يتجاوز مجموع هذه الخصومات 10% من الراتب الأساسي في الشهر.
- القرار الجديد: يُطبق خصمان في الشهر نفسه، كل منهما 200 وحدة، ولا خصومات أخرى.
- سبب الإجابة المقترحة: المجموع 400 ضمن الحد 500.

### English

- Context: This is a fictional internal test rule. Basic salary is 5000 units, and the cap covers the total of the stated deductions.
- Existing decision: The total of these deductions must not exceed 10% of monthly basic salary.
- New decision: Two deductions of 200 units each are applied in the same month, with no other deductions.
- Proposed answer rationale: The total of 400 is within the cap of 500.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0027 — it_access / read versus write

عائلة المراجعة: F026 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحساب C حساب متعاقد. تنزيل نسخة محلية يعد قراءة، وتعديل الأصل يعد كتابة.
- القرار السابق: يسمح لحسابات المتعاقدين بقراءة المجلد المشترك فقط، وتُمنع الكتابة فيه.
- القرار الجديد: يُمنح الحساب C حق تنزيل نسخ محلية دون تعديل الأصل.
- سبب الإجابة المقترحة: الصلاحية الممنوحة قراءة فقط.

### English

- Context: Account C is a contractor account. Downloading a local copy counts as reading; changing the original counts as writing.
- Existing decision: Contractor accounts may only read the shared folder; writing to it is prohibited.
- New decision: Account C receives permission to download local copies without changing the originals.
- Proposed answer rationale: The granted permission is read-only.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0028 — leave / staffing floor

عائلة المراجعة: F010 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: القسم فيه خمسة موظفين مجدولين في اليوم المقصود، ومن يأخذ إجازة لا يكون حاضرًا.
- القرار السابق: يجب بقاء ثلاثة موظفين على الأقل حاضرين في القسم كل يوم.
- القرار الجديد: تُمنح إجازة في اليوم نفسه لثلاثة من الموظفين الخمسة، ويحضر الباقون.
- سبب الإجابة المقترحة: يتبقى موظفان فقط، أقل من ثلاثة.

### English

- Context: The department has five employees scheduled for the day concerned, and anyone on leave is absent.
- Existing decision: At least three employees must remain present in the department every day.
- New decision: Three of the five employees receive leave on the same day, and the others attend.
- Proposed answer rationale: Only two employees remain, fewer than three.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0029 — communications / recipient classification

عائلة المراجعة: F065 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: النشرة الفنية للمجموعة T فقط. الموظفة U ضمن T، والموظف V خارج T.
- القرار السابق: تُوزع النشرة الفنية على أعضاء T فقط.
- القرار الجديد: تُرسل النشرة إلى القائمة L، وعضوية مستلمي القائمة غير متاحة.
- سبب الإجابة المقترحة: يلزم معرفة هل جميع المستلمين أعضاء في T.

### English

- Context: The technical bulletin is for group T only. Employee U belongs to T, and employee V is outside T.
- Existing decision: The technical bulletin must be distributed only to members of T.
- New decision: The bulletin is sent to list L, and its recipients' group membership is unavailable.
- Proposed answer rationale: It is necessary to know whether all recipients belong to T.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0030 — logistics / route approval specific scope

عائلة المراجعة: F095 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الطريق A معتمد للشاحنات الثقيلة فقط، والطريق B معتمد للمركبات الخفيفة فقط.
- القرار السابق: يجب أن تسلك كل مركبة الطريق المعتمد لفئتها فقط.
- القرار الجديد: تسلك شاحنة ثقيلة الطريق B.
- سبب الإجابة المقترحة: B غير معتمد لفئة المركبة الثقيلة.

### English

- Context: Route A is approved only for heavy trucks; route B is approved only for light vehicles.
- Existing decision: Each vehicle must use only the route approved for its category.
- New decision: A heavy truck uses route B.
- Proposed answer rationale: B is not approved for the heavy-vehicle category.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0031 — attendance / prior approval

عائلة المراجعة: F004 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الموظف R سيؤدي ساعتين إضافيتين مساء اليوم. لا توجد استثناءات من شرط الموافقة.
- القرار السابق: لا يبدأ العمل الإضافي إلا بعد تسجيل موافقة المدير.
- القرار الجديد: يبدأ R العمل الإضافي الآن، وحالة تسجيل الموافقة غير معروفة.
- سبب الإجابة المقترحة: يلزم معرفة هل سُجلت الموافقة قبل البدء.

### English

- Context: Employee R will work two overtime hours this evening. There are no exceptions to the approval requirement.
- Existing decision: Overtime must not start until the manager's approval is recorded.
- New decision: R starts overtime now, and the approval-recording status is unknown.
- Proposed answer rationale: It is necessary to know whether approval was recorded before the start.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0032 — procurement / split orders

عائلة المراجعة: F017 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحد هو 8000 وحدة للحاجة الواحدة. الغرض من التقسيم مذكور صراحة عند توفره.
- القرار السابق: يُمنع تقسيم حاجة شرائية واحدة إلى طلبات أصغر بهدف تجاوز مراجعة الحد المالي.
- القرار الجديد: تُقسم حاجة واحدة بقيمة 12000 إلى طلبين بقيمة 6000 لكل منهما لتجاوز المراجعة.
- سبب الإجابة المقترحة: التقسيم صريح والغرض منه تجاوز المراجعة.

### English

- Context: The threshold is 8000 units per purchasing need. The purpose of splitting is stated explicitly when available.
- Existing decision: A single purchasing need must not be split into smaller orders to bypass the financial-threshold review.
- New decision: One need worth 12000 is split into two orders of 6000 each to bypass review.
- Proposed answer rationale: The split and its review-bypass purpose are explicit.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0033 — customer_service / refund eligibility OR

عائلة المراجعة: F068 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحالة مستوفية لشروط الاسترداد الأخرى. العيب المثبت والتسليم الخاطئ سببان بديلان.
- القرار السابق: يحق للعميل الاسترداد عند وجود عيب مثبت أو تسليم صنف خاطئ؛ وفي غير ذلك يُرفض الاسترداد.
- القرار الجديد: يُقبل الاسترداد لصنف غير معيب لكنه سُلّم خطأً.
- سبب الإجابة المقترحة: التسليم الخاطئ وحده يحقق الشرط البديل.

### English

- Context: The case satisfies the other refund conditions. A confirmed defect and wrong delivery are alternative qualifying reasons.
- Existing decision: A customer is entitled to a refund for either a confirmed defect or delivery of the wrong item; otherwise a refund is denied.
- New decision: A refund is accepted for a non-defective item that was wrongly delivered.
- Proposed answer rationale: Wrong delivery alone satisfies an alternative condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0034 — quality / alternative evidence routes

عائلة المراجعة: F075 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الوثيقتان A وB بديلتان مقبولتان، ولا توجد شروط إثبات أخرى لهذه الخطوة.
- القرار السابق: يجوز إغلاق الملاحظة بتقرير اختبار A أو بشهادة مطابقة B؛ لا يجوز إغلاقها دون أحدهما.
- القرار الجديد: تُغلق الملاحظة مع التأكيد بعدم وجود A أو B.
- سبب الإجابة المقترحة: لا يوجد أي من البديلين المقبولين.

### English

- Context: Documents A and B are acceptable alternatives, with no other evidence conditions for this step.
- Existing decision: A finding may be closed with either test report A or conformity certificate B; it must not be closed without one of them.
- New decision: The finding is closed while confirming that neither A nor B exists.
- Proposed answer rationale: Neither acceptable alternative is present.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0035 — recruitment / application window

عائلة المراجعة: F085 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المدة تقاس بعدد أيام تقويمية كاملة يبقى الإعلان خلالها مفتوحًا لاستقبال الطلبات.
- القرار السابق: يجب إبقاء إعلان الوظيفة مفتوحًا لمدة عشرة أيام على الأقل.
- القرار الجديد: يُغلق الإعلان نهائيًا بعد ستة أيام كاملة من فتحه.
- سبب الإجابة المقترحة: الفترة أقل من عشرة أيام.

### English

- Context: Duration is measured in full calendar days during which the advertisement remains open for applications.
- Existing decision: A job advertisement must remain open for at least ten days.
- New decision: The advertisement closes permanently after six full days of being open.
- Proposed answer rationale: The period is shorter than ten days.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0036 — inventory / calibration expiry

عائلة المراجعة: F077 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الجهاز A معاير وصالح، والجهاز B انتهت معايرته، ولا يوجد تمديد له.
- القرار السابق: تُستخدم في القياس أجهزة ذات معايرة سارية فقط.
- القرار الجديد: يُستخدم B للقياس لأنه يعمل ظاهريًا دون أعطال.
- سبب الإجابة المقترحة: سلامة التشغيل الظاهرية لا تعني سريان المعايرة.

### English

- Context: Device A has valid calibration; device B's calibration has expired without extension.
- Existing decision: Only devices with valid calibration may be used for measurement.
- New decision: B is used for measurement because it appears to function without faults.
- Proposed answer rationale: Apparent functionality does not establish valid calibration.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0037 — customer_service / branch-specific hours

عائلة المراجعة: F069 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الفرعان الشرقي والغربي وحدتان مستقلتان. ساعات العمل كلها محلية لليوم نفسه.
- القرار السابق: يجب أن يبقى مكتب خدمة العملاء في الفرع الشرقي مفتوحًا من 09:00 حتى 17:00.
- القرار الجديد: يُغلق مكتب الخدمة في الفرع الشرقي الساعة 15:00 بقية اليوم.
- سبب الإجابة المقترحة: الإغلاق يقطع ساعتين من الفترة المطلوبة.

### English

- Context: The eastern and western branches are separate units. All hours are local and concern the same day.
- Existing decision: The eastern branch's customer-service desk must remain open from 09:00 until 17:00.
- New decision: The eastern branch's service desk closes at 15:00 for the rest of the day.
- Proposed answer rationale: Closure removes two hours of the required opening period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0038 — customer_service / priority ordering

عائلة المراجعة: F067 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الطلبان مفتوحان وجاهزان للمعالجة، وتوجد قدرة لمعالجة طلب واحد في كل مرة.
- القرار السابق: تُعالج الطلبات الحرجة قبل الطلبات العادية، مهما كان ترتيب وصولها.
- القرار الجديد: يُعالج الطلب العادي قبل الحرج لأنه وصل أولًا.
- سبب الإجابة المقترحة: ترتيب الوصول لا يتجاوز أولوية الطلب الحرج.

### English

- Context: Both requests are open and ready for processing, with capacity to process one at a time.
- Existing decision: Critical requests must be processed before ordinary requests, regardless of arrival order.
- New decision: The ordinary request is processed before the critical one because it arrived first.
- Proposed answer rationale: Arrival order does not override critical-request priority.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0039 — logistics / unit conversion

عائلة المراجعة: F092 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: كل صندوق يحتوي 12 وحدة. أمر التسليم يتطلب كمية محددة دون زيادة أو نقص.
- القرار السابق: يجب تسليم 120 وحدة بالضبط للعميل.
- القرار الجديد: يُغلق أمر التسليم بعد تسليم تسعة صناديق فقط.
- سبب الإجابة المقترحة: تسعة صناديق تساوي 108 وحدات، أقل من 120.

### English

- Context: Each box contains 12 units. The delivery order requires an exact quantity with no excess or shortage.
- Existing decision: Exactly 120 units must be delivered to the customer.
- New decision: The delivery order is closed after only nine boxes are delivered.
- Proposed answer rationale: Nine boxes equal 108 units, fewer than 120.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0040 — finance / reporting period scope

عائلة المراجعة: F044 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: بند Q1 يخص الربع الأول وبند Q2 الربع الثاني، والفترتان غير متداخلتين.
- القرار السابق: تُمنع أي مصروفات جديدة على بند Q1 بعد إقفاله.
- القرار الجديد: يُسجل المصروف بعد إقفال Q1، دون تحديد البند الذي سيتحمله.
- سبب الإجابة المقترحة: يلزم تحديد البند المستهدف.

### English

- Context: Budget line Q1 covers the first quarter and Q2 the second quarter; the periods do not overlap.
- Existing decision: New expenses against Q1 are prohibited after it is closed.
- New decision: The expense is posted after Q1 closes without identifying the charged budget line.
- Proposed answer rationale: The charged budget line is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0041 — travel / restricted destination

عائلة المراجعة: F013 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المنطقة R محظورة للسفر الوظيفي، والمنطقة S غير محظورة. الرحلات كلها وظيفية.
- القرار السابق: يُمنع تكليف الموظفين بمهمات داخل المنطقة R.
- القرار الجديد: يُكلف الموظف بمهمة في مدينة موضح أنها داخل R.
- سبب الإجابة المقترحة: المهمة تقع داخل المنطقة المحظورة.

### English

- Context: Region R is restricted for business travel, and Region S is not restricted. All trips are business trips.
- Existing decision: Employees must not be assigned missions inside Region R.
- New decision: The employee is assigned a mission in a city explicitly located inside R.
- Proposed answer rationale: The mission is inside the restricted region.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0042 — finance / cash custody

عائلة المراجعة: F042 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الخزنة A معتمدة للنقد، والخزانة المكتبية B غير معتمدة. المكان X غير موصوف.
- القرار السابق: يجب حفظ النقد المتبقي ليلًا داخل خزنة معتمدة.
- القرار الجديد: يُترك النقد ليلًا في الخزانة B.
- سبب الإجابة المقترحة: مكان الحفظ ليس خزنة معتمدة.

### English

- Context: Safe A is approved for cash, while office cabinet B is not. Location X is undescribed.
- Existing decision: Cash remaining overnight must be kept in an approved safe.
- New decision: Cash is left overnight in cabinet B.
- Proposed answer rationale: The storage location is not an approved safe.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0043 — facilities / emergency access

عائلة المراجعة: F050 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: ممر E مخرج الطوارئ الوحيد. المخزن S منفصل ولا يدخل في مسار الإخلاء.
- القرار السابق: يجب بقاء ممر E خاليًا من أي صناديق طوال الوقت.
- القرار الجديد: توضع الصناديق في الممر الخلفي، ولا يُعرف هل هو E.
- سبب الإجابة المقترحة: يلزم تحديد علاقة الممر الخلفي بممر E.

### English

- Context: Passage E is the only emergency exit route. Store S is separate and outside the evacuation route.
- Existing decision: Passage E must remain free of boxes at all times.
- New decision: Boxes are placed in the rear passage, and it is unknown whether that is E.
- Proposed answer rationale: The relationship between the rear passage and E is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0044 — it_access / shared identity

عائلة المراجعة: F029 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: منصة العمليات تتطلب حساب مستخدم لكل شخص، ولا توجد حسابات مشتركة مستثناة.
- القرار السابق: يُمنع استخدام حساب مستخدم واحد بواسطة أكثر من موظف.
- القرار الجديد: يستخدم كل موظف حسابه الفردي على جهاز مشترك.
- سبب الإجابة المقترحة: اشتراك الجهاز لا يعني اشتراك حساب المستخدم.

### English

- Context: The operations platform requires a user account for each person, with no exempt shared accounts.
- Existing decision: More than one employee must not use the same user account.
- New decision: Each employee uses their individual account on a shared device.
- Proposed answer rationale: Sharing a device does not mean sharing a user account.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0045 — payroll / proportional allowance

عائلة المراجعة: F087 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: البدل الكامل 800 وحدة، والموظف يعمل بنصف دوام طوال الشهر.
- القرار السابق: يُصرف البدل بنسبة الدوام فقط؛ نصف الدوام يستحق نصف البدل الكامل.
- القرار الجديد: يُصرف لهذا الموظف بدل 400 وحدة عن الشهر.
- سبب الإجابة المقترحة: 400 تمثل نصف البدل الكامل.

### English

- Context: The full allowance is 800 units, and the employee works half-time throughout the month.
- Existing decision: The allowance is paid strictly in proportion to working fraction; half-time receives half the full allowance.
- New decision: This employee receives an allowance of 400 units for the month.
- Proposed answer rationale: 400 is half the full allowance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0046 — records / active preservation hold

عائلة المراجعة: F037 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: ملف K عليه أمر حفظ داخلي نشط حتى إشعار الرفع، ولا يجوز اعتبار انتهاء المدة العادية رفعًا للأمر.
- القرار السابق: يُمنع إتلاف ملف عليه أمر حفظ نشط حتى صدور إشعار رفع الأمر.
- القرار الجديد: يُتلف ملف آخر M؛ حالة أمر الحفظ لهذا الملف غير متاحة.
- سبب الإجابة المقترحة: يلزم معرفة حالة الحفظ الخاصة بملف M.

### English

- Context: File K has an active internal preservation hold until a release notice; expiry of ordinary retention does not release the hold.
- Existing decision: A file under an active preservation hold must not be destroyed until a release notice is issued.
- New decision: Another file M is destroyed; its preservation-hold status is unavailable.
- Proposed answer rationale: File M's preservation-hold status is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0047 — attendance / exact start time

عائلة المراجعة: F002 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المقارنة تخص وردية واحدة للفريق B بتاريخ 2030-05-02. جميع الأوقات محلية.
- القرار السابق: تبدأ وردية الفريق B الساعة 08:00 بالضبط.
- القرار الجديد: يُعقد الاجتماع اليومي للفريق الساعة 09:00.
- سبب الإجابة المقترحة: وقت الاجتماع لا يغيّر بدء الوردية.

### English

- Context: The comparison concerns one Team B shift on 2030-05-02. All times are local.
- Existing decision: Team B's shift starts at exactly 08:00.
- New decision: The team's daily meeting is held at 09:00.
- Proposed answer rationale: The meeting time does not change the shift start.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0048 — expenses / receipt requirement

عائلة المراجعة: F021 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المطالبة تخص وجبة عمل. المستند الإلكتروني الرسمي يعد إيصالًا، وكشف البطاقة وحده لا يعد إيصالًا.
- القرار السابق: لا تُسدد مطالبة الوجبة إلا بوجود إيصال معتمد.
- القرار الجديد: تُسدد المطالبة بمرفق غير موضح النوع أو الاعتماد.
- سبب الإجابة المقترحة: يلزم معرفة هل المرفق إيصال معتمد.

### English

- Context: The claim concerns a business meal. An official electronic receipt counts as a receipt; a card statement alone does not.
- Existing decision: A meal claim must not be reimbursed without an accepted receipt.
- New decision: The claim is reimbursed with an attachment whose type and acceptance status are unspecified.
- Proposed answer rationale: It is necessary to know whether the attachment is an accepted receipt.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0049 — leave / consecutive duration

عائلة المراجعة: F007 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحد يطبق على كل فترة إجازة متصلة. الفترات المذكورة لا تتضمن انقطاعًا.
- القرار السابق: الحد الأقصى للإجازة المتصلة هو 12 يومًا تقويميًا.
- القرار الجديد: تُمنح للموظف إجازة متصلة مدتها 14 يومًا.
- سبب الإجابة المقترحة: الفترة تتجاوز حد 12 يومًا.

### English

- Context: The limit applies to each continuous leave period. The stated periods have no interruption.
- Existing decision: The maximum continuous leave period is 12 calendar days.
- New decision: The employee is granted 14 consecutive calendar days of leave.
- Proposed answer rationale: The period exceeds the 12-day limit.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0050 — recruitment / vacancy approval

عائلة المراجعة: F081 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الشاغر V1 معتمد وممول، والشاغر V2 مقترح ولم يعتمد. حالة V3 غير متاحة.
- القرار السابق: لا يُعلن توظيف إلا لشاغر معتمد وممول معًا.
- القرار الجديد: يُنشر إعلان توظيف للشاغر V1.
- سبب الإجابة المقترحة: الشاغر معتمد وممول.

### English

- Context: Vacancy V1 is approved and funded; V2 is proposed and unapproved. V3's status is unavailable.
- Existing decision: Recruitment may be advertised only for a vacancy that is both approved and funded.
- New decision: A recruitment advertisement is published for V1.
- Proposed answer rationale: The vacancy is approved and funded.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0051 — attendance / mandatory location

عائلة المراجعة: F001 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الموظفون المقصودون هم موظفو القسم A يوم 2030-04-07، ولا يوجد استثناء للعمل عن بعد.
- القرار السابق: يجب على موظفي القسم A أداء دوام ذلك اليوم كاملًا في المكتب.
- القرار الجديد: يجب على هؤلاء الموظفين أداء دوام ذلك اليوم كاملًا من المنزل.
- سبب الإجابة المقترحة: المكانان المفروضان مختلفان لنفس الدوام.

### English

- Context: The people concerned are Department A employees on 2030-04-07. No remote-work exception applies.
- Existing decision: Department A employees must work that entire day in the office.
- New decision: These employees must work that entire day from home.
- Proposed answer rationale: The required locations differ for the same shift.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0052 — procurement / quote threshold

عائلة المراجعة: F016 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: القيمة إجمالية لطلب شراء واحد. لا توجد إعفاءات من طلب عروض الأسعار.
- القرار السابق: المشتريات التي تزيد على 10000 وحدة تتطلب ثلاثة عروض أسعار على الأقل.
- القرار الجديد: يُنفذ شراء بقيمة 10000 وحدة اعتمادًا على عرضين.
- سبب الإجابة المقترحة: القاعدة تشترط أكثر من 10000، لا المساواة.

### English

- Context: The value is the total for one purchase request. No quotation exemptions apply.
- Existing decision: Purchases exceeding 10000 units require at least three quotations.
- New decision: A purchase worth 10000 units is executed using two quotations.
- Proposed answer rationale: The rule applies above 10000, not at equality.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0053 — training / delivery modality exception

عائلة المراجعة: F059 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الوحدة P عملية وتتطلب معدات فعلية، والوحدة T نظرية. نوع الوحدة X غير موثق.
- القرار السابق: تُقدم الوحدات العملية حضوريًا فقط، ويجوز تقديم الوحدات النظرية عن بعد.
- القرار الجديد: تُقدم الوحدة P كاملة عن بعد دون حضور.
- سبب الإجابة المقترحة: الوحدة عملية لكن طريقة تقديمها غير حضورية.

### English

- Context: Module P is practical and requires physical equipment; module T is theoretical. Module X's type is undocumented.
- Existing decision: Practical modules must be delivered in person only; theoretical modules may be delivered remotely.
- New decision: Module P is delivered entirely remotely without in-person attendance.
- Proposed answer rationale: The module is practical but its delivery is not in person.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0054 — expenses / per-person versus total

عائلة المراجعة: F023 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الوجبة لخمسة مشاركين، وتقسم التكلفة بالتساوي. المبالغ شاملة كل الرسوم.
- القرار السابق: الحد الأقصى لمصروف الوجبة 100 وحدة لكل مشارك.
- القرار الجديد: تُعتمد تكلفة الوجبة الإجمالية البالغة 600 وحدة.
- سبب الإجابة المقترحة: حصة الفرد 120 وحدة وتتجاوز 100.

### English

- Context: The meal is for five participants, with cost divided equally. Amounts include all charges.
- Existing decision: The meal expense cap is 100 units per participant.
- New decision: The meal's total cost of 600 units is approved.
- Proposed answer rationale: Each person's share is 120 units, exceeding 100.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0055 — communications / publication embargo

عائلة المراجعة: F061 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الإعلان A تحت حظر نشر حتى 2030-12-01 الساعة 09:00 بالتوقيت المحلي. جميع الأوقات بالتوقيت نفسه.
- القرار السابق: يُمنع نشر A للعامة قبل انتهاء حظر النشر.
- القرار الجديد: يُنشر A للعامة يوم 2030-12-01 الساعة 08:30.
- سبب الإجابة المقترحة: النشر يسبق انتهاء الحظر بنصف ساعة.

### English

- Context: Announcement A is under embargo until 2030-12-01 at 09:00 local time. All times use that same time zone.
- Existing decision: A must not be published publicly before the embargo ends.
- New decision: A is published publicly on 2030-12-01 at 08:30.
- Proposed answer rationale: Publication precedes the embargo's end by half an hour.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0056 — meetings / minutes status

عائلة المراجعة: F054 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المحضر M مسودة لم تعتمد بعد. السماح بالتداول الداخلي للمراجعة لا يعد نشرًا نهائيًا.
- القرار السابق: يُمنع نشر المحضر بوصفه نهائيًا قبل اعتماده، ويُسمح بتداوله داخليًا كمسودة للمراجعة.
- القرار الجديد: يُرسل M داخليًا بعنوان مسودة للمراجعة.
- سبب الإجابة المقترحة: التداول يطابق الاستخدام المسموح للمسودة.

### English

- Context: Minutes M are an unapproved draft. Internal circulation for review does not count as final publication.
- Existing decision: Minutes must not be published as final before approval; internal circulation as a review draft is allowed.
- New decision: M is circulated internally with the title Draft for Review.
- Proposed answer rationale: Circulation matches the permitted use of a draft.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0057 — records / version effective dates

عائلة المراجعة: F038 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الإصدار V1 ساري حتى نهاية 2030-03-31، وV2 يبدأ 2030-04-01 ويحل محله صراحة.
- القرار السابق: يجب استخدام الإصدار الساري بتاريخ المعاملة: V1 قبل أبريل وV2 من أول أبريل.
- القرار الجديد: تُعالج معاملة مؤرخة 2030-03-20 باستخدام V1.
- سبب الإجابة المقترحة: V1 كان ساريًا في التاريخ المحدد.

### English

- Context: Version V1 is effective through the end of 2030-03-31; V2 starts on 2030-04-01 and explicitly replaces it.
- Existing decision: Use the version effective on the transaction date: V1 before April and V2 from April 1.
- New decision: A transaction dated 2030-03-20 is processed using V1.
- Proposed answer rationale: V1 was effective on the specified date.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0058 — customer_service / response versus resolution

عائلة المراجعة: F066 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الرد الأول والتسوية النهائية إجراءان مختلفان. الوقت محسوب من تسجيل الشكوى.
- القرار السابق: يجب إرسال رد أول خلال أربع ساعات، وإتمام التسوية النهائية خلال خمسة أيام.
- القرار الجديد: يُرسل الرد الأول بعد ساعتين وتُنجز التسوية في اليوم الرابع.
- سبب الإجابة المقترحة: كل إجراء ضمن مهلته المستقلة.

### English

- Context: An initial response and final resolution are different actions. Time is measured from complaint registration.
- Existing decision: An initial response must be sent within four hours, and final resolution completed within five days.
- New decision: The initial response is sent after two hours and resolution is completed on day four.
- Proposed answer rationale: Each action falls within its separate deadline.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0059 — meetings / agenda notice

عائلة المراجعة: F052 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الإشعار يحسب بالساعات المتصلة قبل بدء الاجتماع، والاجتماع غير طارئ.
- القرار السابق: يجب توزيع جدول أعمال الاجتماع غير الطارئ قبل بدايته بـ48 ساعة على الأقل.
- القرار الجديد: يُوزع جدول الأعمال قبل الاجتماع بـ72 ساعة.
- سبب الإجابة المقترحة: المدة تحقق الحد الأدنى.

### English

- Context: Notice is measured in continuous hours before the meeting starts, and the meeting is not an emergency.
- Existing decision: A non-emergency meeting's agenda must be distributed at least 48 hours before it starts.
- New decision: The agenda is distributed 72 hours before the meeting.
- Proposed answer rationale: The interval meets the minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0060 — travel / report deadline

عائلة المراجعة: F015 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المقارنة تخص موعد تسليم تقرير المهمة النهائي، محسوبًا بعد العودة بالأيام التقويمية.
- القرار السابق: يجب تسليم التقرير خلال خمسة أيام بعد العودة، ويشمل ذلك اليوم الخامس.
- القرار الجديد: يُسلّم التقرير يوم 2030-07-10؛ تاريخ العودة غير محدد.
- سبب الإجابة المقترحة: يلزم تاريخ العودة لتحديد الموعد النهائي.

### English

- Context: The comparison concerns submission of the final mission report, measured in calendar days after return.
- Existing decision: The report must be submitted within five days after return, including day five.
- New decision: The report is submitted on 2030-07-10; the return date is unspecified.
- Proposed answer rationale: The return date is needed to determine the deadline.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0061 — meetings / agenda notice

عائلة المراجعة: F052 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الإشعار يحسب بالساعات المتصلة قبل بدء الاجتماع، والاجتماع غير طارئ.
- القرار السابق: يجب توزيع جدول أعمال الاجتماع غير الطارئ قبل بدايته بـ48 ساعة على الأقل.
- القرار الجديد: يُوزع جدول الأعمال قبل الاجتماع بـ24 ساعة فقط.
- سبب الإجابة المقترحة: مدة الإشعار أقل من 48 ساعة.

### English

- Context: Notice is measured in continuous hours before the meeting starts, and the meeting is not an emergency.
- Existing decision: A non-emergency meeting's agenda must be distributed at least 48 hours before it starts.
- New decision: The agenda is distributed only 24 hours before the meeting.
- Proposed answer rationale: The notice period is shorter than 48 hours.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0062 — customer_service / response versus resolution

عائلة المراجعة: F066 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الرد الأول والتسوية النهائية إجراءان مختلفان. الوقت محسوب من تسجيل الشكوى.
- القرار السابق: يجب إرسال رد أول خلال أربع ساعات، وإتمام التسوية النهائية خلال خمسة أيام.
- القرار الجديد: يؤجل الرد الأول إلى الساعة السادسة بعد التسجيل، وتُنجز التسوية في اليوم الثاني.
- سبب الإجابة المقترحة: سرعة التسوية لا تعالج تجاوز مهلة الرد الأول.

### English

- Context: An initial response and final resolution are different actions. Time is measured from complaint registration.
- Existing decision: An initial response must be sent within four hours, and final resolution completed within five days.
- New decision: The initial response is delayed until hour six after registration, and resolution occurs on day two.
- Proposed answer rationale: Prompt resolution does not cure the missed initial-response deadline.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0063 — leave / notice period

عائلة المراجعة: F006 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: مهلة الإشعار تحسب بالأيام التقويمية الكاملة قبل بدء الإجازة، ولا يوجد استثناء.
- القرار السابق: يجب تقديم طلب الإجازة قبل بدايتها بسبعة أيام على الأقل.
- القرار الجديد: تُعتمد إجازة تبدأ يوم 2030-06-20، وتاريخ تقديم الطلب غير متاح.
- سبب الإجابة المقترحة: يلزم تاريخ التقديم لحساب المهلة.

### English

- Context: Notice is counted in full calendar days before leave starts, and no exception applies.
- Existing decision: A leave request must be submitted at least seven days before the leave starts.
- New decision: Leave starting on 2030-06-20 is approved, but the request submission date is unavailable.
- Proposed answer rationale: The submission date is needed to calculate the notice period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0064 — quality / sample proportion

عائلة المراجعة: F071 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الدفعة فيها 200 قطعة. يجب تقريب أي حد أدنى كسري لعدد القطع إلى الأعلى.
- القرار السابق: يجب فحص 10% على الأقل من قطع كل دفعة قبل الإفراج عنها.
- القرار الجديد: يُفرج عن الدفعة بعد فحص 25 قطعة.
- سبب الإجابة المقترحة: عدد المفحوص يتجاوز الحد الأدنى.

### English

- Context: The batch contains 200 items. Any fractional minimum item count must be rounded upward.
- Existing decision: At least 10% of the items in each batch must be inspected before release.
- New decision: The batch is released after 25 items are inspected.
- Proposed answer rationale: The inspected count exceeds the minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0065 — inventory / safety stock

عائلة المراجعة: F076 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المخزون الحالي 60 وحدة، ولا توجد توريدات خلال الفترة المقصودة.
- القرار السابق: يجب ألا ينخفض المخزون المتبقي عن 20 وحدة.
- القرار الجديد: تُصرف 40 وحدة من المخزون الحالي فورًا.
- سبب الإجابة المقترحة: المتبقي 20 وحدة يحقق الحد.

### English

- Context: Current stock is 60 units, with no deliveries during the period concerned.
- Existing decision: Remaining stock must not fall below 20 units.
- New decision: 40 units are issued immediately from current stock.
- Proposed answer rationale: 20 units remain, meeting the limit.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0066 — recruitment / application window

عائلة المراجعة: F085 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المدة تقاس بعدد أيام تقويمية كاملة يبقى الإعلان خلالها مفتوحًا لاستقبال الطلبات.
- القرار السابق: يجب إبقاء إعلان الوظيفة مفتوحًا لمدة عشرة أيام على الأقل.
- القرار الجديد: يُغلق الإعلان بعد عشرة أيام كاملة من فتحه.
- سبب الإجابة المقترحة: الفترة تحقق الحد الأدنى بالضبط.

### English

- Context: Duration is measured in full calendar days during which the advertisement remains open for applications.
- Existing decision: A job advertisement must remain open for at least ten days.
- New decision: The advertisement closes after ten full days of being open.
- Proposed answer rationale: The period meets the minimum exactly.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0067 — expenses / submission window

عائلة المراجعة: F025 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المهلة تقاس بالأيام التقويمية المنقضية بعد تاريخ المصروف. لا توجد إعفاءات.
- القرار السابق: لا تُقبل مطالبة مقدمة بعد أكثر من 30 يومًا من تاريخ المصروف.
- القرار الجديد: تُقبل مطالبة بتاريخ تقديم معلوم، لكن تاريخ المصروف غير موجود.
- سبب الإجابة المقترحة: لا يمكن حساب المدة دون تاريخ المصروف.

### English

- Context: The window is measured in elapsed calendar days after the expense date. No exemptions apply.
- Existing decision: A claim submitted more than 30 days after the expense date must not be accepted.
- New decision: A claim with a known submission date is accepted, but the expense date is missing.
- Proposed answer rationale: The elapsed time cannot be calculated without the expense date.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0068 — recruitment / vacancy approval

عائلة المراجعة: F081 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الشاغر V1 معتمد وممول، والشاغر V2 مقترح ولم يعتمد. حالة V3 غير متاحة.
- القرار السابق: لا يُعلن توظيف إلا لشاغر معتمد وممول معًا.
- القرار الجديد: يُنشر إعلان توظيف للشاغر V2 رغم عدم اعتماده.
- سبب الإجابة المقترحة: شرط اعتماد الشاغر غير متحقق.

### English

- Context: Vacancy V1 is approved and funded; V2 is proposed and unapproved. V3's status is unavailable.
- Existing decision: Recruitment may be advertised only for a vacancy that is both approved and funded.
- New decision: A recruitment advertisement is published for V2 despite its lack of approval.
- Proposed answer rationale: The vacancy-approval condition is unmet.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0069 — communications / recommendation versus prohibition

عائلة المراجعة: F064 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: القناة A مفضلة لكنها ليست إلزامية، والقناتان A وB معتمدتان ومتاحتان لهذه الرسائل.
- القرار السابق: يُنصح باستخدام A عند الإمكان، ويظل استخدام B مسموحًا دون موافقة إضافية. يُمنع استخدام أي قناة غير معتمدة.
- القرار الجديد: يُمنع جميع الموظفين من استخدام B لهذه الرسائل منعًا مطلقًا.
- سبب الإجابة المقترحة: المنع المطلق يناقض الإذن الصريح باستخدام B.

### English

- Context: Channel A is preferred but not mandatory; channels A and B are both approved and available for these messages.
- Existing decision: Use of A is recommended when possible, while B remains allowed without additional approval. Use of any unapproved channel is prohibited.
- New decision: All employees are absolutely prohibited from using B for these messages.
- Proposed answer rationale: The absolute prohibition contradicts the explicit permission to use B.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0070 — payroll / non-cumulative alternatives

عائلة المراجعة: F088 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: البدلان A وB يغطيان الغرض نفسه، ويمكن اختيار أحدهما خلال الشهر.
- القرار السابق: يجوز صرف A أو B للموظف في الشهر، ويُمنع الجمع بينهما في الشهر نفسه.
- القرار الجديد: يُصرف للموظف A وB معًا عن شهر مارس.
- سبب الإجابة المقترحة: تم الجمع بين بدلين لا يجوز جمعهما للفترة نفسها.

### English

- Context: Allowances A and B cover the same purpose, and one may be chosen for the month.
- Existing decision: An employee may receive A or B for a month, but must not receive both for that same month.
- New decision: The employee receives both A and B for March.
- Proposed answer rationale: Two allowances that cannot be combined are paid for the same period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0071 — finance / rounding direction

عائلة المراجعة: F045 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المبلغ الناتج قبل التقريب 124.7 وحدة، ويُحوّل إلى عدد صحيح.
- القرار السابق: تُقرب مبالغ هذا النوع دائمًا إلى العدد الصحيح الأدنى.
- القرار الجديد: يُثبت المبلغ بعد التقريب بقيمة 125 وحدة.
- سبب الإجابة المقترحة: 125 نتيجة تقريب للأعلى، بينما المطلوب 124.

### English

- Context: The amount before rounding is 124.7 units, and it is converted to an integer.
- Existing decision: Amounts of this type must always be rounded down to the lower integer.
- New decision: The rounded amount is recorded as 125 units.
- Proposed answer rationale: 125 rounds upward, whereas the required result is 124.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0072 — records / original versus copy

عائلة المراجعة: F039 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الأصل الورقي والنسخة الممسوحة سجلان متميزان. إنشاء النسخة لا يلغي وجوب حفظ الأصل.
- القرار السابق: يجب حفظ العقد الورقي الأصلي، ويجوز إنشاء نسخة إلكترونية للاستخدام اليومي.
- القرار الجديد: يُتلف المستند المسمى نسخة التوقيع، دون بيان هل هو الأصل أم صورة عنه.
- سبب الإجابة المقترحة: يلزم تحديد هوية المستند بالنسبة للأصل.

### English

- Context: The paper original and scanned copy are distinct records. Creating a copy does not waive original retention.
- Existing decision: The original paper contract must be retained; an electronic copy may be created for daily use.
- New decision: The document named signature copy is destroyed, without specifying whether it is the original or a reproduction.
- Proposed answer rationale: The document's identity relative to the original is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0073 — communications / approval covers exact text

عائلة المراجعة: F063 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الموافقة الإعلامية مرتبطة بالنص الذي روجع تحديدًا. تعديل الحقائق يتطلب موافقة جديدة.
- القرار السابق: لا يُنشر بيان إعلامي إلا إذا اعتمدت نسخة النص المنشورة نفسها.
- القرار الجديد: تُنشر النسخة التي اعتُمدت دون أي تغيير في نصها.
- سبب الإجابة المقترحة: النص المنشور مطابق للنص المعتمد.

### English

- Context: Media approval covers the exact reviewed text. Changing factual content requires new approval.
- Existing decision: A media statement may be published only if the exact published text version has been approved.
- New decision: The approved version is published without any change to its text.
- Proposed answer rationale: The published text matches the approved text.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0074 — recruitment / application window

عائلة المراجعة: F085 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المدة تقاس بعدد أيام تقويمية كاملة يبقى الإعلان خلالها مفتوحًا لاستقبال الطلبات.
- القرار السابق: يجب إبقاء إعلان الوظيفة مفتوحًا لمدة عشرة أيام على الأقل.
- القرار الجديد: يُغلق الإعلان يوم 2030-02-20، وتاريخ فتحه غير متاح.
- سبب الإجابة المقترحة: يلزم تاريخ الفتح لحساب مدة استقبال الطلبات.

### English

- Context: Duration is measured in full calendar days during which the advertisement remains open for applications.
- Existing decision: A job advertisement must remain open for at least ten days.
- New decision: The advertisement closes on 2030-02-20, and its opening date is unavailable.
- Proposed answer rationale: The opening date is needed to calculate the application period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0075 — finance / budget balance

عائلة المراجعة: F041 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المتبقي المتاح في بند الصيانة 7000 وحدة، ولا يسمح بتحويل مبالغ إليه ضمن هذه الحالات.
- القرار السابق: يُمنع اعتماد التزامات مالية تتجاوز الرصيد المتاح للبند.
- القرار الجديد: يُعتمد التزام صيانة من البند دون تحديد قيمته.
- سبب الإجابة المقترحة: يلزم مقدار الالتزام لمقارنته بالرصيد.

### English

- Context: The maintenance budget has 7000 units available, and no transfers into it are permitted in these cases.
- Existing decision: Financial commitments exceeding the budget line's available balance must not be approved.
- New decision: A maintenance commitment is approved against the line without specifying its amount.
- Proposed answer rationale: The commitment amount is needed for comparison with the balance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0076 — leave / notice period

عائلة المراجعة: F006 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: مهلة الإشعار تحسب بالأيام التقويمية الكاملة قبل بدء الإجازة، ولا يوجد استثناء.
- القرار السابق: يجب تقديم طلب الإجازة قبل بدايتها بسبعة أيام على الأقل.
- القرار الجديد: تُعتمد إجازة تبدأ بعد عشرة أيام من تقديم طلبها.
- سبب الإجابة المقترحة: المهلة أطول من الحد الأدنى المطلوب.

### English

- Context: Notice is counted in full calendar days before leave starts, and no exception applies.
- Existing decision: A leave request must be submitted at least seven days before the leave starts.
- New decision: Leave starting ten days after its request is submitted is approved.
- Proposed answer rationale: The notice exceeds the required minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0077 — finance / rounding direction

عائلة المراجعة: F045 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المبلغ الناتج قبل التقريب 124.7 وحدة، ويُحوّل إلى عدد صحيح.
- القرار السابق: تُقرب مبالغ هذا النوع دائمًا إلى العدد الصحيح الأدنى.
- القرار الجديد: يُثبت المبلغ بعد التقريب بقيمة 124 وحدة.
- سبب الإجابة المقترحة: القيمة هي العدد الصحيح الأدنى.

### English

- Context: The amount before rounding is 124.7 units, and it is converted to an integer.
- Existing decision: Amounts of this type must always be rounded down to the lower integer.
- New decision: The rounded amount is recorded as 124 units.
- Proposed answer rationale: The value is the lower integer.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0078 — travel / inclusive lodging cap

عائلة المراجعة: F012 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المبالغ لكل ليلة وبالعملة نفسها. الحد يشمل الضريبة وجميع الرسوم الإلزامية.
- القرار السابق: لا تتجاوز تكلفة السكن 500 وحدة لليلة.
- القرار الجديد: يُحجز سكن بسعر 480 وحدة، وتضاف ضريبة إلزامية قدرها 40 وحدة لليلة.
- سبب الإجابة المقترحة: المجموع 520 ويتجاوز 500.

### English

- Context: Amounts are per night and in the same currency. The cap includes tax and all mandatory fees.
- Existing decision: Accommodation must cost no more than 500 units per night.
- New decision: Accommodation is booked at 480 units plus a mandatory tax of 40 units per night.
- Proposed answer rationale: The total is 520, exceeding 500.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0079 — customer_service / required notification channel

عائلة المراجعة: F070 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: يُقصد بالإشعار رسالة تصل إلى العميل؛ نشر تحديث داخل ملف الموظف ليس إشعارًا للعميل.
- القرار السابق: يجب إشعار العميل بالإلغاء قبل تنفيذ الإلغاء.
- القرار الجديد: يُنفذ الإلغاء بعد وصول رسالة الإلغاء إلى العميل.
- سبب الإجابة المقترحة: الإشعار سبق التنفيذ.

### English

- Context: A notification means a message delivered to the customer; an update inside the staff case file is not a customer notification.
- Existing decision: The customer must be notified of cancellation before cancellation is executed.
- New decision: Cancellation is executed after the cancellation message reaches the customer.
- Proposed answer rationale: Notification preceded execution.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0080 — recruitment / conflict of interest recusal

عائلة المراجعة: F083 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: عضو اللجنة M قريب للمرشح A وفق تعريف القرابة المعتمد. العضو N ليس قريبًا له.
- القرار السابق: يجب امتناع عضو لجنة التوظيف عن تقييم أي مرشح تربطه به القرابة المحددة.
- القرار الجديد: يتولى العضو X تقييم A، وعلاقته بالمرشح غير معروفة.
- سبب الإجابة المقترحة: يلزم تحديد علاقة X بالمرشح.

### English

- Context: Panel member M is related to candidate A under the adopted relationship definition. Member N is not related to A.
- Existing decision: A hiring-panel member must abstain from evaluating a candidate with the specified family relationship.
- New decision: Member X evaluates A, and their relationship to the candidate is unknown.
- Proposed answer rationale: X's relationship to the candidate is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0081 — it_access / environment scope

عائلة المراجعة: F030 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: بيئة الإنتاج P وبيئة الاختبار T منفصلتان بالكامل، ولا تنسخ تعديلات T إلى P تلقائيًا.
- القرار السابق: خلال فترة الإقفال يُمنع تعديل إعدادات الإنتاج P.
- القرار الجديد: تُعدّل إعدادات الخادم X خلال الإقفال، وبيئته غير محددة.
- سبب الإجابة المقترحة: يلزم تحديد هل الخادم إنتاجي أم اختباري.

### English

- Context: Production environment P and test environment T are completely separate; changes in T are not automatically copied to P.
- Existing decision: During the closing period, configuration changes in production P are prohibited.
- New decision: Server X's configuration is changed during closing, and its environment is unspecified.
- Proposed answer rationale: It is necessary to determine whether the server is production or test.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0082 — meetings / peer departments

عائلة المراجعة: F055 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: القسمان A وB مستقلان في تنظيم اجتماعاتهما. لا موظفين أو قاعات مشتركة في الاجتماعات المذكورة.
- القرار السابق: يُعقد اجتماع القسم A الأسبوعي يوم الاثنين فقط.
- القرار الجديد: يُنقل اجتماع A الأسبوعي نفسه إلى الثلاثاء فقط.
- سبب الإجابة المقترحة: القراران يحددان يومين حصريين للاجتماع نفسه.

### English

- Context: Departments A and B organize their meetings independently. The stated meetings share neither employees nor rooms.
- Existing decision: Department A's weekly meeting is held only on Monday.
- New decision: That same weekly meeting of A is moved to Tuesday only.
- Proposed answer rationale: The decisions prescribe different exclusive days for the same meeting.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0083 — finance / cash custody

عائلة المراجعة: F042 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الخزنة A معتمدة للنقد، والخزانة المكتبية B غير معتمدة. المكان X غير موصوف.
- القرار السابق: يجب حفظ النقد المتبقي ليلًا داخل خزنة معتمدة.
- القرار الجديد: يُحفظ النقد ليلًا في المكان X.
- سبب الإجابة المقترحة: يلزم تحديد طبيعة X واعتماده.

### English

- Context: Safe A is approved for cash, while office cabinet B is not. Location X is undescribed.
- Existing decision: Cash remaining overnight must be kept in an approved safe.
- New decision: Cash is kept overnight in location X.
- Proposed answer rationale: X's nature and approval status are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0084 — communications / publication embargo

عائلة المراجعة: F061 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الإعلان A تحت حظر نشر حتى 2030-12-01 الساعة 09:00 بالتوقيت المحلي. جميع الأوقات بالتوقيت نفسه.
- القرار السابق: يُمنع نشر A للعامة قبل انتهاء حظر النشر.
- القرار الجديد: يُنشر A للعامة يوم 2030-12-01 دون تحديد الساعة.
- سبب الإجابة المقترحة: قد يقع النشر قبل 09:00 أو بعدها.

### English

- Context: Announcement A is under embargo until 2030-12-01 at 09:00 local time. All times use that same time zone.
- Existing decision: A must not be published publicly before the embargo ends.
- New decision: A is published publicly on 2030-12-01 without specifying the time.
- Proposed answer rationale: Publication could occur before or after 09:00.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0085 — travel / restricted destination

عائلة المراجعة: F013 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المنطقة R محظورة للسفر الوظيفي، والمنطقة S غير محظورة. الرحلات كلها وظيفية.
- القرار السابق: يُمنع تكليف الموظفين بمهمات داخل المنطقة R.
- القرار الجديد: يُكلف الموظف بمهمة في مدينة L، والمنطقة التابعة لها غير معروفة.
- سبب الإجابة المقترحة: يلزم موقع المدينة بالنسبة للمنطقة R.

### English

- Context: Region R is restricted for business travel, and Region S is not restricted. All trips are business trips.
- Existing decision: Employees must not be assigned missions inside Region R.
- New decision: The employee is assigned a mission in City L, whose region is unknown.
- Proposed answer rationale: The city's location relative to Region R is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0086 — it_access / access expiry

عائلة المراجعة: F027 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: تنتهي مهمة المتعاقد في نهاية 2030-08-31. الأوقات المذكورة بتوقيت الموقع نفسه.
- القرار السابق: يجب تعطيل وصول المتعاقد فور انتهاء مهمته، ولا يجوز إبقاؤه نشطًا بعدها.
- القرار الجديد: يُعطل الوصول في نهاية 2030-08-31.
- سبب الإجابة المقترحة: التعطيل متزامن مع انتهاء المهمة.

### English

- Context: The contractor's assignment ends at the end of 2030-08-31. All stated times use the same site time zone.
- Existing decision: Contractor access must be disabled when the assignment ends and must not remain active afterwards.
- New decision: Access is disabled at the end of 2030-08-31.
- Proposed answer rationale: Disabling access coincides with the assignment end.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0087 — expenses / receipt requirement

عائلة المراجعة: F021 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المطالبة تخص وجبة عمل. المستند الإلكتروني الرسمي يعد إيصالًا، وكشف البطاقة وحده لا يعد إيصالًا.
- القرار السابق: لا تُسدد مطالبة الوجبة إلا بوجود إيصال معتمد.
- القرار الجديد: تُسدد المطالبة بكشف البطاقة فقط، ولا يوجد إيصال.
- سبب الإجابة المقترحة: المستند الوحيد لا يحقق شرط الإيصال.

### English

- Context: The claim concerns a business meal. An official electronic receipt counts as a receipt; a card statement alone does not.
- Existing decision: A meal claim must not be reimbursed without an accepted receipt.
- New decision: The claim is reimbursed using only a card statement, with no receipt.
- Proposed answer rationale: The only document does not meet the receipt requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0088 — quality / independent audit

عائلة المراجعة: F072 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المدقق A شارك في تنفيذ العملية، والمدقق B لم يشارك فيها بأي دور تنفيذي.
- القرار السابق: لا يتولى التدقيق النهائي للعملية شخص شارك في تنفيذها.
- القرار الجديد: يُعيّن C مدققًا نهائيًا دون بيان دوره السابق في العملية.
- سبب الإجابة المقترحة: يلزم معرفة هل شارك C في التنفيذ.

### English

- Context: Auditor A participated in executing the process; auditor B had no execution role in it.
- Existing decision: Final process auditing must not be performed by someone who participated in its execution.
- New decision: C is appointed final auditor without describing any prior role in the process.
- Proposed answer rationale: It is necessary to know whether C participated in execution.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0089 — information_security / external sharing

عائلة المراجعة: F032 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: تصنيف الوثيقة D سري داخلي. المكتب E خارج المنظمة، والموظف F عضو داخلي مخول بالاطلاع.
- القرار السابق: يُمنع إرسال الوثائق السرية الداخلية إلى أي مستلم خارج المنظمة.
- القرار الجديد: تُرسل D إلى المستلم G، ولا تُعرف جهة انتسابه.
- سبب الإجابة المقترحة: يلزم تحديد هل G داخل المنظمة أم خارجها.

### English

- Context: Document D is classified as internal confidential. Office E is outside the organization, while employee F is an internal member authorized to view it.
- Existing decision: Internal confidential documents must not be sent to any recipient outside the organization.
- New decision: D is sent to recipient G, whose organizational affiliation is unknown.
- Proposed answer rationale: It is necessary to determine whether G is inside or outside the organization.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0090 — procurement / quote threshold

عائلة المراجعة: F016 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: القيمة إجمالية لطلب شراء واحد. لا توجد إعفاءات من طلب عروض الأسعار.
- القرار السابق: المشتريات التي تزيد على 10000 وحدة تتطلب ثلاثة عروض أسعار على الأقل.
- القرار الجديد: يُنفذ الشراء بعرضين فقط، وقيمته الإجمالية غير مذكورة.
- سبب الإجابة المقترحة: يلزم إجمالي القيمة لمعرفة انطباق العتبة.

### English

- Context: The value is the total for one purchase request. No quotation exemptions apply.
- Existing decision: Purchases exceeding 10000 units require at least three quotations.
- New decision: The purchase is executed using only two quotations, and its total value is unspecified.
- Proposed answer rationale: The total value is needed to determine whether the threshold applies.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0091 — training / certificate validity

عائلة المراجعة: F057 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: تاريخ انتهاء الشهادة مشمول بصلاحيتها. يلزم أن تكون صالحة طوال تشغيل الجهاز.
- القرار السابق: لا يُكلف موظف بتشغيل الجهاز دون شهادة صالحة وقت التشغيل.
- القرار الجديد: يشغل الموظف الجهاز يوم 2030-10-31 بشهادة تنتهي بنهاية ذلك اليوم.
- سبب الإجابة المقترحة: التشغيل يقع ضمن مدة الصلاحية.

### English

- Context: The certificate's expiry date is included in its validity. It must remain valid throughout equipment operation.
- Existing decision: An employee must not be assigned to operate the equipment without a certificate valid at the time of operation.
- New decision: The employee operates the equipment on 2030-10-31 with a certificate valid through that day's end.
- Proposed answer rationale: Operation falls within the validity period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0092 — records / destruction witnesses

عائلة المراجعة: F040 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: إتلاف السجلات يتطلب حضور شهود فعليين، وتوقيع غائب لا يعد حضورًا.
- القرار السابق: يجب حضور شاهدين على الأقل عند إتلاف السجلات.
- القرار الجديد: يتم الإتلاف بحضور ثلاثة شهود.
- سبب الإجابة المقترحة: عدد الحاضرين يحقق الحد الأدنى.

### English

- Context: Record destruction requires witnesses to be physically present; an absent person's signature does not count as attendance.
- Existing decision: At least two witnesses must be present during record destruction.
- New decision: Destruction occurs with three witnesses present.
- Proposed answer rationale: The number present meets the minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0093 — attendance / mandatory location

عائلة المراجعة: F001 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الموظفون المقصودون هم موظفو القسم A يوم 2030-04-07، ولا يوجد استثناء للعمل عن بعد.
- القرار السابق: يجب على موظفي القسم A أداء دوام ذلك اليوم كاملًا في المكتب.
- القرار الجديد: يبدأ اجتماع هؤلاء الموظفين في المكتب الساعة 10:00 من ذلك اليوم.
- سبب الإجابة المقترحة: الاجتماع في المكتب ينسجم مع الحضور الإلزامي.

### English

- Context: The people concerned are Department A employees on 2030-04-07. No remote-work exception applies.
- Existing decision: Department A employees must work that entire day in the office.
- New decision: These employees' office meeting starts at 10:00 that day.
- Proposed answer rationale: An office meeting is compatible with mandatory office attendance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0094 — leave / handover condition

عائلة المراجعة: F008 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الموظفة S مسؤولة مناوبة. بدء الإجازة لا يلغي شرط التسليم.
- القرار السابق: لا تبدأ إجازة مسؤول المناوبة قبل قبول البديل لمحضر التسليم.
- القرار الجديد: تبدأ إجازة S اليوم، ويقبل البديل المحضر غدًا.
- سبب الإجابة المقترحة: الإجازة تبدأ قبل قبول التسليم.

### English

- Context: Employee S is an on-call lead. Starting leave does not waive the handover requirement.
- Existing decision: An on-call lead's leave must not start before the replacement accepts the handover record.
- New decision: S's leave starts today, and the replacement will accept the record tomorrow.
- Proposed answer rationale: Leave starts before handover acceptance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0095 — logistics / delivery identity

عائلة المراجعة: F091 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المستلم المعين للشحنة هو A. تسليم الشحنة لشخص آخر يتطلب تفويضًا مكتوبًا من A.
- القرار السابق: لا تُسلم الشحنة إلا إلى A أو شخص يحمل تفويضًا مكتوبًا منه.
- القرار الجديد: تُسلم الشحنة إلى B بعد تقديم تفويض مكتوب صحيح من A.
- سبب الإجابة المقترحة: المستلم البديل يحقق شرط التفويض.

### English

- Context: The shipment's designated recipient is A. Delivery to another person requires written authorization from A.
- Existing decision: The shipment may be delivered only to A or a person carrying written authorization from A.
- New decision: The shipment is delivered to B after valid written authorization from A is presented.
- Proposed answer rationale: The alternative recipient satisfies the authorization condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0096 — training / prerequisite completion

عائلة المراجعة: F056 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الدورة المتقدمة T تتطلب إكمال الأساسيات. التسجيل في الأساسيات وحده لا يعد إكمالًا.
- القرار السابق: لا يبدأ الموظف الدورة T قبل إكمال دورة الأساسيات.
- القرار الجديد: يبدأ الموظف T وهو مسجل في الأساسيات ولم يكملها.
- سبب الإجابة المقترحة: الشرط السابق لم يكتمل.

### English

- Context: Advanced course T requires completion of the basics. Merely enrolling in the basics does not count as completion.
- Existing decision: An employee must not start course T before completing the basics course.
- New decision: The employee starts T while enrolled in the basics but without completing them.
- Proposed answer rationale: The prerequisite has not been completed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0097 — leave / handover condition

عائلة المراجعة: F008 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الموظفة S مسؤولة مناوبة. بدء الإجازة لا يلغي شرط التسليم.
- القرار السابق: لا تبدأ إجازة مسؤول المناوبة قبل قبول البديل لمحضر التسليم.
- القرار الجديد: تبدأ إجازة S اليوم بعدما قبل البديل المحضر أمس.
- سبب الإجابة المقترحة: قبول التسليم سبق بدء الإجازة.

### English

- Context: Employee S is an on-call lead. Starting leave does not waive the handover requirement.
- Existing decision: An on-call lead's leave must not start before the replacement accepts the handover record.
- New decision: S's leave starts today after the replacement accepted the record yesterday.
- Proposed answer rationale: Handover acceptance preceded the start of leave.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0098 — records / active preservation hold

عائلة المراجعة: F037 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: ملف K عليه أمر حفظ داخلي نشط حتى إشعار الرفع، ولا يجوز اعتبار انتهاء المدة العادية رفعًا للأمر.
- القرار السابق: يُمنع إتلاف ملف عليه أمر حفظ نشط حتى صدور إشعار رفع الأمر.
- القرار الجديد: يُؤجل إتلاف K حتى صدور إشعار رفع أمر الحفظ.
- سبب الإجابة المقترحة: الإتلاف معلق حتى انتهاء المنع.

### English

- Context: File K has an active internal preservation hold until a release notice; expiry of ordinary retention does not release the hold.
- Existing decision: A file under an active preservation hold must not be destroyed until a release notice is issued.
- New decision: Destruction of K is deferred until a hold-release notice is issued.
- Proposed answer rationale: Destruction is deferred until the prohibition ends.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0099 — attendance / break threshold

عائلة المراجعة: F005 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الوردية متصلة، والاستراحة المقصودة مدتها 30 دقيقة.
- القرار السابق: إذا تجاوزت الوردية ست ساعات، يجب منح استراحة؛ الوردية التي لا تتجاوز ست ساعات لا يشملها هذا الشرط.
- القرار الجديد: يعمل الفريق ست ساعات بالضبط دون استراحة.
- سبب الإجابة المقترحة: الحد مشروط بتجاوز ست ساعات، لا بلوغها فقط.

### English

- Context: The shift is continuous, and the break in question lasts 30 minutes.
- Existing decision: If a shift exceeds six hours, a break must be given; shifts of six hours or less are outside this requirement.
- New decision: The team works exactly six hours without a break.
- Proposed answer rationale: The threshold requires exceeding six hours, not merely reaching it.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0100 — travel / inclusive lodging cap

عائلة المراجعة: F012 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المبالغ لكل ليلة وبالعملة نفسها. الحد يشمل الضريبة وجميع الرسوم الإلزامية.
- القرار السابق: لا تتجاوز تكلفة السكن 500 وحدة لليلة.
- القرار الجديد: يُحجز سكن بسعر إجمالي شامل قدره 500 وحدة لليلة.
- سبب الإجابة المقترحة: التكلفة الشاملة لا تتجاوز الحد.

### English

- Context: Amounts are per night and in the same currency. The cap includes tax and all mandatory fees.
- Existing decision: Accommodation must cost no more than 500 units per night.
- New decision: Accommodation is booked at an all-inclusive total of 500 units per night.
- Proposed answer rationale: The all-inclusive cost does not exceed the cap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0101 — it_access / access expiry

عائلة المراجعة: F027 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: تنتهي مهمة المتعاقد في نهاية 2030-08-31. الأوقات المذكورة بتوقيت الموقع نفسه.
- القرار السابق: يجب تعطيل وصول المتعاقد فور انتهاء مهمته، ولا يجوز إبقاؤه نشطًا بعدها.
- القرار الجديد: يُعطل الوصول فور إنجاز التسليم النهائي؛ موعد التسليم غير معلوم.
- سبب الإجابة المقترحة: يلزم موعد التسليم لمعرفة استمرار الوصول بعد نهاية المهمة.

### English

- Context: The contractor's assignment ends at the end of 2030-08-31. All stated times use the same site time zone.
- Existing decision: Contractor access must be disabled when the assignment ends and must not remain active afterwards.
- New decision: Access is disabled upon final handover completion; the handover time is unknown.
- Proposed answer rationale: The handover time is needed to determine whether access persists after the assignment ends.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0102 — communications / bilingual simultaneous release

عائلة المراجعة: F062 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الإعلان رسمي، والمطلوب نسختان عربـية وإنجليزية كاملتان. الملخص لا يعد نسخة كاملة.
- القرار السابق: يجب نشر النسختين العربية والإنجليزية من كل إعلان رسمي في الوقت نفسه.
- القرار الجديد: تُنشر النسخة الإنجليزية اليوم، وتُنشر النسخة العربية غدًا.
- سبب الإجابة المقترحة: النشر في يومين مختلفين لا يحقق التزامن.

### English

- Context: The announcement is official, and full Arabic and English versions are required. A summary is not a full version.
- Existing decision: The Arabic and English versions of every official announcement must be published at the same time.
- New decision: The English version is published today, and the Arabic version tomorrow.
- Proposed answer rationale: Publication on different days does not satisfy simultaneity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0103 — recruitment / conflict of interest recusal

عائلة المراجعة: F083 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: عضو اللجنة M قريب للمرشح A وفق تعريف القرابة المعتمد. العضو N ليس قريبًا له.
- القرار السابق: يجب امتناع عضو لجنة التوظيف عن تقييم أي مرشح تربطه به القرابة المحددة.
- القرار الجديد: يمتنع M عن تقييم A ويتولى N التقييم.
- سبب الإجابة المقترحة: العضو المعني امتنع وحل محله شخص غير قريب.

### English

- Context: Panel member M is related to candidate A under the adopted relationship definition. Member N is not related to A.
- Existing decision: A hiring-panel member must abstain from evaluating a candidate with the specified family relationship.
- New decision: M abstains from evaluating A, and N performs the evaluation.
- Proposed answer rationale: The affected member abstains and is replaced by an unrelated person.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0104 — customer_service / required notification channel

عائلة المراجعة: F070 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: يُقصد بالإشعار رسالة تصل إلى العميل؛ نشر تحديث داخل ملف الموظف ليس إشعارًا للعميل.
- القرار السابق: يجب إشعار العميل بالإلغاء قبل تنفيذ الإلغاء.
- القرار الجديد: يُنفذ الإلغاء بعد تحديث الحالة إلى مُبلّغ، دون معرفة هل وصلت رسالة للعميل.
- سبب الإجابة المقترحة: اسم الحالة لا يكفي لإثبات وصول الإشعار.

### English

- Context: A notification means a message delivered to the customer; an update inside the staff case file is not a customer notification.
- Existing decision: The customer must be notified of cancellation before cancellation is executed.
- New decision: Cancellation is executed after the status becomes Notified, without knowing whether a message reached the customer.
- Proposed answer rationale: The status name is insufficient to establish delivery of notification.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0105 — records / minimum retention

عائلة المراجعة: F036 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: العمر محسوب من تاريخ إقفال الملف. لا توجد التزامات احتفاظ إضافية.
- القرار السابق: يجب الاحتفاظ بالسجل خمس سنوات على الأقل بعد إقفاله.
- القرار الجديد: يُحتفظ بالسجل ست سنوات بعد إقفاله.
- سبب الإجابة المقترحة: الاحتفاظ يتجاوز الحد الأدنى ولا يخالفه.

### English

- Context: Age is measured from the file closure date. No additional retention obligations apply.
- Existing decision: A record must be retained for at least five years after closure.
- New decision: The record is retained for six years after closure.
- Proposed answer rationale: Retention exceeds the minimum without violating it.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0106 — logistics / route approval specific scope

عائلة المراجعة: F095 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الطريق A معتمد للشاحنات الثقيلة فقط، والطريق B معتمد للمركبات الخفيفة فقط.
- القرار السابق: يجب أن تسلك كل مركبة الطريق المعتمد لفئتها فقط.
- القرار الجديد: تسلك المركبة V الطريق B، وفئتها غير محددة.
- سبب الإجابة المقترحة: يلزم تحديد فئة V.

### English

- Context: Route A is approved only for heavy trucks; route B is approved only for light vehicles.
- Existing decision: Each vehicle must use only the route approved for its category.
- New decision: Vehicle V uses route B, and its category is unspecified.
- Proposed answer rationale: V's category must be identified.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0107 — it_access / environment scope

عائلة المراجعة: F030 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: بيئة الإنتاج P وبيئة الاختبار T منفصلتان بالكامل، ولا تنسخ تعديلات T إلى P تلقائيًا.
- القرار السابق: خلال فترة الإقفال يُمنع تعديل إعدادات الإنتاج P.
- القرار الجديد: تُعدّل إعدادات P خلال فترة الإقفال.
- سبب الإجابة المقترحة: التغيير يقع في البيئة والفترة المحظورتين.

### English

- Context: Production environment P and test environment T are completely separate; changes in T are not automatically copied to P.
- Existing decision: During the closing period, configuration changes in production P are prohibited.
- New decision: P's configuration is changed during the closing period.
- Proposed answer rationale: The change occurs in the prohibited environment and period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0108 — inventory / asset traceability

عائلة المراجعة: F079 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: جميع الأجهزة في هذه الحالة أصول مرقمة. التسجيل يجب أن يربط رقم الجهاز بمستلمه.
- القرار السابق: لا يُسلم جهاز إلا بعد تسجيل رقمه التسلسلي واسم مستلمه معًا.
- القرار الجديد: يُسلم الجهاز بعد قراءة رمزه الشريطي، دون معرفة البيانات المسجلة أو ربط المستلم.
- سبب الإجابة المقترحة: المسح وحده لا يثبت تسجيل الحقلين وربطهما.

### English

- Context: All devices in this case are numbered assets. Registration must link the device number to its recipient.
- Existing decision: A device must not be handed over until both its serial number and recipient's name are recorded.
- New decision: The device is handed over after scanning its barcode, without knowing the recorded data or recipient linkage.
- Proposed answer rationale: Scanning alone does not establish that both fields are recorded and linked.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0109 — inventory / first-expiring first-out

عائلة المراجعة: F078 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: دفعتا A وB من الصنف نفسه ومتاحتان وصالحتان للصرف في المواعيد المقصودة. تنتهي A في يناير وB في مارس من السنة نفسها.
- القرار السابق: يجب صرف الدفعة الأقرب انتهاءً أولًا ما دامت متاحة وصالحة.
- القرار الجديد: تُصرف دفعة C قبل A، وتاريخ انتهاء C غير مذكور.
- سبب الإجابة المقترحة: يلزم تاريخ انتهاء C لتحديد ترتيب الأولوية.

### English

- Context: Batches A and B contain the same item and are available and valid for issue at the relevant times. A expires in January and B in March of the same year.
- Existing decision: The earliest-expiring batch must be issued first while it is available and valid.
- New decision: Batch C is issued before A, and C's expiry date is unspecified.
- Proposed answer rationale: C's expiry date is needed to determine priority order.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0110 — meetings / peer departments

عائلة المراجعة: F055 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: القسمان A وB مستقلان في تنظيم اجتماعاتهما. لا موظفين أو قاعات مشتركة في الاجتماعات المذكورة.
- القرار السابق: يُعقد اجتماع القسم A الأسبوعي يوم الاثنين فقط.
- القرار الجديد: يُعقد اجتماع القسم الأسبوعي يوم الثلاثاء دون تسمية القسم.
- سبب الإجابة المقترحة: يلزم تحديد القسم لمعرفة هل القرار يخص اجتماع A.

### English

- Context: Departments A and B organize their meetings independently. The stated meetings share neither employees nor rooms.
- Existing decision: Department A's weekly meeting is held only on Monday.
- New decision: The department's weekly meeting is held on Tuesday without naming the department.
- Proposed answer rationale: The department must be identified to determine whether A's meeting is affected.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0111 — facilities / maintenance closure

عائلة المراجعة: F048 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المبنى N مغلق كامل يوم 2030-10-15. المبنى M مفتوح ومستقل عنه.
- القرار السابق: يُمنع عقد أي اجتماع حضوري داخل N أثناء إغلاقه.
- القرار الجديد: يُعقد الاجتماع داخل M ظهر 2030-10-15.
- سبب الإجابة المقترحة: المبنى الآخر خارج نطاق الإغلاق.

### English

- Context: Building N is closed throughout 2030-10-15. Building M is open and separate.
- Existing decision: No in-person meeting may be held inside N while it is closed.
- New decision: The meeting is held inside M at noon on 2030-10-15.
- Proposed answer rationale: The other building is outside the closure scope.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0112 — finance / payment prerequisites AND

عائلة المراجعة: F043 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المستندان المطلوبان مستقلان: فاتورة معتمدة ومحضر استلام موقع.
- القرار السابق: لا يُصرف مبلغ المورد إلا بعد توفر الفاتورة المعتمدة ومحضر الاستلام الموقع معًا.
- القرار الجديد: يُصرف المبلغ بعد توفر المستندين المطلوبين.
- سبب الإجابة المقترحة: الشرطان متحققان قبل الصرف.

### English

- Context: The two required documents are independent: an approved invoice and a signed receipt-of-goods record.
- Existing decision: The supplier must not be paid until both the approved invoice and signed receipt-of-goods record are available.
- New decision: Payment is made after both required documents are available.
- Proposed answer rationale: Both conditions are satisfied before payment.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0113 — travel / fare class

عائلة المراجعة: F011 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الرحلة عملية مدتها أربع ساعات، ولا تنطبق عليها استثناءات الدرجة.
- القرار السابق: الرحلات التي تقل عن ست ساعات تُحجز بالدرجة الاقتصادية فقط.
- القرار الجديد: تُحجز الرحلة المذكورة بالدرجة الاقتصادية مع مقعد قرب النافذة.
- سبب الإجابة المقترحة: اختيار المقعد لا يغيّر الدرجة المطلوبة.

### English

- Context: The business flight lasts four hours, and no fare-class exceptions apply.
- Existing decision: Flights shorter than six hours must be booked in economy class only.
- New decision: The stated flight is booked in economy class with a window seat.
- Proposed answer rationale: The seat choice does not change the required fare class.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0114 — meetings / minutes status

عائلة المراجعة: F054 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المحضر M مسودة لم تعتمد بعد. السماح بالتداول الداخلي للمراجعة لا يعد نشرًا نهائيًا.
- القرار السابق: يُمنع نشر المحضر بوصفه نهائيًا قبل اعتماده، ويُسمح بتداوله داخليًا كمسودة للمراجعة.
- القرار الجديد: يُعمم M الآن دون تحديد المستلمين أو هل يقدم كمسودة أم نسخة نهائية.
- سبب الإجابة المقترحة: يلزم تحديد طبيعة التعميم ووضع النسخة.

### English

- Context: Minutes M are an unapproved draft. Internal circulation for review does not count as final publication.
- Existing decision: Minutes must not be published as final before approval; internal circulation as a review draft is allowed.
- New decision: M is circulated now without identifying recipients or whether it is presented as a draft or final version.
- Proposed answer rationale: The nature of circulation and version status are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0115 — records / version effective dates

عائلة المراجعة: F038 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الإصدار V1 ساري حتى نهاية 2030-03-31، وV2 يبدأ 2030-04-01 ويحل محله صراحة.
- القرار السابق: يجب استخدام الإصدار الساري بتاريخ المعاملة: V1 قبل أبريل وV2 من أول أبريل.
- القرار الجديد: تُعالج معاملة مؤرخة 2030-04-05 باستخدام V1.
- سبب الإجابة المقترحة: V1 انتهى قبل تاريخ المعاملة.

### English

- Context: Version V1 is effective through the end of 2030-03-31; V2 starts on 2030-04-01 and explicitly replaces it.
- Existing decision: Use the version effective on the transaction date: V1 before April and V2 from April 1.
- New decision: A transaction dated 2030-04-05 is processed using V1.
- Proposed answer rationale: V1 expired before the transaction date.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0116 — finance / cash custody

عائلة المراجعة: F042 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الخزنة A معتمدة للنقد، والخزانة المكتبية B غير معتمدة. المكان X غير موصوف.
- القرار السابق: يجب حفظ النقد المتبقي ليلًا داخل خزنة معتمدة.
- القرار الجديد: يُحفظ النقد ليلًا في الخزنة A.
- سبب الإجابة المقترحة: مكان الحفظ يحقق الشرط.

### English

- Context: Safe A is approved for cash, while office cabinet B is not. Location X is undescribed.
- Existing decision: Cash remaining overnight must be kept in an approved safe.
- New decision: Cash is kept overnight in safe A.
- Proposed answer rationale: The storage location meets the requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0117 — travel / inclusive lodging cap

عائلة المراجعة: F012 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المبالغ لكل ليلة وبالعملة نفسها. الحد يشمل الضريبة وجميع الرسوم الإلزامية.
- القرار السابق: لا تتجاوز تكلفة السكن 500 وحدة لليلة.
- القرار الجديد: يُحجز سكن بسعر 480 وحدة قبل الضريبة، وقيمة الضريبة غير مذكورة.
- سبب الإجابة المقترحة: قد تجعل الضريبة الإجمالي أعلى من الحد أو ضمنه.

### English

- Context: Amounts are per night and in the same currency. The cap includes tax and all mandatory fees.
- Existing decision: Accommodation must cost no more than 500 units per night.
- New decision: Accommodation is booked at 480 units before tax, whose amount is unspecified.
- Proposed answer rationale: Tax could put the total above the cap or leave it within it.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0118 — procurement / separation of duties

عائلة المراجعة: F020 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: كل رمز موظف يشير إلى شخص مختلف. لا توجد استثناءات لفصل المهام.
- القرار السابق: يجب أن يكون معتمد طلب الشراء شخصًا غير منشئ الطلب.
- القرار الجديد: يعتمد E2 الطلب، ولا تُذكر هوية منشئه.
- سبب الإجابة المقترحة: يلزم تحديد المنشئ للتحقق من اختلاف الشخصين.

### English

- Context: Each employee identifier denotes a different person. There are no separation-of-duties exceptions.
- Existing decision: The purchase request approver must be someone other than its creator.
- New decision: E2 approves the request, and its creator is not identified.
- Proposed answer rationale: The creator's identity is needed to check that the two people differ.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0119 — customer_service / refund eligibility OR

عائلة المراجعة: F068 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحالة مستوفية لشروط الاسترداد الأخرى. العيب المثبت والتسليم الخاطئ سببان بديلان.
- القرار السابق: يحق للعميل الاسترداد عند وجود عيب مثبت أو تسليم صنف خاطئ؛ وفي غير ذلك يُرفض الاسترداد.
- القرار الجديد: يُرفض الاسترداد لصنف معيب مثبت العيب فقط لأنه ليس صنفًا خاطئًا.
- سبب الإجابة المقترحة: أحد السببين يكفي، ولا يلزم اجتماعهما.

### English

- Context: The case satisfies the other refund conditions. A confirmed defect and wrong delivery are alternative qualifying reasons.
- Existing decision: A customer is entitled to a refund for either a confirmed defect or delivery of the wrong item; otherwise a refund is denied.
- New decision: A refund for an item with a confirmed defect is denied solely because the item was not wrongly delivered.
- Proposed answer rationale: Either reason is sufficient; both are not required.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0120 — it_access / authentication alternatives

عائلة المراجعة: F028 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: كل الحسابات المقصودة حسابات إدارية حساسة. كلمة المرور وحدها عامل واحد.
- القرار السابق: يجب استخدام عاملين مستقلين على الأقل عند كل دخول إلى حساب إداري.
- القرار الجديد: يُسمح بالدخول إلى الحساب الإداري بكلمة المرور وحدها.
- سبب الإجابة المقترحة: عامل واحد أقل من العاملين المطلوبين.

### English

- Context: All accounts concerned are sensitive administrator accounts. A password alone is one factor.
- Existing decision: At least two independent factors must be used for every administrator-account login.
- New decision: Logging into the administrator account with only a password is permitted.
- Proposed answer rationale: One factor is fewer than the two required.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0121 — procurement / emergency exemption

عائلة المراجعة: F019 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المراجعة العادية تتطلب مناقصة. الإعفاء الوحيد هو إعلان طوارئ رسمي لهذه المشتريات.
- القرار السابق: تُجرى مناقصة قبل الشراء، ويجوز الشراء المباشر عند وجود إعلان الطوارئ المحدد.
- القرار الجديد: يُنفذ شراء مباشر دون مناقصة، مع التأكيد بعدم وجود إعلان طوارئ.
- سبب الإجابة المقترحة: تم تجاوز المناقصة دون تحقق الإعفاء.

### English

- Context: Ordinary review requires a tender. The only exemption is an official emergency declaration covering these purchases.
- Existing decision: A tender must precede the purchase; direct purchasing is allowed when the specified emergency declaration exists.
- New decision: A direct purchase is executed without a tender, with confirmation that no emergency declaration exists.
- Proposed answer rationale: The tender is bypassed without the exemption being satisfied.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0122 — attendance / exact start time

عائلة المراجعة: F002 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المقارنة تخص وردية واحدة للفريق B بتاريخ 2030-05-02. جميع الأوقات محلية.
- القرار السابق: تبدأ وردية الفريق B الساعة 08:00 بالضبط.
- القرار الجديد: تبدأ الوردية نفسها عند افتتاح المبنى؛ وقت الافتتاح غير متاح.
- سبب الإجابة المقترحة: يلزم وقت افتتاح المبنى للمقارنة مع 08:00.

### English

- Context: The comparison concerns one Team B shift on 2030-05-02. All times are local.
- Existing decision: Team B's shift starts at exactly 08:00.
- New decision: The same shift starts when the building opens; the opening time is unavailable.
- Proposed answer rationale: The building opening time is needed for comparison with 08:00.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0123 — training / minimum annual hours

عائلة المراجعة: F058 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: السنة التدريبية تنتهي بعد تنفيذ القرار، ولا توجد أنشطة تدريبية أخرى هذا العام.
- القرار السابق: يجب أن يكمل كل موظف 20 ساعة تدريب على الأقل خلال السنة.
- القرار الجديد: تُقفل الخطة السنوية للموظف عند إجمالي نهائي قدره 24 ساعة.
- سبب الإجابة المقترحة: الإجمالي يحقق الحد المطلوب.

### English

- Context: The training year ends after the decision is carried out, and there are no other training activities this year.
- Existing decision: Every employee must complete at least 20 training hours during the year.
- New decision: The employee's annual plan is closed with a final total of 24 hours.
- Proposed answer rationale: The total meets the required minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0124 — procurement / split orders

عائلة المراجعة: F017 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحد هو 8000 وحدة للحاجة الواحدة. الغرض من التقسيم مذكور صراحة عند توفره.
- القرار السابق: يُمنع تقسيم حاجة شرائية واحدة إلى طلبات أصغر بهدف تجاوز مراجعة الحد المالي.
- القرار الجديد: يُنفذ طلبان بقيمة 6000 لكل منهما دون بيان هل يمثلان حاجة واحدة أو سبب الفصل.
- سبب الإجابة المقترحة: يلزم معرفة علاقة الطلبين والغرض من الفصل.

### English

- Context: The threshold is 8000 units per purchasing need. The purpose of splitting is stated explicitly when available.
- Existing decision: A single purchasing need must not be split into smaller orders to bypass the financial-threshold review.
- New decision: Two orders of 6000 each are executed without stating whether they serve one need or why they are separate.
- Proposed answer rationale: The relationship between the orders and the purpose of separation are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0125 — it_access / environment scope

عائلة المراجعة: F030 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: بيئة الإنتاج P وبيئة الاختبار T منفصلتان بالكامل، ولا تنسخ تعديلات T إلى P تلقائيًا.
- القرار السابق: خلال فترة الإقفال يُمنع تعديل إعدادات الإنتاج P.
- القرار الجديد: تُعدّل إعدادات T فقط خلال فترة الإقفال.
- سبب الإجابة المقترحة: بيئة الاختبار خارج نطاق الحظر المحدد.

### English

- Context: Production environment P and test environment T are completely separate; changes in T are not automatically copied to P.
- Existing decision: During the closing period, configuration changes in production P are prohibited.
- New decision: Only T's configuration is changed during the closing period.
- Proposed answer rationale: The test environment is outside the stated prohibition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0126 — payroll / non-cumulative alternatives

عائلة المراجعة: F088 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: البدلان A وB يغطيان الغرض نفسه، ويمكن اختيار أحدهما خلال الشهر.
- القرار السابق: يجوز صرف A أو B للموظف في الشهر، ويُمنع الجمع بينهما في الشهر نفسه.
- القرار الجديد: يُصرف A وB للموظف، دون تحديد الشهر الذي يغطيه كل بدل.
- سبب الإجابة المقترحة: يلزم تحديد فترتي الاستحقاق لمعرفة التداخل.

### English

- Context: Allowances A and B cover the same purpose, and one may be chosen for the month.
- Existing decision: An employee may receive A or B for a month, but must not receive both for that same month.
- New decision: A and B are paid to the employee without identifying the month each covers.
- Proposed answer rationale: Both entitlement periods are needed to determine overlap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0127 — recruitment / recognized equivalence

عائلة المراجعة: F082 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: لأغراض هذه الوظيفة فقط، الشهادة B معادلة صراحة للشهادة A، والشهادة C ليست معادلة لها.
- القرار السابق: يجب امتلاك الشهادة A أو ما يعادلها المعتمد للتعيين في الوظيفة.
- القرار الجديد: يُعيّن مرشح لا يملك سوى الشهادة B.
- سبب الإجابة المقترحة: المعادلة الصريحة تحقق شرط المؤهل.

### English

- Context: For this position only, certificate B is explicitly equivalent to A, while certificate C is not equivalent.
- Existing decision: Appointment to the position requires certificate A or an approved equivalent.
- New decision: A candidate holding only certificate B is appointed.
- Proposed answer rationale: Explicit equivalence satisfies the qualification requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0128 — attendance / break threshold

عائلة المراجعة: F005 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الوردية متصلة، والاستراحة المقصودة مدتها 30 دقيقة.
- القرار السابق: إذا تجاوزت الوردية ست ساعات، يجب منح استراحة؛ الوردية التي لا تتجاوز ست ساعات لا يشملها هذا الشرط.
- القرار الجديد: يعمل الفريق سبع ساعات متصلة دون استراحة.
- سبب الإجابة المقترحة: المدة تتجاوز ست ساعات مع حذف الاستراحة المطلوبة.

### English

- Context: The shift is continuous, and the break in question lasts 30 minutes.
- Existing decision: If a shift exceeds six hours, a break must be given; shifts of six hours or less are outside this requirement.
- New decision: The team works seven continuous hours without a break.
- Proposed answer rationale: The duration exceeds six hours while omitting the required break.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0129 — travel / advance settlement

عائلة المراجعة: F014 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: السلفة السابقة A تخص الموظف نفسه، والسلفة الجديدة B طلب منفصل.
- القرار السابق: لا تُصرف سلفة سفر جديدة قبل إقفال السلفة السابقة محاسبيًا.
- القرار الجديد: تُصرف B اليوم بعد إقفال A محاسبيًا أمس.
- سبب الإجابة المقترحة: الإقفال سبق الصرف الجديد.

### English

- Context: Previous advance A belongs to the same employee, and new advance B is a separate request.
- Existing decision: A new travel advance must not be paid before the previous advance is closed in the accounts.
- New decision: B is paid today after A was closed in the accounts yesterday.
- Proposed answer rationale: Closure preceded the new payment.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0130 — expenses / duplicate reimbursement

عائلة المراجعة: F022 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الفاتورة I7 صُرفت بالكامل سابقًا. الفاتورة I8 لم تُصرف من قبل.
- القرار السابق: يُمنع سداد المصروف نفسه أكثر من مرة.
- القرار الجديد: تُسدد فاتورة بلا رقم، ولم يُتحقق من سبق صرفها.
- سبب الإجابة المقترحة: هوية المصروف وسجل سداده غير كافيين للحكم.

### English

- Context: Invoice I7 has already been reimbursed in full. Invoice I8 has never been reimbursed.
- Existing decision: The same expense must not be reimbursed more than once.
- New decision: An unnumbered invoice is reimbursed, and prior payment has not been checked.
- Proposed answer rationale: The expense identity and payment history are insufficient to decide.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0131 — attendance / weekly ceiling

عائلة المراجعة: F003 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: جميع الساعات المذكورة ساعات عمل فعلية لنفس الموظف في الأسبوع نفسه.
- القرار السابق: لا يجوز أن يتجاوز عمل الموظف 40 ساعة في الأسبوع.
- القرار الجديد: يُكلف الموظف بالعمل 43 ساعة هذا الأسبوع.
- سبب الإجابة المقترحة: 43 تتجاوز الحد الأقصى 40.

### English

- Context: All stated hours are actual working hours for the same employee in the same week.
- Existing decision: The employee must not work more than 40 hours per week.
- New decision: The employee is assigned 43 working hours this week.
- Proposed answer rationale: 43 exceeds the maximum of 40.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0132 — it_access / authentication alternatives

عائلة المراجعة: F028 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: كل الحسابات المقصودة حسابات إدارية حساسة. كلمة المرور وحدها عامل واحد.
- القرار السابق: يجب استخدام عاملين مستقلين على الأقل عند كل دخول إلى حساب إداري.
- القرار الجديد: يتطلب الدخول كلمة مرور ومفتاح أمان مادي مستقلًا.
- سبب الإجابة المقترحة: الدخول يستلزم عاملين مستقلين.

### English

- Context: All accounts concerned are sensitive administrator accounts. A password alone is one factor.
- Existing decision: At least two independent factors must be used for every administrator-account login.
- New decision: Login requires a password and an independent physical security key.
- Proposed answer rationale: Login requires two independent factors.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0133 — expenses / submission window

عائلة المراجعة: F025 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المهلة تقاس بالأيام التقويمية المنقضية بعد تاريخ المصروف. لا توجد إعفاءات.
- القرار السابق: لا تُقبل مطالبة مقدمة بعد أكثر من 30 يومًا من تاريخ المصروف.
- القرار الجديد: تُقبل مطالبة قُدمت بعد 35 يومًا من المصروف.
- سبب الإجابة المقترحة: مدة التقديم تجاوزت 30 يومًا.

### English

- Context: The window is measured in elapsed calendar days after the expense date. No exemptions apply.
- Existing decision: A claim submitted more than 30 days after the expense date must not be accepted.
- New decision: A claim submitted 35 days after the expense is accepted.
- Proposed answer rationale: Submission occurred more than 30 days later.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0134 — procurement / quote threshold

عائلة المراجعة: F016 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: القيمة إجمالية لطلب شراء واحد. لا توجد إعفاءات من طلب عروض الأسعار.
- القرار السابق: المشتريات التي تزيد على 10000 وحدة تتطلب ثلاثة عروض أسعار على الأقل.
- القرار الجديد: يُنفذ شراء بقيمة 12000 وحدة اعتمادًا على عرضين فقط.
- سبب الإجابة المقترحة: الطلب تجاوز العتبة وعدد العروض أقل من ثلاثة.

### English

- Context: The value is the total for one purchase request. No quotation exemptions apply.
- Existing decision: Purchases exceeding 10000 units require at least three quotations.
- New decision: A purchase worth 12000 units is executed using only two quotations.
- Proposed answer rationale: The purchase exceeds the threshold and has fewer than three quotations.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0135 — projects / two independent limits

عائلة المراجعة: F098 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الزيادة تقاس مقابل الميزانية الأساسية 100000 وحدة. التأخير يقاس بالأيام التقويمية.
- القرار السابق: يُسمح بالتغيير فقط إذا لم يزد التكلفة بأكثر من 5% ولم يؤخر الموعد بأكثر من ثلاثة أيام.
- القرار الجديد: يُعتمد تغيير يزيد التكلفة 5000 وحدة ويؤخر الموعد ثلاثة أيام.
- سبب الإجابة المقترحة: الشرطان عند حديهما المسموحين.

### English

- Context: The increase is measured against a base budget of 100000 units. Delay is measured in calendar days.
- Existing decision: A change is allowed only if it increases cost by no more than 5% and delays the deadline by no more than three days.
- New decision: A change adding 5000 units and delaying the deadline by three days is approved.
- Proposed answer rationale: Both conditions are at their allowed limits.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0136 — quality / all versus most

عائلة المراجعة: F073 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: يوجد عشرة عيوب حرجة في الإصدار. إغلاق العيب يعني التحقق من إصلاحه.
- القرار السابق: لا يُطلق الإصدار إلا بعد إغلاق جميع العيوب الحرجة.
- القرار الجديد: يُطلق الإصدار بعد إغلاق العيوب العشرة والتحقق من إصلاحها.
- سبب الإجابة المقترحة: جميع العيوب الحرجة مغلقة.

### English

- Context: The release has ten critical defects. Closing a defect means its repair has been verified.
- Existing decision: The release must not be launched until all critical defects are closed.
- New decision: The release is launched after all ten defects are closed and their repairs verified.
- Proposed answer rationale: All critical defects are closed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0137 — recruitment / anonymous screening stage

عائلة المراجعة: F084 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الفرز الأولي يسبق المقابلات. أسماء المرشحين محجوبة في الفرز ومسموحة للمقابلين عند المقابلة.
- القرار السابق: تُحجب أسماء المرشحين عن المقيمين أثناء الفرز الأولي فقط.
- القرار الجديد: تُعرض الأسماء على المقيمين أثناء الفرز الأولي.
- سبب الإجابة المقترحة: الكشف يحدث في المرحلة التي يجب فيها الحجب.

### English

- Context: Initial screening precedes interviews. Candidate names are hidden during screening and available to interviewers at interview time.
- Existing decision: Candidate names must be hidden from assessors during initial screening only.
- New decision: Names are shown to assessors during initial screening.
- Proposed answer rationale: Disclosure occurs during the stage requiring anonymity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0138 — payroll / allowance effective interval

عائلة المراجعة: F086 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: البدل الشهري كان 300 وحدة حتى نهاية يونيو، وأصبح 400 من أول يوليو بقرار إحلال صريح. لا يطبق بأثر رجعي.
- القرار السابق: يُحسب بدل يونيو بـ300 وحدة وبدل يوليو بـ400 وحدة للموظف نفسه.
- القرار الجديد: يُحسب بدل يونيو بـ400 وحدة استنادًا إلى قرار يوليو دون استثناء رجعي.
- سبب الإجابة المقترحة: القيمة الجديدة لا تسري على يونيو.

### English

- Context: The monthly allowance was 300 units through June and becomes 400 from July 1 under an explicit replacement decision. It is not retroactive.
- Existing decision: The same employee's June allowance is 300 units and July allowance is 400 units.
- New decision: June's allowance is calculated as 400 units using July's decision without a retroactive exception.
- Proposed answer rationale: The new amount does not apply to June.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0139 — communications / recipient classification

عائلة المراجعة: F065 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: النشرة الفنية للمجموعة T فقط. الموظفة U ضمن T، والموظف V خارج T.
- القرار السابق: تُوزع النشرة الفنية على أعضاء T فقط.
- القرار الجديد: تُرسل النشرة إلى U.
- سبب الإجابة المقترحة: المستلمة ضمن المجموعة المحددة.

### English

- Context: The technical bulletin is for group T only. Employee U belongs to T, and employee V is outside T.
- Existing decision: The technical bulletin must be distributed only to members of T.
- New decision: The bulletin is sent to U.
- Proposed answer rationale: The recipient belongs to the specified group.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0140 — quality / independent audit

عائلة المراجعة: F072 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المدقق A شارك في تنفيذ العملية، والمدقق B لم يشارك فيها بأي دور تنفيذي.
- القرار السابق: لا يتولى التدقيق النهائي للعملية شخص شارك في تنفيذها.
- القرار الجديد: يُعيّن A مدققًا نهائيًا لهذه العملية.
- سبب الإجابة المقترحة: المدقق شارك في تنفيذ العملية.

### English

- Context: Auditor A participated in executing the process; auditor B had no execution role in it.
- Existing decision: Final process auditing must not be performed by someone who participated in its execution.
- New decision: A is appointed final auditor for this process.
- Proposed answer rationale: The auditor participated in executing the process.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0141 — quality / sample proportion

عائلة المراجعة: F071 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الدفعة فيها 200 قطعة. يجب تقريب أي حد أدنى كسري لعدد القطع إلى الأعلى.
- القرار السابق: يجب فحص 10% على الأقل من قطع كل دفعة قبل الإفراج عنها.
- القرار الجديد: يُفرج عن الدفعة بعد فحص 15 قطعة فقط.
- سبب الإجابة المقترحة: الحد الأدنى 20 قطعة ولم يتحقق.

### English

- Context: The batch contains 200 items. Any fractional minimum item count must be rounded upward.
- Existing decision: At least 10% of the items in each batch must be inspected before release.
- New decision: The batch is released after only 15 items are inspected.
- Proposed answer rationale: The minimum is 20 items and has not been met.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0142 — payroll / allowance effective interval

عائلة المراجعة: F086 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: البدل الشهري كان 300 وحدة حتى نهاية يونيو، وأصبح 400 من أول يوليو بقرار إحلال صريح. لا يطبق بأثر رجعي.
- القرار السابق: يُحسب بدل يونيو بـ300 وحدة وبدل يوليو بـ400 وحدة للموظف نفسه.
- القرار الجديد: يُحسب البدل بـ400 وحدة، والشهر الذي يخصه غير محدد.
- سبب الإجابة المقترحة: يلزم تحديد شهر الاستحقاق.

### English

- Context: The monthly allowance was 300 units through June and becomes 400 from July 1 under an explicit replacement decision. It is not retroactive.
- Existing decision: The same employee's June allowance is 300 units and July allowance is 400 units.
- New decision: The allowance is calculated as 400 units, and the month it concerns is unspecified.
- Proposed answer rationale: The entitlement month must be identified.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0143 — projects / aggregate staff allocation

عائلة المراجعة: F099 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الموظف E متاح 30 ساعة للمشاريع خلال الأسبوع، ولا يسمح بتجاوز هذه الطاقة.
- القرار السابق: يجب ألا يتجاوز مجموع ساعات تكليف E في جميع المشاريع 30 ساعة لهذا الأسبوع.
- القرار الجديد: يُكلف E بعشرين ساعة في المشروع A وخمس عشرة ساعة في B خلال الأسبوع نفسه.
- سبب الإجابة المقترحة: المجموع 35 ساعة ويتجاوز الطاقة 30.

### English

- Context: Employee E has 30 hours available for projects during the week, and this capacity must not be exceeded.
- Existing decision: E's total assigned hours across all projects must not exceed 30 this week.
- New decision: E is assigned twenty hours to project A and fifteen to B in the same week.
- Proposed answer rationale: The total is 35 hours, exceeding the capacity of 30.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0144 — information_security / public redaction

عائلة المراجعة: F035 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: أسماء الأفراد وأرقام هوياتهم بيانات شخصية. أرقام الإحصاءات المجمعة هنا لا تعرّف أفرادًا.
- القرار السابق: يجب إزالة جميع البيانات الشخصية قبل نشر التقرير للعامة.
- القرار الجديد: يُنشر تقرير يحتوي إحصاءات مجمعة فقط ولا يتضمن أي بيانات شخصية.
- سبب الإجابة المقترحة: المحتوى المنشور خالٍ من البيانات الشخصية.

### English

- Context: Individuals' names and identity numbers are personal data. The aggregate statistics here do not identify individuals.
- Existing decision: All personal data must be removed before publishing the report publicly.
- New decision: A report containing only aggregate statistics and no personal data is published.
- Proposed answer rationale: The published content contains no personal data.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0145 — finance / rounding direction

عائلة المراجعة: F045 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المبلغ الناتج قبل التقريب 124.7 وحدة، ويُحوّل إلى عدد صحيح.
- القرار السابق: تُقرب مبالغ هذا النوع دائمًا إلى العدد الصحيح الأدنى.
- القرار الجديد: يُثبت المبلغ باستخدام إعداد التقريب الافتراضي، دون تحديد نتيجته أو طريقته.
- سبب الإجابة المقترحة: يلزم معرفة نتيجة الإعداد أو قاعدة التقريب فيه.

### English

- Context: The amount before rounding is 124.7 units, and it is converted to an integer.
- Existing decision: Amounts of this type must always be rounded down to the lower integer.
- New decision: The amount is recorded using the default rounding setting, without specifying its method or result.
- Proposed answer rationale: The setting's result or rounding rule is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0146 — travel / advance settlement

عائلة المراجعة: F014 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: السلفة السابقة A تخص الموظف نفسه، والسلفة الجديدة B طلب منفصل.
- القرار السابق: لا تُصرف سلفة سفر جديدة قبل إقفال السلفة السابقة محاسبيًا.
- القرار الجديد: تُصرف B اليوم مع بقاء A مفتوحة محاسبيًا.
- سبب الإجابة المقترحة: السلفة السابقة لم تُقفل قبل الصرف.

### English

- Context: Previous advance A belongs to the same employee, and new advance B is a separate request.
- Existing decision: A new travel advance must not be paid before the previous advance is closed in the accounts.
- New decision: B is paid today while A remains open in the accounts.
- Proposed answer rationale: The previous advance was not closed before payment.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0147 — logistics / segregated storage

عائلة المراجعة: F094 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الفئتان X وY يجب فصلهما إداريًا لمنع خلط الجرد، دون افتراض خطر مادي.
- القرار السابق: يُمنع وضع أصناف X وY داخل الحاوية نفسها.
- القرار الجديد: توضع X وY في المنطقة L دون بيان توزيع الحاويات داخلها.
- سبب الإجابة المقترحة: يلزم تحديد هل الحاويات مشتركة أم منفصلة.

### English

- Context: Categories X and Y must be separated administratively to prevent inventory mix-ups; no physical hazard is assumed.
- Existing decision: Items from X and Y must not be placed in the same container.
- New decision: X and Y are placed in area L without describing their container allocation within it.
- Proposed answer rationale: It is necessary to determine whether the containers are shared or separate.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0148 — facilities / temperature interval

عائلة المراجعة: F049 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المقارنة تخص نقطة ضبط حرارة غرفة الخوادم نفسها، بالدرجة المئوية.
- القرار السابق: يجب أن تكون نقطة ضبط الحرارة بين 18 و24 درجة شاملًا الطرفين.
- القرار الجديد: تُثبت نقطة الضبط على 26 درجة.
- سبب الإجابة المقترحة: 26 خارج المجال المسموح.

### English

- Context: The comparison concerns the temperature setpoint of the same server room, in degrees Celsius.
- Existing decision: The temperature setpoint must be between 18 and 24 degrees, inclusive.
- New decision: The setpoint is fixed at 26 degrees.
- Proposed answer rationale: 26 is outside the allowed interval.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0149 — logistics / vehicle allocation overlap

عائلة المراجعة: F093 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المركبة V واحدة، والمهمتان تتطلبانها طوال مدتيهما. فترات الاستخدام تستثني وقت النهاية.
- القرار السابق: تُخصص V حصريًا للمهمة A من 13:00 إلى 15:00 في اليوم المحدد.
- القرار الجديد: تُخصص V للمهمة B من 14:00 إلى 16:00 في اليوم نفسه.
- سبب الإجابة المقترحة: المركبة الواحدة مطلوبة لمهمتين متداخلتين.

### English

- Context: There is one vehicle V, and both missions require it throughout their durations. Usage intervals exclude their end time.
- Existing decision: V is allocated exclusively to mission A from 13:00 to 15:00 on the specified day.
- New decision: V is allocated to mission B from 14:00 to 16:00 on the same day.
- Proposed answer rationale: The single vehicle is required for two overlapping missions.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0150 — attendance / break threshold

عائلة المراجعة: F005 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الوردية متصلة، والاستراحة المقصودة مدتها 30 دقيقة.
- القرار السابق: إذا تجاوزت الوردية ست ساعات، يجب منح استراحة؛ الوردية التي لا تتجاوز ست ساعات لا يشملها هذا الشرط.
- القرار الجديد: يعمل الفريق وردية دون استراحة، ولم تحدد مدة الوردية.
- سبب الإجابة المقترحة: تحديد وجوب الاستراحة يتطلب مدة الوردية.

### English

- Context: The shift is continuous, and the break in question lasts 30 minutes.
- Existing decision: If a shift exceeds six hours, a break must be given; shifts of six hours or less are outside this requirement.
- New decision: The team works a shift without a break, and its duration is unspecified.
- Proposed answer rationale: The shift duration is needed to determine whether a break is required.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0151 — information_security / storage encryption

عائلة المراجعة: F031 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الملف يحتوي بيانات موظفين سرية. تشفير النقل وحده لا يشفر الملف المخزن.
- القرار السابق: يجب تشفير الملفات السرية عند تخزينها.
- القرار الجديد: يُخزن الملف في مخزن يفرض تشفير البيانات عند التخزين.
- سبب الإجابة المقترحة: طريقة التخزين تحقق الشرط.

### English

- Context: The file contains confidential employee data. Transport encryption alone does not encrypt the stored file.
- Existing decision: Confidential files must be encrypted at rest.
- New decision: The file is stored in a repository that enforces encryption at rest.
- Proposed answer rationale: The storage method meets the requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0152 — travel / report deadline

عائلة المراجعة: F015 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المقارنة تخص موعد تسليم تقرير المهمة النهائي، محسوبًا بعد العودة بالأيام التقويمية.
- القرار السابق: يجب تسليم التقرير خلال خمسة أيام بعد العودة، ويشمل ذلك اليوم الخامس.
- القرار الجديد: يُسلّم التقرير في اليوم السابع بعد العودة فقط.
- سبب الإجابة المقترحة: اليوم السابع خارج الموعد النهائي.

### English

- Context: The comparison concerns submission of the final mission report, measured in calendar days after return.
- Existing decision: The report must be submitted within five days after return, including day five.
- New decision: The report is submitted only on the seventh day after return.
- Proposed answer rationale: Day seven is beyond the deadline.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0153 — it_access / shared identity

عائلة المراجعة: F029 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: منصة العمليات تتطلب حساب مستخدم لكل شخص، ولا توجد حسابات مشتركة مستثناة.
- القرار السابق: يُمنع استخدام حساب مستخدم واحد بواسطة أكثر من موظف.
- القرار الجديد: يستخدم الفريق حساب العمليات، دون بيان هل هو اسم نظام أم هوية دخول مشتركة.
- سبب الإجابة المقترحة: وصف الحساب لا يكفي لتحديد مشاركة الهوية.

### English

- Context: The operations platform requires a user account for each person, with no exempt shared accounts.
- Existing decision: More than one employee must not use the same user account.
- New decision: The team uses the operations account, without clarifying whether this is a system name or a shared login identity.
- Proposed answer rationale: The account description is insufficient to determine identity sharing.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0154 — information_security / public redaction

عائلة المراجعة: F035 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: أسماء الأفراد وأرقام هوياتهم بيانات شخصية. أرقام الإحصاءات المجمعة هنا لا تعرّف أفرادًا.
- القرار السابق: يجب إزالة جميع البيانات الشخصية قبل نشر التقرير للعامة.
- القرار الجديد: يُنشر التقرير بعد إزالة الأسماء؛ وجود أي بيانات شخصية أخرى غير معلوم.
- سبب الإجابة المقترحة: إزالة الأسماء وحدها لا تثبت إزالة جميع البيانات الشخصية.

### English

- Context: Individuals' names and identity numbers are personal data. The aggregate statistics here do not identify individuals.
- Existing decision: All personal data must be removed before publishing the report publicly.
- New decision: The report is published after names are removed; whether other personal data remain is unknown.
- Proposed answer rationale: Removing names alone does not establish removal of all personal data.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0155 — records / minimum retention

عائلة المراجعة: F036 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: العمر محسوب من تاريخ إقفال الملف. لا توجد التزامات احتفاظ إضافية.
- القرار السابق: يجب الاحتفاظ بالسجل خمس سنوات على الأقل بعد إقفاله.
- القرار الجديد: يُتلف السجل هذا الشهر، وتاريخ إقفاله غير معروف.
- سبب الإجابة المقترحة: يلزم تاريخ الإقفال لتحديد عمر السجل.

### English

- Context: Age is measured from the file closure date. No additional retention obligations apply.
- Existing decision: A record must be retained for at least five years after closure.
- New decision: The record is destroyed this month, and its closure date is unknown.
- Proposed answer rationale: The closure date is needed to determine the record's age.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0156 — leave / notice period

عائلة المراجعة: F006 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: مهلة الإشعار تحسب بالأيام التقويمية الكاملة قبل بدء الإجازة، ولا يوجد استثناء.
- القرار السابق: يجب تقديم طلب الإجازة قبل بدايتها بسبعة أيام على الأقل.
- القرار الجديد: تُعتمد إجازة تبدأ بعد ثلاثة أيام من تقديم طلبها.
- سبب الإجابة المقترحة: ثلاثة أيام أقل من مهلة السبعة أيام.

### English

- Context: Notice is counted in full calendar days before leave starts, and no exception applies.
- Existing decision: A leave request must be submitted at least seven days before the leave starts.
- New decision: Leave starting three days after its request is submitted is approved.
- Proposed answer rationale: Three days is shorter than the seven-day notice period.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0157 — travel / restricted destination

عائلة المراجعة: F013 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المنطقة R محظورة للسفر الوظيفي، والمنطقة S غير محظورة. الرحلات كلها وظيفية.
- القرار السابق: يُمنع تكليف الموظفين بمهمات داخل المنطقة R.
- القرار الجديد: يُكلف الموظف بمهمة داخل المنطقة S فقط.
- سبب الإجابة المقترحة: النطاق الجغرافي للمهمة خارج الحظر.

### English

- Context: Region R is restricted for business travel, and Region S is not restricted. All trips are business trips.
- Existing decision: Employees must not be assigned missions inside Region R.
- New decision: The employee is assigned a mission only inside Region S.
- Proposed answer rationale: The mission's geographical scope is outside the restriction.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0158 — projects / explicit authority does not erase conflict

عائلة المراجعة: F100 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: كلا المصدرين مخول بإصدار توجيهات للمشروع P. التوجيه الجديد صادر من جهة أعلى، لكنه لا يتضمن إلغاءً أو استثناءً للتوجيه الساري. نقيّم تعارض المتطلبات، لا أولوية التنفيذ.
- القرار السابق: يجب على المشروع P الاحتفاظ بسجلات الاختبار حتى إقفاله، ويُمنع حذفها قبل الإقفال. هذا التوجيه لا يفرض الاحتفاظ بعد الإقفال.
- القرار الجديد: تأمر الجهة الأعلى بحذف سجلات اختبار P الآن، وحالة إقفال المشروع غير متاحة.
- سبب الإجابة المقترحة: يلزم معرفة هل شرط ما قبل الإقفال لا يزال ساريًا.

### English

- Context: Both issuers are authorized to direct project P. The new directive comes from a higher authority but contains no repeal or exception to the effective directive. Assess requirement conflict, not implementation priority.
- Existing decision: Project P must retain its test records until closure, and deletion before closure is prohibited. This directive imposes no retention requirement after closure.
- New decision: The higher authority orders P's test records deleted now, and the project's closure status is unavailable.
- Proposed answer rationale: It is necessary to know whether the pre-closure condition still applies.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0159 — attendance / prior approval

عائلة المراجعة: F004 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الموظف R سيؤدي ساعتين إضافيتين مساء اليوم. لا توجد استثناءات من شرط الموافقة.
- القرار السابق: لا يبدأ العمل الإضافي إلا بعد تسجيل موافقة المدير.
- القرار الجديد: يبدأ R العمل الإضافي الآن، وتسجل الموافقة غدًا.
- سبب الإجابة المقترحة: الموافقة اللاحقة لا تحقق شرط الموافقة السابقة.

### English

- Context: Employee R will work two overtime hours this evening. There are no exceptions to the approval requirement.
- Existing decision: Overtime must not start until the manager's approval is recorded.
- New decision: R starts overtime now, and approval will be recorded tomorrow.
- Proposed answer rationale: Later approval does not satisfy the prior-approval requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0160 — information_security / external sharing

عائلة المراجعة: F032 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: تصنيف الوثيقة D سري داخلي. المكتب E خارج المنظمة، والموظف F عضو داخلي مخول بالاطلاع.
- القرار السابق: يُمنع إرسال الوثائق السرية الداخلية إلى أي مستلم خارج المنظمة.
- القرار الجديد: تُرسل D إلى الموظف F عبر قناة داخلية.
- سبب الإجابة المقترحة: المستلم داخلي مخول، فلا ينطبق حظر الإرسال الخارجي.

### English

- Context: Document D is classified as internal confidential. Office E is outside the organization, while employee F is an internal member authorized to view it.
- Existing decision: Internal confidential documents must not be sent to any recipient outside the organization.
- New decision: D is sent to employee F through an internal channel.
- Proposed answer rationale: The recipient is authorized and internal, so the external-sharing prohibition does not apply.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0161 — inventory / first-expiring first-out

عائلة المراجعة: F078 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: دفعتا A وB من الصنف نفسه ومتاحتان وصالحتان للصرف في المواعيد المقصودة. تنتهي A في يناير وB في مارس من السنة نفسها.
- القرار السابق: يجب صرف الدفعة الأقرب انتهاءً أولًا ما دامت متاحة وصالحة.
- القرار الجديد: تُصرف A أولًا ثم B بعد نفاد A.
- سبب الإجابة المقترحة: الترتيب يتبع تواريخ الانتهاء.

### English

- Context: Batches A and B contain the same item and are available and valid for issue at the relevant times. A expires in January and B in March of the same year.
- Existing decision: The earliest-expiring batch must be issued first while it is available and valid.
- New decision: A is issued first, followed by B after A is exhausted.
- Proposed answer rationale: The order follows expiry dates.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0162 — logistics / unit conversion

عائلة المراجعة: F092 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: كل صندوق يحتوي 12 وحدة. أمر التسليم يتطلب كمية محددة دون زيادة أو نقص.
- القرار السابق: يجب تسليم 120 وحدة بالضبط للعميل.
- القرار الجديد: يُغلق أمر التسليم بعد تسليم منصة كاملة، وعدد الصناديق عليها غير مذكور.
- سبب الإجابة المقترحة: يلزم عدد الصناديق على المنصة لحساب الوحدات.

### English

- Context: Each box contains 12 units. The delivery order requires an exact quantity with no excess or shortage.
- Existing decision: Exactly 120 units must be delivered to the customer.
- New decision: The delivery order is closed after a full pallet is delivered, and its box count is unspecified.
- Proposed answer rationale: The pallet's box count is needed to calculate units.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0163 — communications / approval covers exact text

عائلة المراجعة: F063 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الموافقة الإعلامية مرتبطة بالنص الذي روجع تحديدًا. تعديل الحقائق يتطلب موافقة جديدة.
- القرار السابق: لا يُنشر بيان إعلامي إلا إذا اعتمدت نسخة النص المنشورة نفسها.
- القرار الجديد: تُنشر النسخة المسماة Final2، ولا يُعرف هل هي النسخة المعتمدة.
- سبب الإجابة المقترحة: اسم الملف لا يثبت تطابقه مع النسخة المعتمدة.

### English

- Context: Media approval covers the exact reviewed text. Changing factual content requires new approval.
- Existing decision: A media statement may be published only if the exact published text version has been approved.
- New decision: The version named Final2 is published, and it is unknown whether it is the approved version.
- Proposed answer rationale: The filename does not establish a match with the approved version.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0164 — payroll / bank detail change confirmation

عائلة المراجعة: F090 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: التأكيد المستقل اتصال موثق بالموظف باستخدام رقم معروف سابقًا. رسالة طلب التغيير وحدها ليست تأكيدًا مستقلًا.
- القرار السابق: لا يُفعّل تغيير الحساب البنكي في الرواتب قبل التأكيد المستقل.
- القرار الجديد: يُفعّل التغيير بعد اتصال موثق بالرقم المعروف سابقًا وتأكيد الموظف.
- سبب الإجابة المقترحة: التأكيد المستقل تحقق قبل التفعيل.

### English

- Context: Independent confirmation is a documented call to the employee using a previously known number. The change-request message alone is not independent confirmation.
- Existing decision: A bank-account change in payroll must not be activated before independent confirmation.
- New decision: The change is activated after a documented call to the previously known number and the employee's confirmation.
- Proposed answer rationale: Independent confirmation occurred before activation.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0165 — information_security / storage encryption

عائلة المراجعة: F031 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الملف يحتوي بيانات موظفين سرية. تشفير النقل وحده لا يشفر الملف المخزن.
- القرار السابق: يجب تشفير الملفات السرية عند تخزينها.
- القرار الجديد: يُخزن الملف في خدمة تسمى SecureStore، ولا تتوفر مواصفاتها.
- سبب الإجابة المقترحة: اسم الخدمة لا يثبت تشفير البيانات المخزنة.

### English

- Context: The file contains confidential employee data. Transport encryption alone does not encrypt the stored file.
- Existing decision: Confidential files must be encrypted at rest.
- New decision: The file is stored in a service named SecureStore, whose specifications are unavailable.
- Proposed answer rationale: The service name does not establish encryption at rest.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0166 — projects / finish-to-start dependency

عائلة المراجعة: F096 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الاختبار A والنشر B مرحلتان منفصلتان. اكتمال A حدث محدد وليس مجرد بدء اختباره.
- القرار السابق: لا يبدأ النشر B إلا بعد اكتمال الاختبار A بنجاح.
- القرار الجديد: يبدأ B بالتزامن مع بدء A وقبل اكتماله.
- سبب الإجابة المقترحة: النشر يبدأ قبل تحقق شرطه السابق.

### English

- Context: Testing A and deployment B are separate stages. Completion of A is a specific event, not merely the start of testing.
- Existing decision: Deployment B must not start until testing A has been completed successfully.
- New decision: B starts at the same time as A begins, before A is completed.
- Proposed answer rationale: Deployment starts before its prerequisite is satisfied.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0167 — expenses / duplicate reimbursement

عائلة المراجعة: F022 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الفاتورة I7 صُرفت بالكامل سابقًا. الفاتورة I8 لم تُصرف من قبل.
- القرار السابق: يُمنع سداد المصروف نفسه أكثر من مرة.
- القرار الجديد: يُصرف مبلغ الفاتورة I7 مرة أخرى.
- سبب الإجابة المقترحة: المصروف سبق سداده بالكامل.

### English

- Context: Invoice I7 has already been reimbursed in full. Invoice I8 has never been reimbursed.
- Existing decision: The same expense must not be reimbursed more than once.
- New decision: The amount of invoice I7 is reimbursed again.
- Proposed answer rationale: The expense was already fully reimbursed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0168 — projects / working-day calendar

عائلة المراجعة: F097 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: التقويم المحدد لهذا الاختبار: الأيام 1 و2 و5 أيام عمل، و3 و4 عطلة. يبدأ العد بعد نهاية اليوم 1.
- القرار السابق: لا يجوز بدء التنفيذ قبل مرور يومي عمل كاملين بعد نهاية اليوم 1.
- القرار الجديد: يبدأ التنفيذ بعد نهاية اليوم 5 مباشرة.
- سبب الإجابة المقترحة: اكتمل يوما العمل 2 و5.

### English

- Context: The test calendar defines days 1, 2, and 5 as working days, and days 3 and 4 as holidays. Counting starts after the end of day 1.
- Existing decision: Execution must not start until two full working days have elapsed after the end of day 1.
- New decision: Execution starts immediately after the end of day 5.
- Proposed answer rationale: Working days 2 and 5 have both been completed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0169 — information_security / incident reporting window

عائلة المراجعة: F033 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المهلة تبدأ عند اكتشاف الحادث وتُحسب بساعات متصلة، بما فيها الليل.
- القرار السابق: يجب الإبلاغ عن الحادث خلال ساعتين من اكتشافه.
- القرار الجديد: يؤجل أول إبلاغ عن حادث اكتُشف 09:00 إلى 12:00 في اليوم نفسه.
- سبب الإجابة المقترحة: التأخير ثلاث ساعات ويتجاوز ساعتين.

### English

- Context: The deadline starts at incident discovery and is measured in continuous hours, including overnight.
- Existing decision: An incident must be reported within two hours of discovery.
- New decision: The first report of an incident discovered at 09:00 is delayed until 12:00 the same day.
- Proposed answer rationale: The delay is three hours, exceeding two.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0170 — logistics / delivery identity

عائلة المراجعة: F091 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المستلم المعين للشحنة هو A. تسليم الشحنة لشخص آخر يتطلب تفويضًا مكتوبًا من A.
- القرار السابق: لا تُسلم الشحنة إلا إلى A أو شخص يحمل تفويضًا مكتوبًا منه.
- القرار الجديد: تُسلم الشحنة إلى B دون تفويض مكتوب، لأنه يعرف A.
- سبب الإجابة المقترحة: المعرفة الشخصية لا تحقق التفويض المطلوب.

### English

- Context: The shipment's designated recipient is A. Delivery to another person requires written authorization from A.
- Existing decision: The shipment may be delivered only to A or a person carrying written authorization from A.
- New decision: The shipment is delivered to B without written authorization because B knows A.
- Proposed answer rationale: Personal acquaintance does not satisfy the required authorization.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0171 — facilities / temperature interval

عائلة المراجعة: F049 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المقارنة تخص نقطة ضبط حرارة غرفة الخوادم نفسها، بالدرجة المئوية.
- القرار السابق: يجب أن تكون نقطة ضبط الحرارة بين 18 و24 درجة شاملًا الطرفين.
- القرار الجديد: تُفعّل وضعية Eco، ولا تُعرف نقطة الضبط التي تستخدمها.
- سبب الإجابة المقترحة: يلزم معرفة درجة الضبط في وضعية Eco.

### English

- Context: The comparison concerns the temperature setpoint of the same server room, in degrees Celsius.
- Existing decision: The temperature setpoint must be between 18 and 24 degrees, inclusive.
- New decision: Eco mode is enabled, and its temperature setpoint is unknown.
- Proposed answer rationale: The setpoint used in Eco mode is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0172 — meetings / voting denominator

عائلة المراجعة: F053 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: اللجنة عشرة أعضاء، والقاعدة تعتمد كامل العضوية حتى عند الغياب.
- القرار السابق: إقرار المقترح يتطلب موافقة أكثر من نصف جميع أعضاء اللجنة.
- القرار الجديد: يُعلن إقرار المقترح بخمسة أصوات موافقة من أصل عشرة أعضاء.
- سبب الإجابة المقترحة: خمسة تساوي النصف ولا تزيد عليه.

### English

- Context: The committee has ten members, and the rule uses the entire membership even when some are absent.
- Existing decision: Adopting a proposal requires approval by more than half of all committee members.
- New decision: The proposal is declared adopted with five approving votes out of ten members.
- Proposed answer rationale: Five equals half rather than exceeding it.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0173 — facilities / room capacity

عائلة المراجعة: F046 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: القاعة H تسع 40 شخصًا كحد أقصى، ويشمل العدد المشاركين والمنظمين.
- القرار السابق: يُمنع تجاوز سعة القاعة H أثناء أي نشاط.
- القرار الجديد: يحضر النشاط في H عدد 38 مشاركًا وخمسة منظمين في الوقت نفسه.
- سبب الإجابة المقترحة: المجموع 43 ويتجاوز سعة 40.

### English

- Context: Room H holds at most 40 people, counting both participants and organizers.
- Existing decision: Room H's capacity must not be exceeded during any event.
- New decision: An event in H has 38 participants and five organizers present simultaneously.
- Proposed answer rationale: The total is 43, exceeding the capacity of 40.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0174 — facilities / maintenance closure

عائلة المراجعة: F048 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المبنى N مغلق كامل يوم 2030-10-15. المبنى M مفتوح ومستقل عنه.
- القرار السابق: يُمنع عقد أي اجتماع حضوري داخل N أثناء إغلاقه.
- القرار الجديد: يُعقد اجتماع حضوري داخل N ظهر 2030-10-15.
- سبب الإجابة المقترحة: المكان والوقت داخل نطاق الإغلاق.

### English

- Context: Building N is closed throughout 2030-10-15. Building M is open and separate.
- Existing decision: No in-person meeting may be held inside N while it is closed.
- New decision: An in-person meeting is held inside N at noon on 2030-10-15.
- Proposed answer rationale: The location and time fall within the closure.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0175 — projects / working-day calendar

عائلة المراجعة: F097 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: التقويم المحدد لهذا الاختبار: الأيام 1 و2 و5 أيام عمل، و3 و4 عطلة. يبدأ العد بعد نهاية اليوم 1.
- القرار السابق: لا يجوز بدء التنفيذ قبل مرور يومي عمل كاملين بعد نهاية اليوم 1.
- القرار الجديد: يبدأ التنفيذ عند نهاية دوام الفريق، دون تحديد رقم اليوم الذي سيبدأ فيه.
- سبب الإجابة المقترحة: يلزم رقم يوم البداية لمعرفة هل اكتمل يوما العمل المطلوبان.

### English

- Context: The test calendar defines days 1, 2, and 5 as working days, and days 3 and 4 as holidays. Counting starts after the end of day 1.
- Existing decision: Execution must not start until two full working days have elapsed after the end of day 1.
- New decision: Execution starts at the end of the team's working day, without identifying which numbered day it starts on.
- Proposed answer rationale: The start day's number is needed to determine whether the required two working days have elapsed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0176 — quality / sample proportion

عائلة المراجعة: F071 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الدفعة فيها 200 قطعة. يجب تقريب أي حد أدنى كسري لعدد القطع إلى الأعلى.
- القرار السابق: يجب فحص 10% على الأقل من قطع كل دفعة قبل الإفراج عنها.
- القرار الجديد: يُفرج عن الدفعة بعد فحص عينة وُصفت بالكافية دون تحديد عددها.
- سبب الإجابة المقترحة: يلزم عدد القطع المفحوصة.

### English

- Context: The batch contains 200 items. Any fractional minimum item count must be rounded upward.
- Existing decision: At least 10% of the items in each batch must be inspected before release.
- New decision: The batch is released after inspecting a sample described as sufficient without stating its size.
- Proposed answer rationale: The number of inspected items is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0177 — communications / publication embargo

عائلة المراجعة: F061 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الإعلان A تحت حظر نشر حتى 2030-12-01 الساعة 09:00 بالتوقيت المحلي. جميع الأوقات بالتوقيت نفسه.
- القرار السابق: يُمنع نشر A للعامة قبل انتهاء حظر النشر.
- القرار الجديد: يُنشر A للعامة يوم 2030-12-01 الساعة 09:00.
- سبب الإجابة المقترحة: النشر يقع عند انتهاء الحظر.

### English

- Context: Announcement A is under embargo until 2030-12-01 at 09:00 local time. All times use that same time zone.
- Existing decision: A must not be published publicly before the embargo ends.
- New decision: A is published publicly on 2030-12-01 at 09:00.
- Proposed answer rationale: Publication occurs when the embargo ends.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0178 — meetings / quorum

عائلة المراجعة: F051 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: اللجنة سبعة أعضاء، والحضور يحسب بالأشخاص لا بعدد الأصوات المفوضة.
- القرار السابق: لا يصدر قرار اللجنة إلا بحضور أربعة أعضاء على الأقل.
- القرار الجديد: يصدر قرار اللجنة بحضور خمسة أعضاء.
- سبب الإجابة المقترحة: الحضور يحقق النصاب.

### English

- Context: The committee has seven members, and attendance counts people rather than delegated votes.
- Existing decision: A committee decision may be issued only with at least four members present.
- New decision: The committee decision is issued with five members present.
- Proposed answer rationale: Attendance meets the quorum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0179 — facilities / overlapping reservations

عائلة المراجعة: F047 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحجزان يتطلبان الاستخدام الحصري للقاعة نفسها. الفترات من البداية المشمولة إلى النهاية غير المشمولة.
- القرار السابق: القاعة محجوزة حصريًا للفريق A من 09:00 إلى 10:00 يوم 2030-09-12.
- القرار الجديد: تُحجز القاعة حصريًا للفريق B من 09:30 إلى 10:30 في اليوم نفسه.
- سبب الإجابة المقترحة: يتداخل الاستخدام الحصري بين 09:30 و10:00.

### English

- Context: Both bookings require exclusive use of the same room. Intervals include their start and exclude their end.
- Existing decision: The room is reserved exclusively for Team A from 09:00 to 10:00 on 2030-09-12.
- New decision: The room is reserved exclusively for Team B from 09:30 to 10:30 that same day.
- Proposed answer rationale: Exclusive use overlaps between 09:30 and 10:00.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0180 — facilities / room capacity

عائلة المراجعة: F046 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: القاعة H تسع 40 شخصًا كحد أقصى، ويشمل العدد المشاركين والمنظمين.
- القرار السابق: يُمنع تجاوز سعة القاعة H أثناء أي نشاط.
- القرار الجديد: يحضر 38 مشاركًا إلى H، وعدد المنظمين الحاضرين غير محدد.
- سبب الإجابة المقترحة: يلزم العدد الإجمالي الموجود في القاعة.

### English

- Context: Room H holds at most 40 people, counting both participants and organizers.
- Existing decision: Room H's capacity must not be exceeded during any event.
- New decision: 38 participants attend in H, and the number of organizers present is unspecified.
- Proposed answer rationale: The total number present in the room is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0181 — finance / payment prerequisites AND

عائلة المراجعة: F043 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المستندان المطلوبان مستقلان: فاتورة معتمدة ومحضر استلام موقع.
- القرار السابق: لا يُصرف مبلغ المورد إلا بعد توفر الفاتورة المعتمدة ومحضر الاستلام الموقع معًا.
- القرار الجديد: يُصرف المبلغ مع توفر الفاتورة، وحالة محضر الاستلام غير معروفة.
- سبب الإجابة المقترحة: وجود الفاتورة وحدها لا يحدد تحقق الشرط الآخر.

### English

- Context: The two required documents are independent: an approved invoice and a signed receipt-of-goods record.
- Existing decision: The supplier must not be paid until both the approved invoice and signed receipt-of-goods record are available.
- New decision: Payment is made with the invoice available, while the receipt-of-goods record status is unknown.
- Proposed answer rationale: Having the invoice alone does not establish the other condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0182 — projects / working-day calendar

عائلة المراجعة: F097 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: التقويم المحدد لهذا الاختبار: الأيام 1 و2 و5 أيام عمل، و3 و4 عطلة. يبدأ العد بعد نهاية اليوم 1.
- القرار السابق: لا يجوز بدء التنفيذ قبل مرور يومي عمل كاملين بعد نهاية اليوم 1.
- القرار الجديد: يبدأ التنفيذ في بداية اليوم 5.
- سبب الإجابة المقترحة: مر يوم عمل كامل واحد فقط، وهو اليوم 2.

### English

- Context: The test calendar defines days 1, 2, and 5 as working days, and days 3 and 4 as holidays. Counting starts after the end of day 1.
- Existing decision: Execution must not start until two full working days have elapsed after the end of day 1.
- New decision: Execution starts at the beginning of day 5.
- Proposed answer rationale: Only one full working day has elapsed: day 2.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0183 — quality / audit frequency

عائلة المراجعة: F074 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الشهور تقويمية، وكل زيارة تدقيق مستقلة. المقارنة تخص خطة السنة المقبلة.
- القرار السابق: يجب إجراء زيارة تدقيق واحدة على الأقل في كل شهر.
- القرار الجديد: تُعتمد خطة تضم 12 زيارة سنوية دون تحديد توزيعها على الشهور.
- سبب الإجابة المقترحة: يلزم الجدول الشهري، وليس المجموع وحده.

### English

- Context: Months are calendar months, and each audit visit is separate. The comparison concerns next year's plan.
- Existing decision: At least one audit visit must take place in every month.
- New decision: A plan with twelve annual visits is approved without specifying their distribution across months.
- Proposed answer rationale: The monthly schedule is needed, not merely the total.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0184 — expenses / currency conversion

عائلة المراجعة: F024 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحد بالعملة X. سعر التحويل المعتمد هو وحدة Y واحدة تساوي وحدتين X.
- القرار السابق: يجب ألا يتجاوز إجمالي التعويض 1000 وحدة X بعد التحويل.
- القرار الجديد: يُعوض الموظف بمبلغ 600 وحدة Y.
- سبب الإجابة المقترحة: 600 Y تساوي 1200 X وتتجاوز الحد.

### English

- Context: The cap is in currency X. The approved exchange rate is one Y unit equals two X units.
- Existing decision: Total reimbursement must not exceed 1000 X units after conversion.
- New decision: The employee is reimbursed 600 Y units.
- Proposed answer rationale: 600 Y equals 1200 X, exceeding the cap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0185 — facilities / emergency access

عائلة المراجعة: F050 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: ممر E مخرج الطوارئ الوحيد. المخزن S منفصل ولا يدخل في مسار الإخلاء.
- القرار السابق: يجب بقاء ممر E خاليًا من أي صناديق طوال الوقت.
- القرار الجديد: توضع الصناديق في المخزن S مع إبقاء E خاليًا.
- سبب الإجابة المقترحة: القرار يحافظ على خلو الممر.

### English

- Context: Passage E is the only emergency exit route. Store S is separate and outside the evacuation route.
- Existing decision: Passage E must remain free of boxes at all times.
- New decision: Boxes are placed in store S while E remains clear.
- Proposed answer rationale: The decision keeps the passage clear.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0186 — records / original versus copy

عائلة المراجعة: F039 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الأصل الورقي والنسخة الممسوحة سجلان متميزان. إنشاء النسخة لا يلغي وجوب حفظ الأصل.
- القرار السابق: يجب حفظ العقد الورقي الأصلي، ويجوز إنشاء نسخة إلكترونية للاستخدام اليومي.
- القرار الجديد: يُتلف الأصل الورقي فور إنشاء النسخة الإلكترونية.
- سبب الإجابة المقترحة: حفظ النسخة لا يحقق حفظ الأصل المطلوب.

### English

- Context: The paper original and scanned copy are distinct records. Creating a copy does not waive original retention.
- Existing decision: The original paper contract must be retained; an electronic copy may be created for daily use.
- New decision: The paper original is destroyed immediately after the electronic copy is created.
- Proposed answer rationale: Keeping the copy does not satisfy required retention of the original.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0187 — records / active preservation hold

عائلة المراجعة: F037 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: ملف K عليه أمر حفظ داخلي نشط حتى إشعار الرفع، ولا يجوز اعتبار انتهاء المدة العادية رفعًا للأمر.
- القرار السابق: يُمنع إتلاف ملف عليه أمر حفظ نشط حتى صدور إشعار رفع الأمر.
- القرار الجديد: يُتلف K الآن لأن مدة الاحتفاظ العادية انتهت، مع بقاء أمر الحفظ نشطًا.
- سبب الإجابة المقترحة: انتهاء المدة لا يلغي أمر الحفظ النشط.

### English

- Context: File K has an active internal preservation hold until a release notice; expiry of ordinary retention does not release the hold.
- Existing decision: A file under an active preservation hold must not be destroyed until a release notice is issued.
- New decision: K is destroyed now because ordinary retention has expired, while the hold remains active.
- Proposed answer rationale: Retention expiry does not cancel the active hold.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0188 — logistics / vehicle allocation overlap

عائلة المراجعة: F093 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المركبة V واحدة، والمهمتان تتطلبانها طوال مدتيهما. فترات الاستخدام تستثني وقت النهاية.
- القرار السابق: تُخصص V حصريًا للمهمة A من 13:00 إلى 15:00 في اليوم المحدد.
- القرار الجديد: تُخصص V للمهمة B من 15:00 إلى 16:00 في اليوم نفسه، ولا يلزم وقت انتقال.
- سبب الإجابة المقترحة: المهمتان متعاقبتان دون تداخل.

### English

- Context: There is one vehicle V, and both missions require it throughout their durations. Usage intervals exclude their end time.
- Existing decision: V is allocated exclusively to mission A from 13:00 to 15:00 on the specified day.
- New decision: V is allocated to mission B from 15:00 to 16:00 that day, with no transfer time required.
- Proposed answer rationale: The missions are consecutive without overlap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0189 — projects / finish-to-start dependency

عائلة المراجعة: F096 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الاختبار A والنشر B مرحلتان منفصلتان. اكتمال A حدث محدد وليس مجرد بدء اختباره.
- القرار السابق: لا يبدأ النشر B إلا بعد اكتمال الاختبار A بنجاح.
- القرار الجديد: يبدأ B بعد انتهاء نشاط التحقق X، ولا يُعرف هل X هو الاختبار A أو ما كانت نتيجته.
- سبب الإجابة المقترحة: يلزم تحديد X ونتيجة الاختبار المطلوب.

### English

- Context: Testing A and deployment B are separate stages. Completion of A is a specific event, not merely the start of testing.
- Existing decision: Deployment B must not start until testing A has been completed successfully.
- New decision: B starts after verification activity X ends, and it is unknown whether X is test A or what its result was.
- Proposed answer rationale: X's identity and the required test result are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0190 — training / prerequisite completion

عائلة المراجعة: F056 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الدورة المتقدمة T تتطلب إكمال الأساسيات. التسجيل في الأساسيات وحده لا يعد إكمالًا.
- القرار السابق: لا يبدأ الموظف الدورة T قبل إكمال دورة الأساسيات.
- القرار الجديد: يبدأ الموظف T بعد توثيق إكمال الأساسيات.
- سبب الإجابة المقترحة: الإكمال سبق بدء الدورة المتقدمة.

### English

- Context: Advanced course T requires completion of the basics. Merely enrolling in the basics does not count as completion.
- Existing decision: An employee must not start course T before completing the basics course.
- New decision: The employee starts T after basics completion is documented.
- Proposed answer rationale: Completion preceded the advanced course start.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0191 — meetings / peer departments

عائلة المراجعة: F055 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: القسمان A وB مستقلان في تنظيم اجتماعاتهما. لا موظفين أو قاعات مشتركة في الاجتماعات المذكورة.
- القرار السابق: يُعقد اجتماع القسم A الأسبوعي يوم الاثنين فقط.
- القرار الجديد: يُعقد اجتماع القسم B الأسبوعي يوم الثلاثاء فقط.
- سبب الإجابة المقترحة: اجتماع B مستقل وخارج نطاق قرار A.

### English

- Context: Departments A and B organize their meetings independently. The stated meetings share neither employees nor rooms.
- Existing decision: Department A's weekly meeting is held only on Monday.
- New decision: Department B's weekly meeting is held only on Tuesday.
- Proposed answer rationale: B's meeting is independent and outside A's decision scope.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0192 — projects / aggregate staff allocation

عائلة المراجعة: F099 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الموظف E متاح 30 ساعة للمشاريع خلال الأسبوع، ولا يسمح بتجاوز هذه الطاقة.
- القرار السابق: يجب ألا يتجاوز مجموع ساعات تكليف E في جميع المشاريع 30 ساعة لهذا الأسبوع.
- القرار الجديد: يضاف تكليف عشر ساعات إلى E هذا الأسبوع، وساعات تكليفاته الأخرى غير متاحة.
- سبب الإجابة المقترحة: يلزم مجموع التكليفات الأخرى.

### English

- Context: Employee E has 30 hours available for projects during the week, and this capacity must not be exceeded.
- Existing decision: E's total assigned hours across all projects must not exceed 30 this week.
- New decision: A ten-hour assignment is added for E this week, and hours for other assignments are unavailable.
- Proposed answer rationale: The total of the other assignments is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0193 — quality / all versus most

عائلة المراجعة: F073 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: يوجد عشرة عيوب حرجة في الإصدار. إغلاق العيب يعني التحقق من إصلاحه.
- القرار السابق: لا يُطلق الإصدار إلا بعد إغلاق جميع العيوب الحرجة.
- القرار الجديد: يُطلق الإصدار بعد إغلاق تسعة عيوب مع بقاء العاشر مفتوحًا.
- سبب الإجابة المقترحة: إغلاق معظم العيوب لا يحقق شرط الجميع.

### English

- Context: The release has ten critical defects. Closing a defect means its repair has been verified.
- Existing decision: The release must not be launched until all critical defects are closed.
- New decision: The release is launched after nine defects are closed while the tenth remains open.
- Proposed answer rationale: Closing most defects does not satisfy the all-defects requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0194 — records / minimum retention

عائلة المراجعة: F036 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: العمر محسوب من تاريخ إقفال الملف. لا توجد التزامات احتفاظ إضافية.
- القرار السابق: يجب الاحتفاظ بالسجل خمس سنوات على الأقل بعد إقفاله.
- القرار الجديد: يُتلف سجل بعد ثلاث سنوات من إقفاله.
- سبب الإجابة المقترحة: الإتلاف يسبق اكتمال الحد الأدنى.

### English

- Context: Age is measured from the file closure date. No additional retention obligations apply.
- Existing decision: A record must be retained for at least five years after closure.
- New decision: A record is destroyed three years after closure.
- Proposed answer rationale: Destruction occurs before the minimum retention period ends.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0195 — information_security / public redaction

عائلة المراجعة: F035 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: أسماء الأفراد وأرقام هوياتهم بيانات شخصية. أرقام الإحصاءات المجمعة هنا لا تعرّف أفرادًا.
- القرار السابق: يجب إزالة جميع البيانات الشخصية قبل نشر التقرير للعامة.
- القرار الجديد: يُنشر التقرير للعامة متضمنًا أسماء الموظفين وأرقام هوياتهم.
- سبب الإجابة المقترحة: النشر يتضمن بيانات يجب إزالتها.

### English

- Context: Individuals' names and identity numbers are personal data. The aggregate statistics here do not identify individuals.
- Existing decision: All personal data must be removed before publishing the report publicly.
- New decision: The report is published publicly with employee names and identity numbers.
- Proposed answer rationale: Publication includes data that must be removed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0196 — customer_service / branch-specific hours

عائلة المراجعة: F069 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الفرعان الشرقي والغربي وحدتان مستقلتان. ساعات العمل كلها محلية لليوم نفسه.
- القرار السابق: يجب أن يبقى مكتب خدمة العملاء في الفرع الشرقي مفتوحًا من 09:00 حتى 17:00.
- القرار الجديد: يُغلق مكتب الخدمة الساعة 15:00 دون تسمية الفرع.
- سبب الإجابة المقترحة: يلزم تحديد الفرع المتأثر.

### English

- Context: The eastern and western branches are separate units. All hours are local and concern the same day.
- Existing decision: The eastern branch's customer-service desk must remain open from 09:00 until 17:00.
- New decision: The service desk closes at 15:00 without naming the branch.
- Proposed answer rationale: The affected branch must be identified.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0197 — procurement / emergency exemption

عائلة المراجعة: F019 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المراجعة العادية تتطلب مناقصة. الإعفاء الوحيد هو إعلان طوارئ رسمي لهذه المشتريات.
- القرار السابق: تُجرى مناقصة قبل الشراء، ويجوز الشراء المباشر عند وجود إعلان الطوارئ المحدد.
- القرار الجديد: يُنفذ شراء مباشر دون مناقصة في ظل إعلان طوارئ رسمي يغطي هذا الطلب.
- سبب الإجابة المقترحة: الطلب مشمول بالإعفاء المحدد.

### English

- Context: Ordinary review requires a tender. The only exemption is an official emergency declaration covering these purchases.
- Existing decision: A tender must precede the purchase; direct purchasing is allowed when the specified emergency declaration exists.
- New decision: A direct purchase is executed without a tender under an official emergency declaration covering this request.
- Proposed answer rationale: The request is covered by the stated exemption.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0198 — quality / alternative evidence routes

عائلة المراجعة: F075 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الوثيقتان A وB بديلتان مقبولتان، ولا توجد شروط إثبات أخرى لهذه الخطوة.
- القرار السابق: يجوز إغلاق الملاحظة بتقرير اختبار A أو بشهادة مطابقة B؛ لا يجوز إغلاقها دون أحدهما.
- القرار الجديد: تُغلق الملاحظة بمستند D دون بيان محتواه أو نوعه.
- سبب الإجابة المقترحة: يلزم معرفة هل D يمثل A أو B.

### English

- Context: Documents A and B are acceptable alternatives, with no other evidence conditions for this step.
- Existing decision: A finding may be closed with either test report A or conformity certificate B; it must not be closed without one of them.
- New decision: The finding is closed using document D without describing its content or type.
- Proposed answer rationale: It is necessary to determine whether D is A or B.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0199 — records / version effective dates

عائلة المراجعة: F038 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الإصدار V1 ساري حتى نهاية 2030-03-31، وV2 يبدأ 2030-04-01 ويحل محله صراحة.
- القرار السابق: يجب استخدام الإصدار الساري بتاريخ المعاملة: V1 قبل أبريل وV2 من أول أبريل.
- القرار الجديد: تُعالج المعاملة باستخدام V1، دون تحديد تاريخ المعاملة.
- سبب الإجابة المقترحة: يلزم التاريخ لتحديد الإصدار الساري.

### English

- Context: Version V1 is effective through the end of 2030-03-31; V2 starts on 2030-04-01 and explicitly replaces it.
- Existing decision: Use the version effective on the transaction date: V1 before April and V2 from April 1.
- New decision: The transaction is processed using V1 without specifying its transaction date.
- Proposed answer rationale: The date is needed to determine the effective version.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0200 — facilities / overlapping reservations

عائلة المراجعة: F047 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحجزان يتطلبان الاستخدام الحصري للقاعة نفسها. الفترات من البداية المشمولة إلى النهاية غير المشمولة.
- القرار السابق: القاعة محجوزة حصريًا للفريق A من 09:00 إلى 10:00 يوم 2030-09-12.
- القرار الجديد: تُحجز القاعة حصريًا للفريق B من 10:00 إلى 11:00 في اليوم نفسه.
- سبب الإجابة المقترحة: الحجز الثاني يبدأ عند نهاية الأول دون تداخل.

### English

- Context: Both bookings require exclusive use of the same room. Intervals include their start and exclude their end.
- Existing decision: The room is reserved exclusively for Team A from 09:00 to 10:00 on 2030-09-12.
- New decision: The room is reserved exclusively for Team B from 10:00 to 11:00 that same day.
- Proposed answer rationale: The second booking starts at the first one's end without overlap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0201 — attendance / weekly ceiling

عائلة المراجعة: F003 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: جميع الساعات المذكورة ساعات عمل فعلية لنفس الموظف في الأسبوع نفسه.
- القرار السابق: لا يجوز أن يتجاوز عمل الموظف 40 ساعة في الأسبوع.
- القرار الجديد: يُكلف الموظف بالعمل 38 ساعة هذا الأسبوع.
- سبب الإجابة المقترحة: 38 ضمن الحد الأقصى.

### English

- Context: All stated hours are actual working hours for the same employee in the same week.
- Existing decision: The employee must not work more than 40 hours per week.
- New decision: The employee is assigned 38 working hours this week.
- Proposed answer rationale: 38 is within the maximum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0202 — quality / independent audit

عائلة المراجعة: F072 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المدقق A شارك في تنفيذ العملية، والمدقق B لم يشارك فيها بأي دور تنفيذي.
- القرار السابق: لا يتولى التدقيق النهائي للعملية شخص شارك في تنفيذها.
- القرار الجديد: يُعيّن B مدققًا نهائيًا لهذه العملية.
- سبب الإجابة المقترحة: المدقق مستقل عن تنفيذ العملية.

### English

- Context: Auditor A participated in executing the process; auditor B had no execution role in it.
- Existing decision: Final process auditing must not be performed by someone who participated in its execution.
- New decision: B is appointed final auditor for this process.
- Proposed answer rationale: The auditor is independent of process execution.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0203 — leave / handover condition

عائلة المراجعة: F008 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الموظفة S مسؤولة مناوبة. بدء الإجازة لا يلغي شرط التسليم.
- القرار السابق: لا تبدأ إجازة مسؤول المناوبة قبل قبول البديل لمحضر التسليم.
- القرار الجديد: تبدأ إجازة S اليوم، لكن وقت قبول البديل للمحضر غير معلوم.
- سبب الإجابة المقترحة: يلزم معرفة توقيت القبول بالنسبة لبداية الإجازة.

### English

- Context: Employee S is an on-call lead. Starting leave does not waive the handover requirement.
- Existing decision: An on-call lead's leave must not start before the replacement accepts the handover record.
- New decision: S's leave starts today, but the time of the replacement's acceptance is unknown.
- Proposed answer rationale: The acceptance time relative to the leave start is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0204 — training / minimum annual hours

عائلة المراجعة: F058 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: السنة التدريبية تنتهي بعد تنفيذ القرار، ولا توجد أنشطة تدريبية أخرى هذا العام.
- القرار السابق: يجب أن يكمل كل موظف 20 ساعة تدريب على الأقل خلال السنة.
- القرار الجديد: تُقفل الخطة السنوية للموظف عند إجمالي نهائي قدره 16 ساعة.
- سبب الإجابة المقترحة: الإجمالي النهائي أقل من المطلوب.

### English

- Context: The training year ends after the decision is carried out, and there are no other training activities this year.
- Existing decision: Every employee must complete at least 20 training hours during the year.
- New decision: The employee's annual plan is closed with a final total of 16 hours.
- Proposed answer rationale: The final total is below the requirement.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0205 — information_security / incident reporting window

عائلة المراجعة: F033 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المهلة تبدأ عند اكتشاف الحادث وتُحسب بساعات متصلة، بما فيها الليل.
- القرار السابق: يجب الإبلاغ عن الحادث خلال ساعتين من اكتشافه.
- القرار الجديد: يتم أول إبلاغ 10:30 عن حادث اكتُشف 09:00 في اليوم نفسه.
- سبب الإجابة المقترحة: الفاصل ساعة ونصف ضمن المهلة.

### English

- Context: The deadline starts at incident discovery and is measured in continuous hours, including overnight.
- Existing decision: An incident must be reported within two hours of discovery.
- New decision: The first report is made at 10:30 for an incident discovered at 09:00 the same day.
- Proposed answer rationale: The interval is one and a half hours, within the deadline.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0206 — it_access / authentication alternatives

عائلة المراجعة: F028 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: كل الحسابات المقصودة حسابات إدارية حساسة. كلمة المرور وحدها عامل واحد.
- القرار السابق: يجب استخدام عاملين مستقلين على الأقل عند كل دخول إلى حساب إداري.
- القرار الجديد: يُستخدم نظام الدخول السريع X، دون وصف عوامل التحقق فيه.
- سبب الإجابة المقترحة: يلزم معرفة عدد العوامل واستقلالها.

### English

- Context: All accounts concerned are sensitive administrator accounts. A password alone is one factor.
- Existing decision: At least two independent factors must be used for every administrator-account login.
- New decision: Quick-login system X is used, without describing its authentication factors.
- Proposed answer rationale: The number and independence of the factors are needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0207 — communications / bilingual simultaneous release

عائلة المراجعة: F062 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الإعلان رسمي، والمطلوب نسختان عربـية وإنجليزية كاملتان. الملخص لا يعد نسخة كاملة.
- القرار السابق: يجب نشر النسختين العربية والإنجليزية من كل إعلان رسمي في الوقت نفسه.
- القرار الجديد: تُنشر النسخة العربية الساعة 14:00، وجدول نشر الإنجليزية غير متاح.
- سبب الإجابة المقترحة: يلزم موعد النسخة الإنجليزية للتحقق من التزامن.

### English

- Context: The announcement is official, and full Arabic and English versions are required. A summary is not a full version.
- Existing decision: The Arabic and English versions of every official announcement must be published at the same time.
- New decision: The Arabic version is published at 14:00, and the English publication schedule is unavailable.
- Proposed answer rationale: The English version's publication time is needed to check simultaneity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0208 — travel / fare class

عائلة المراجعة: F011 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الرحلة عملية مدتها أربع ساعات، ولا تنطبق عليها استثناءات الدرجة.
- القرار السابق: الرحلات التي تقل عن ست ساعات تُحجز بالدرجة الاقتصادية فقط.
- القرار الجديد: تُحجز الرحلة المذكورة بدرجة رجال الأعمال.
- سبب الإجابة المقترحة: درجة رجال الأعمال تخالف الاقتصار على الاقتصادية.

### English

- Context: The business flight lasts four hours, and no fare-class exceptions apply.
- Existing decision: Flights shorter than six hours must be booked in economy class only.
- New decision: The stated flight is booked in business class.
- Proposed answer rationale: Business class conflicts with the economy-only restriction.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0209 — finance / payment prerequisites AND

عائلة المراجعة: F043 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المستندان المطلوبان مستقلان: فاتورة معتمدة ومحضر استلام موقع.
- القرار السابق: لا يُصرف مبلغ المورد إلا بعد توفر الفاتورة المعتمدة ومحضر الاستلام الموقع معًا.
- القرار الجديد: يُصرف المبلغ بفاتورة معتمدة مع التأكيد بعدم وجود محضر استلام.
- سبب الإجابة المقترحة: أحد الشرطين الإلزاميين غير متحقق.

### English

- Context: The two required documents are independent: an approved invoice and a signed receipt-of-goods record.
- Existing decision: The supplier must not be paid until both the approved invoice and signed receipt-of-goods record are available.
- New decision: Payment is made with an approved invoice while confirming that no receipt-of-goods record exists.
- Proposed answer rationale: One of the two mandatory conditions is unmet.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0210 — meetings / voting denominator

عائلة المراجعة: F053 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: اللجنة عشرة أعضاء، والقاعدة تعتمد كامل العضوية حتى عند الغياب.
- القرار السابق: إقرار المقترح يتطلب موافقة أكثر من نصف جميع أعضاء اللجنة.
- القرار الجديد: يُعلن إقرار المقترح بستة أصوات موافقة من أصل عشرة أعضاء.
- سبب الإجابة المقترحة: ستة أكثر من نصف العضوية.

### English

- Context: The committee has ten members, and the rule uses the entire membership even when some are absent.
- Existing decision: Adopting a proposal requires approval by more than half of all committee members.
- New decision: The proposal is declared adopted with six approving votes out of ten members.
- Proposed answer rationale: Six exceeds half the membership.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0211 — inventory / calibration expiry

عائلة المراجعة: F077 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الجهاز A معاير وصالح، والجهاز B انتهت معايرته، ولا يوجد تمديد له.
- القرار السابق: تُستخدم في القياس أجهزة ذات معايرة سارية فقط.
- القرار الجديد: يُستخدم الجهاز C للقياس، وسجل معايرته غير متاح.
- سبب الإجابة المقترحة: يلزم التحقق من سريان معايرة C.

### English

- Context: Device A has valid calibration; device B's calibration has expired without extension.
- Existing decision: Only devices with valid calibration may be used for measurement.
- New decision: Device C is used for measurement, and its calibration record is unavailable.
- Proposed answer rationale: C's calibration validity must be established.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0212 — leave / consecutive duration

عائلة المراجعة: F007 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحد يطبق على كل فترة إجازة متصلة. الفترات المذكورة لا تتضمن انقطاعًا.
- القرار السابق: الحد الأقصى للإجازة المتصلة هو 12 يومًا تقويميًا.
- القرار الجديد: تُمنح للموظف إجازة متصلة مدتها 12 يومًا.
- سبب الإجابة المقترحة: الفترة تساوي الحد ولا تتجاوزه.

### English

- Context: The limit applies to each continuous leave period. The stated periods have no interruption.
- Existing decision: The maximum continuous leave period is 12 calendar days.
- New decision: The employee is granted 12 consecutive calendar days of leave.
- Proposed answer rationale: The period equals the limit without exceeding it.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0213 — payroll / aggregate deduction ceiling

عائلة المراجعة: F089 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: هذه قاعدة داخلية افتراضية للاختبار. الراتب الأساسي 5000 وحدة، والحد يشمل مجموع الخصومات المذكورة.
- القرار السابق: لا يتجاوز مجموع هذه الخصومات 10% من الراتب الأساسي في الشهر.
- القرار الجديد: يضاف خصم 200 وحدة، وقيمة الخصومات الأخرى للشهر غير معلومة.
- سبب الإجابة المقترحة: يلزم مجموع الخصومات الأخرى للتحقق من الحد الإجمالي.

### English

- Context: This is a fictional internal test rule. Basic salary is 5000 units, and the cap covers the total of the stated deductions.
- Existing decision: The total of these deductions must not exceed 10% of monthly basic salary.
- New decision: A deduction of 200 units is added, and the month's other deductions are unknown.
- Proposed answer rationale: The total of other deductions is needed to check the aggregate cap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0214 — information_security / removable media exception

عائلة المراجعة: F034 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: حالة وحدة USB A مشفرة ومعتمدة، ووحدة B غير مشفرة. حالة C غير موثقة.
- القرار السابق: لا تُنسخ ملفات العمل إلى وحدات USB إلا إذا كانت مشفرة ومعتمدة معًا.
- القرار الجديد: تُنسخ ملفات العمل إلى B بعد اعتمادها إداريًا دون تشفيرها.
- سبب الإجابة المقترحة: الاعتماد وحده لا يحقق الشرطين معًا.

### English

- Context: USB drive A is encrypted and approved; drive B is unencrypted. C's status is undocumented.
- Existing decision: Work files may be copied to USB drives only if the drives are both encrypted and approved.
- New decision: Work files are copied to B after administrative approval without encrypting it.
- Proposed answer rationale: Approval alone does not satisfy both conditions.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0215 — leave / staffing floor

عائلة المراجعة: F010 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: القسم فيه خمسة موظفين مجدولين في اليوم المقصود، ومن يأخذ إجازة لا يكون حاضرًا.
- القرار السابق: يجب بقاء ثلاثة موظفين على الأقل حاضرين في القسم كل يوم.
- القرار الجديد: يُمنح موظف إجازة لذلك اليوم، وحضور الموظفين الأربعة الآخرين غير معلوم.
- سبب الإجابة المقترحة: لا يُعرف عدد الحاضرين النهائي.

### English

- Context: The department has five employees scheduled for the day concerned, and anyone on leave is absent.
- Existing decision: At least three employees must remain present in the department every day.
- New decision: One employee receives leave that day, and the attendance of the other four is unknown.
- Proposed answer rationale: The final number of employees present is unknown.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0216 — recruitment / recognized equivalence

عائلة المراجعة: F082 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: لأغراض هذه الوظيفة فقط، الشهادة B معادلة صراحة للشهادة A، والشهادة C ليست معادلة لها.
- القرار السابق: يجب امتلاك الشهادة A أو ما يعادلها المعتمد للتعيين في الوظيفة.
- القرار الجديد: يُعيّن مرشح لا يملك سوى الشهادة C.
- سبب الإجابة المقترحة: C ليست الشهادة المطلوبة ولا معادلًا مقبولًا.

### English

- Context: For this position only, certificate B is explicitly equivalent to A, while certificate C is not equivalent.
- Existing decision: Appointment to the position requires certificate A or an approved equivalent.
- New decision: A candidate holding only certificate C is appointed.
- Proposed answer rationale: C is neither the required certificate nor an accepted equivalent.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0217 — it_access / access expiry

عائلة المراجعة: F027 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: تنتهي مهمة المتعاقد في نهاية 2030-08-31. الأوقات المذكورة بتوقيت الموقع نفسه.
- القرار السابق: يجب تعطيل وصول المتعاقد فور انتهاء مهمته، ولا يجوز إبقاؤه نشطًا بعدها.
- القرار الجديد: يبقى الوصول نشطًا حتى نهاية 2030-09-03.
- سبب الإجابة المقترحة: الوصول يستمر بعد انتهاء المهمة.

### English

- Context: The contractor's assignment ends at the end of 2030-08-31. All stated times use the same site time zone.
- Existing decision: Contractor access must be disabled when the assignment ends and must not remain active afterwards.
- New decision: Access remains active through the end of 2030-09-03.
- Proposed answer rationale: Access continues after the assignment ends.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0218 — inventory / safety stock

عائلة المراجعة: F076 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المخزون الحالي 60 وحدة، ولا توجد توريدات خلال الفترة المقصودة.
- القرار السابق: يجب ألا ينخفض المخزون المتبقي عن 20 وحدة.
- القرار الجديد: تُصرف 45 وحدة من المخزون الحالي فورًا.
- سبب الإجابة المقترحة: المتبقي 15 وحدة دون الحد الأدنى.

### English

- Context: Current stock is 60 units, with no deliveries during the period concerned.
- Existing decision: Remaining stock must not fall below 20 units.
- New decision: 45 units are issued immediately from current stock.
- Proposed answer rationale: 15 units remain, below the minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0219 — information_security / removable media exception

عائلة المراجعة: F034 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: حالة وحدة USB A مشفرة ومعتمدة، ووحدة B غير مشفرة. حالة C غير موثقة.
- القرار السابق: لا تُنسخ ملفات العمل إلى وحدات USB إلا إذا كانت مشفرة ومعتمدة معًا.
- القرار الجديد: تُنسخ ملفات العمل إلى C لكونها جديدة.
- سبب الإجابة المقترحة: كونها جديدة لا يبين التشفير أو الاعتماد.

### English

- Context: USB drive A is encrypted and approved; drive B is unencrypted. C's status is undocumented.
- Existing decision: Work files may be copied to USB drives only if the drives are both encrypted and approved.
- New decision: Work files are copied to C because it is new.
- Proposed answer rationale: Being new does not establish encryption or approval.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0220 — leave / staffing floor

عائلة المراجعة: F010 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: القسم فيه خمسة موظفين مجدولين في اليوم المقصود، ومن يأخذ إجازة لا يكون حاضرًا.
- القرار السابق: يجب بقاء ثلاثة موظفين على الأقل حاضرين في القسم كل يوم.
- القرار الجديد: تُمنح إجازة في اليوم نفسه لموظفين اثنين، ويحضر الثلاثة الآخرون.
- سبب الإجابة المقترحة: الحضور المتبقي يحقق الحد الأدنى.

### English

- Context: The department has five employees scheduled for the day concerned, and anyone on leave is absent.
- Existing decision: At least three employees must remain present in the department every day.
- New decision: Two employees receive leave on the same day, and the other three attend.
- Proposed answer rationale: The remaining attendance meets the minimum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0221 — facilities / temperature interval

عائلة المراجعة: F049 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المقارنة تخص نقطة ضبط حرارة غرفة الخوادم نفسها، بالدرجة المئوية.
- القرار السابق: يجب أن تكون نقطة ضبط الحرارة بين 18 و24 درجة شاملًا الطرفين.
- القرار الجديد: تُثبت نقطة الضبط على 21 درجة.
- سبب الإجابة المقترحة: 21 داخل المجال المسموح.

### English

- Context: The comparison concerns the temperature setpoint of the same server room, in degrees Celsius.
- Existing decision: The temperature setpoint must be between 18 and 24 degrees, inclusive.
- New decision: The setpoint is fixed at 21 degrees.
- Proposed answer rationale: 21 is inside the allowed interval.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0222 — information_security / external sharing

عائلة المراجعة: F032 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: تصنيف الوثيقة D سري داخلي. المكتب E خارج المنظمة، والموظف F عضو داخلي مخول بالاطلاع.
- القرار السابق: يُمنع إرسال الوثائق السرية الداخلية إلى أي مستلم خارج المنظمة.
- القرار الجديد: تُرسل D إلى المكتب E كاملة.
- سبب الإجابة المقترحة: المستلم خارج المنظمة والوثيقة سرية داخلية.

### English

- Context: Document D is classified as internal confidential. Office E is outside the organization, while employee F is an internal member authorized to view it.
- Existing decision: Internal confidential documents must not be sent to any recipient outside the organization.
- New decision: D is sent in full to Office E.
- Proposed answer rationale: The recipient is external and the document is internal confidential.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0223 — communications / recipient classification

عائلة المراجعة: F065 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: النشرة الفنية للمجموعة T فقط. الموظفة U ضمن T، والموظف V خارج T.
- القرار السابق: تُوزع النشرة الفنية على أعضاء T فقط.
- القرار الجديد: تُرسل النشرة إلى V.
- سبب الإجابة المقترحة: المستلم خارج المجموعة المحددة.

### English

- Context: The technical bulletin is for group T only. Employee U belongs to T, and employee V is outside T.
- Existing decision: The technical bulletin must be distributed only to members of T.
- New decision: The bulletin is sent to V.
- Proposed answer rationale: The recipient is outside the specified group.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0224 — meetings / quorum

عائلة المراجعة: F051 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: اللجنة سبعة أعضاء، والحضور يحسب بالأشخاص لا بعدد الأصوات المفوضة.
- القرار السابق: لا يصدر قرار اللجنة إلا بحضور أربعة أعضاء على الأقل.
- القرار الجديد: يصدر القرار بعد اجتماع للجنة، دون تسجيل عدد الحاضرين.
- سبب الإجابة المقترحة: يلزم عدد الحاضرين للتحقق من النصاب.

### English

- Context: The committee has seven members, and attendance counts people rather than delegated votes.
- Existing decision: A committee decision may be issued only with at least four members present.
- New decision: The decision is issued after a committee meeting, without recording the number present.
- Proposed answer rationale: The attendance count is needed to check the quorum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0225 — travel / fare class

عائلة المراجعة: F011 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الرحلة عملية مدتها أربع ساعات، ولا تنطبق عليها استثناءات الدرجة.
- القرار السابق: الرحلات التي تقل عن ست ساعات تُحجز بالدرجة الاقتصادية فقط.
- القرار الجديد: تُحجز الرحلة بفئة Flex، ولا توضح البيانات هل هي اقتصادية أم رجال أعمال.
- سبب الإجابة المقترحة: يلزم تحديد الدرجة المرتبطة بفئة Flex.

### English

- Context: The business flight lasts four hours, and no fare-class exceptions apply.
- Existing decision: Flights shorter than six hours must be booked in economy class only.
- New decision: The flight is booked with a Flex fare, and the data do not say whether it is economy or business class.
- Proposed answer rationale: The cabin class associated with the Flex fare is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0226 — it_access / read versus write

عائلة المراجعة: F026 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الحساب C حساب متعاقد. تنزيل نسخة محلية يعد قراءة، وتعديل الأصل يعد كتابة.
- القرار السابق: يسمح لحسابات المتعاقدين بقراءة المجلد المشترك فقط، وتُمنع الكتابة فيه.
- القرار الجديد: يُمنح الحساب C حق تعديل الملفات الأصلية في المجلد.
- سبب الإجابة المقترحة: التعديل كتابة محظورة على هذا النوع من الحسابات.

### English

- Context: Account C is a contractor account. Downloading a local copy counts as reading; changing the original counts as writing.
- Existing decision: Contractor accounts may only read the shared folder; writing to it is prohibited.
- New decision: Account C receives permission to edit the original files in the folder.
- Proposed answer rationale: Editing is a write operation prohibited for this account type.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0227 — expenses / currency conversion

عائلة المراجعة: F024 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحد بالعملة X. سعر التحويل المعتمد هو وحدة Y واحدة تساوي وحدتين X.
- القرار السابق: يجب ألا يتجاوز إجمالي التعويض 1000 وحدة X بعد التحويل.
- القرار الجديد: يُعوض الموظف بمبلغ 600 وحدة Z، وسعر تحويل Z غير متاح.
- سبب الإجابة المقترحة: يلزم سعر تحويل Z إلى X.

### English

- Context: The cap is in currency X. The approved exchange rate is one Y unit equals two X units.
- Existing decision: Total reimbursement must not exceed 1000 X units after conversion.
- New decision: The employee is reimbursed 600 Z units, and the exchange rate for Z is unavailable.
- Proposed answer rationale: The Z-to-X exchange rate is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0228 — meetings / agenda notice

عائلة المراجعة: F052 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الإشعار يحسب بالساعات المتصلة قبل بدء الاجتماع، والاجتماع غير طارئ.
- القرار السابق: يجب توزيع جدول أعمال الاجتماع غير الطارئ قبل بدايته بـ48 ساعة على الأقل.
- القرار الجديد: يُوزع الجدول في تاريخ يسبق تاريخ الاجتماع بيومين، دون معرفة ساعة الاجتماع أو ساعة التوزيع.
- سبب الإجابة المقترحة: اختلاف الساعتين قد يجعل الفاصل أقل من 48 ساعة أو أكثر.

### English

- Context: Notice is measured in continuous hours before the meeting starts, and the meeting is not an emergency.
- Existing decision: A non-emergency meeting's agenda must be distributed at least 48 hours before it starts.
- New decision: The agenda is distributed on a calendar date two days before the meeting date, without knowing either time of day.
- Proposed answer rationale: The two times of day could make the interval shorter or longer than 48 hours.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0229 — inventory / calibration expiry

عائلة المراجعة: F077 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الجهاز A معاير وصالح، والجهاز B انتهت معايرته، ولا يوجد تمديد له.
- القرار السابق: تُستخدم في القياس أجهزة ذات معايرة سارية فقط.
- القرار الجديد: يُستخدم A للقياس خلال مدة صلاحية معايرته.
- سبب الإجابة المقترحة: شرط المعايرة السارية متحقق.

### English

- Context: Device A has valid calibration; device B's calibration has expired without extension.
- Existing decision: Only devices with valid calibration may be used for measurement.
- New decision: A is used for measurement during its calibration validity period.
- Proposed answer rationale: The valid-calibration condition is satisfied.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0230 — quality / audit frequency

عائلة المراجعة: F074 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الشهور تقويمية، وكل زيارة تدقيق مستقلة. المقارنة تخص خطة السنة المقبلة.
- القرار السابق: يجب إجراء زيارة تدقيق واحدة على الأقل في كل شهر.
- القرار الجديد: تُجرى زيارة في منتصف كل شهر من شهور السنة.
- سبب الإجابة المقترحة: كل شهر يحتوي زيارة.

### English

- Context: Months are calendar months, and each audit visit is separate. The comparison concerns next year's plan.
- Existing decision: At least one audit visit must take place in every month.
- New decision: One visit takes place in the middle of each month of the year.
- Proposed answer rationale: Every month contains a visit.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0231 — customer_service / branch-specific hours

عائلة المراجعة: F069 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الفرعان الشرقي والغربي وحدتان مستقلتان. ساعات العمل كلها محلية لليوم نفسه.
- القرار السابق: يجب أن يبقى مكتب خدمة العملاء في الفرع الشرقي مفتوحًا من 09:00 حتى 17:00.
- القرار الجديد: يُغلق مكتب الخدمة في الفرع الغربي الساعة 15:00 بقية اليوم.
- سبب الإجابة المقترحة: الفرع الغربي خارج نطاق القرار السابق.

### English

- Context: The eastern and western branches are separate units. All hours are local and concern the same day.
- Existing decision: The eastern branch's customer-service desk must remain open from 09:00 until 17:00.
- New decision: The western branch's service desk closes at 15:00 for the rest of the day.
- Proposed answer rationale: The western branch is outside the prior decision's scope.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0232 — leave / explicit exception

عائلة المراجعة: F009 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: كل الطلبات تستوفي شروط الإجازة الأخرى. نوع الإجازة هو العامل الوحيد محل المقارنة.
- القرار السابق: تُمنع الإجازات خلال أسبوع الجرد، باستثناء إجازة الوفاة التي يسمح بها خلاله.
- القرار الجديد: تُمنح إجازة خلال أسبوع الجرد، دون تحديد نوعها.
- سبب الإجابة المقترحة: يلزم نوع الإجازة لمعرفة انطباق الاستثناء.

### English

- Context: All requests satisfy the other leave conditions. Leave type is the only factor under comparison.
- Existing decision: Leave is prohibited during inventory week, except bereavement leave, which is allowed during that week.
- New decision: Leave is granted during inventory week without specifying its type.
- Proposed answer rationale: The leave type is needed to determine whether the exception applies.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0233 — quality / audit frequency

عائلة المراجعة: F074 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الشهور تقويمية، وكل زيارة تدقيق مستقلة. المقارنة تخص خطة السنة المقبلة.
- القرار السابق: يجب إجراء زيارة تدقيق واحدة على الأقل في كل شهر.
- القرار الجديد: تُجرى 12 زيارة في يناير فقط، ولا تُجرى زيارات في بقية السنة.
- سبب الإجابة المقترحة: المجموع السنوي لا يحقق التوزيع الشهري المطلوب.

### English

- Context: Months are calendar months, and each audit visit is separate. The comparison concerns next year's plan.
- Existing decision: At least one audit visit must take place in every month.
- New decision: Twelve visits take place only in January, with none during the rest of the year.
- Proposed answer rationale: The annual total does not satisfy the required monthly distribution.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0234 — inventory / quarantine status

عائلة المراجعة: F080 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الدفعة Q في الحجر الداخلي للفحص، ولا يوجد إشعار إفراج عنها حتى الآن.
- القرار السابق: لا تُستخدم دفعة محجوزة للفحص قبل صدور إشعار الإفراج عنها.
- القرار الجديد: تُستخدم Q الآن لتلبية طلب عاجل رغم عدم صدور الإفراج.
- سبب الإجابة المقترحة: الاستعجال لا يحقق شرط الإفراج السابق.

### English

- Context: Batch Q is in internal inspection quarantine, with no release notice issued yet.
- Existing decision: A batch held for inspection must not be used before a release notice is issued.
- New decision: Q is used now to meet an urgent request despite the absence of release.
- Proposed answer rationale: Urgency does not satisfy the prior-release condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0235 — payroll / bank detail change confirmation

عائلة المراجعة: F090 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: التأكيد المستقل اتصال موثق بالموظف باستخدام رقم معروف سابقًا. رسالة طلب التغيير وحدها ليست تأكيدًا مستقلًا.
- القرار السابق: لا يُفعّل تغيير الحساب البنكي في الرواتب قبل التأكيد المستقل.
- القرار الجديد: يُفعّل التغيير بناءً على رسالة الطلب فقط دون اتصال تحقق.
- سبب الإجابة المقترحة: المصدر الوحيد لا يحقق التأكيد المستقل.

### English

- Context: Independent confirmation is a documented call to the employee using a previously known number. The change-request message alone is not independent confirmation.
- Existing decision: A bank-account change in payroll must not be activated before independent confirmation.
- New decision: The change is activated based only on the request message without a verification call.
- Proposed answer rationale: The sole source does not satisfy independent confirmation.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0236 — customer_service / priority ordering

عائلة المراجعة: F067 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الطلبان مفتوحان وجاهزان للمعالجة، وتوجد قدرة لمعالجة طلب واحد في كل مرة.
- القرار السابق: تُعالج الطلبات الحرجة قبل الطلبات العادية، مهما كان ترتيب وصولها.
- القرار الجديد: يُعالج الطلب X قبل Y، ولا تتوفر درجة أولوية أي منهما.
- سبب الإجابة المقترحة: يلزم تصنيف الطلبين لتحديد ترتيب المعالجة.

### English

- Context: Both requests are open and ready for processing, with capacity to process one at a time.
- Existing decision: Critical requests must be processed before ordinary requests, regardless of arrival order.
- New decision: Request X is processed before Y, and neither priority classification is available.
- Proposed answer rationale: Both requests' classifications are needed to determine processing order.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0237 — customer_service / priority ordering

عائلة المراجعة: F067 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الطلبان مفتوحان وجاهزان للمعالجة، وتوجد قدرة لمعالجة طلب واحد في كل مرة.
- القرار السابق: تُعالج الطلبات الحرجة قبل الطلبات العادية، مهما كان ترتيب وصولها.
- القرار الجديد: يُعالج الطلب الحرج أولًا رغم وصوله لاحقًا.
- سبب الإجابة المقترحة: الترتيب يوافق الأولوية المحددة.

### English

- Context: Both requests are open and ready for processing, with capacity to process one at a time.
- Existing decision: Critical requests must be processed before ordinary requests, regardless of arrival order.
- New decision: The critical request is processed first despite arriving later.
- Proposed answer rationale: The order follows the specified priority.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0238 — customer_service / required notification channel

عائلة المراجعة: F070 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: يُقصد بالإشعار رسالة تصل إلى العميل؛ نشر تحديث داخل ملف الموظف ليس إشعارًا للعميل.
- القرار السابق: يجب إشعار العميل بالإلغاء قبل تنفيذ الإلغاء.
- القرار الجديد: يُنفذ الإلغاء الآن دون إرسال أي إشعار للعميل، ويُحدث الملف الداخلي فقط.
- سبب الإجابة المقترحة: التحديث الداخلي لا يحقق الإشعار السابق للعميل.

### English

- Context: A notification means a message delivered to the customer; an update inside the staff case file is not a customer notification.
- Existing decision: The customer must be notified of cancellation before cancellation is executed.
- New decision: Cancellation is executed now without sending any customer notification; only the internal file is updated.
- Proposed answer rationale: An internal update does not satisfy prior customer notification.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0239 — training / minimum annual hours

عائلة المراجعة: F058 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: السنة التدريبية تنتهي بعد تنفيذ القرار، ولا توجد أنشطة تدريبية أخرى هذا العام.
- القرار السابق: يجب أن يكمل كل موظف 20 ساعة تدريب على الأقل خلال السنة.
- القرار الجديد: تُقفل الخطة بعد دورة إضافية مدتها أربع ساعات، وإجمالي الساعات السابقة غير معلوم.
- سبب الإجابة المقترحة: يلزم الإجمالي السابق لحساب ساعات السنة.

### English

- Context: The training year ends after the decision is carried out, and there are no other training activities this year.
- Existing decision: Every employee must complete at least 20 training hours during the year.
- New decision: The plan is closed after an additional four-hour course, and the previous total is unknown.
- Proposed answer rationale: The previous total is needed to calculate annual hours.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0240 — expenses / duplicate reimbursement

عائلة المراجعة: F022 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الفاتورة I7 صُرفت بالكامل سابقًا. الفاتورة I8 لم تُصرف من قبل.
- القرار السابق: يُمنع سداد المصروف نفسه أكثر من مرة.
- القرار الجديد: يُصرف مبلغ الفاتورة I8 للمرة الأولى.
- سبب الإجابة المقترحة: لا يوجد سداد سابق للمصروف المحدد.

### English

- Context: Invoice I7 has already been reimbursed in full. Invoice I8 has never been reimbursed.
- Existing decision: The same expense must not be reimbursed more than once.
- New decision: The amount of invoice I8 is reimbursed for the first time.
- Proposed answer rationale: There is no previous reimbursement for this expense.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0241 — training / assessment threshold

عائلة المراجعة: F060 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: النجاح يعتمد على الدرجة النهائية من 100، ولا توجد إعفاءات أو درجات إضافية.
- القرار السابق: لا تُمنح شهادة الاجتياز إلا لمن حصل على 80 درجة على الأقل.
- القرار الجديد: تُمنح الشهادة لموظف وُصفت نتيجته بالجيدة دون درجة رقمية أو سلم تحويل.
- سبب الإجابة المقترحة: الوصف اللفظي لا يحدد بلوغ 80.

### English

- Context: Passing depends on the final score out of 100, with no exemptions or additional points.
- Existing decision: A completion certificate may be awarded only to someone scoring at least 80.
- New decision: A certificate is awarded to an employee whose result is described as good, without a numeric score or conversion scale.
- Proposed answer rationale: The verbal description does not establish a score of at least 80.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0242 — procurement / separation of duties

عائلة المراجعة: F020 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: كل رمز موظف يشير إلى شخص مختلف. لا توجد استثناءات لفصل المهام.
- القرار السابق: يجب أن يكون معتمد طلب الشراء شخصًا غير منشئ الطلب.
- القرار الجديد: ينشئ الموظف E1 الطلب ويعتمد الطلب نفسه.
- سبب الإجابة المقترحة: الشخص نفسه يجمع الوظيفتين المتعارضتين.

### English

- Context: Each employee identifier denotes a different person. There are no separation-of-duties exceptions.
- Existing decision: The purchase request approver must be someone other than its creator.
- New decision: Employee E1 creates the request and approves that same request.
- Proposed answer rationale: The same person performs both incompatible duties.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0243 — it_access / shared identity

عائلة المراجعة: F029 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: منصة العمليات تتطلب حساب مستخدم لكل شخص، ولا توجد حسابات مشتركة مستثناة.
- القرار السابق: يُمنع استخدام حساب مستخدم واحد بواسطة أكثر من موظف.
- القرار الجديد: يستخدم جميع موظفي الوردية الحساب نفسه وكلمة مروره.
- سبب الإجابة المقترحة: عدة موظفين يستخدمون هوية دخول واحدة.

### English

- Context: The operations platform requires a user account for each person, with no exempt shared accounts.
- Existing decision: More than one employee must not use the same user account.
- New decision: All shift employees use the same account and password.
- Proposed answer rationale: Multiple employees use one login identity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0244 — quality / alternative evidence routes

عائلة المراجعة: F075 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الوثيقتان A وB بديلتان مقبولتان، ولا توجد شروط إثبات أخرى لهذه الخطوة.
- القرار السابق: يجوز إغلاق الملاحظة بتقرير اختبار A أو بشهادة مطابقة B؛ لا يجوز إغلاقها دون أحدهما.
- القرار الجديد: تُغلق الملاحظة بشهادة B فقط دون تقرير A.
- سبب الإجابة المقترحة: أحد البديلين يكفي وفق القاعدة.

### English

- Context: Documents A and B are acceptable alternatives, with no other evidence conditions for this step.
- Existing decision: A finding may be closed with either test report A or conformity certificate B; it must not be closed without one of them.
- New decision: The finding is closed with certificate B alone, without report A.
- Proposed answer rationale: Either alternative is sufficient under the rule.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0245 — facilities / room capacity

عائلة المراجعة: F046 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: القاعة H تسع 40 شخصًا كحد أقصى، ويشمل العدد المشاركين والمنظمين.
- القرار السابق: يُمنع تجاوز سعة القاعة H أثناء أي نشاط.
- القرار الجديد: يحضر النشاط في H عدد 36 مشاركًا وأربعة منظمين في الوقت نفسه.
- سبب الإجابة المقترحة: المجموع 40 ويساوي السعة المسموحة.

### English

- Context: Room H holds at most 40 people, counting both participants and organizers.
- Existing decision: Room H's capacity must not be exceeded during any event.
- New decision: An event in H has 36 participants and four organizers present simultaneously.
- Proposed answer rationale: The total is 40, equal to the allowed capacity.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0246 — recruitment / recognized equivalence

عائلة المراجعة: F082 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: لأغراض هذه الوظيفة فقط، الشهادة B معادلة صراحة للشهادة A، والشهادة C ليست معادلة لها.
- القرار السابق: يجب امتلاك الشهادة A أو ما يعادلها المعتمد للتعيين في الوظيفة.
- القرار الجديد: يُعيّن مرشح بشهادة D فقط، وحالة معادلتها غير مذكورة.
- سبب الإجابة المقترحة: يلزم تحديد هل D معادل معتمد.

### English

- Context: For this position only, certificate B is explicitly equivalent to A, while certificate C is not equivalent.
- Existing decision: Appointment to the position requires certificate A or an approved equivalent.
- New decision: A candidate holding only certificate D is appointed, and its equivalence status is unspecified.
- Proposed answer rationale: It is necessary to know whether D is an approved equivalent.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0247 — leave / consecutive duration

عائلة المراجعة: F007 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحد يطبق على كل فترة إجازة متصلة. الفترات المذكورة لا تتضمن انقطاعًا.
- القرار السابق: الحد الأقصى للإجازة المتصلة هو 12 يومًا تقويميًا.
- القرار الجديد: تُمدد الإجازة المتصلة يومين إضافيين؛ مدتها السابقة غير محددة.
- سبب الإجابة المقترحة: يلزم طول الفترة السابقة لحساب الإجمالي.

### English

- Context: The limit applies to each continuous leave period. The stated periods have no interruption.
- Existing decision: The maximum continuous leave period is 12 calendar days.
- New decision: The continuous leave is extended by two days; its previous duration is unspecified.
- Proposed answer rationale: The previous period length is needed to calculate the total.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0248 — logistics / vehicle allocation overlap

عائلة المراجعة: F093 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المركبة V واحدة، والمهمتان تتطلبانها طوال مدتيهما. فترات الاستخدام تستثني وقت النهاية.
- القرار السابق: تُخصص V حصريًا للمهمة A من 13:00 إلى 15:00 في اليوم المحدد.
- القرار الجديد: تُخصص V للمهمة B في اليوم نفسه دون تحديد مدتها أو وقتها.
- سبب الإجابة المقترحة: يلزم جدول المهمة B لتحديد التداخل.

### English

- Context: There is one vehicle V, and both missions require it throughout their durations. Usage intervals exclude their end time.
- Existing decision: V is allocated exclusively to mission A from 13:00 to 15:00 on the specified day.
- New decision: V is allocated to mission B on the same day without specifying its time or duration.
- Proposed answer rationale: Mission B's schedule is needed to determine overlap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0249 — procurement / emergency exemption

عائلة المراجعة: F019 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المراجعة العادية تتطلب مناقصة. الإعفاء الوحيد هو إعلان طوارئ رسمي لهذه المشتريات.
- القرار السابق: تُجرى مناقصة قبل الشراء، ويجوز الشراء المباشر عند وجود إعلان الطوارئ المحدد.
- القرار الجديد: يُنفذ شراء مباشر دون مناقصة لأن الطلب عاجل، دون بيان وجود إعلان رسمي.
- سبب الإجابة المقترحة: الاستعجال وحده لا يبين وجود الإعلان المطلوب.

### English

- Context: Ordinary review requires a tender. The only exemption is an official emergency declaration covering these purchases.
- Existing decision: A tender must precede the purchase; direct purchasing is allowed when the specified emergency declaration exists.
- New decision: A direct purchase is executed without a tender because it is urgent, without stating whether an official declaration exists.
- Proposed answer rationale: Urgency alone does not establish the required declaration.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0250 — finance / budget balance

عائلة المراجعة: F041 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المتبقي المتاح في بند الصيانة 7000 وحدة، ولا يسمح بتحويل مبالغ إليه ضمن هذه الحالات.
- القرار السابق: يُمنع اعتماد التزامات مالية تتجاوز الرصيد المتاح للبند.
- القرار الجديد: يُعتمد التزام صيانة جديد بقيمة 6500 وحدة من هذا البند.
- سبب الإجابة المقترحة: الالتزام ضمن الرصيد المتاح.

### English

- Context: The maintenance budget has 7000 units available, and no transfers into it are permitted in these cases.
- Existing decision: Financial commitments exceeding the budget line's available balance must not be approved.
- New decision: A new maintenance commitment of 6500 units is approved against this budget line.
- Proposed answer rationale: The commitment is within the available balance.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0251 — inventory / safety stock

عائلة المراجعة: F076 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المخزون الحالي 60 وحدة، ولا توجد توريدات خلال الفترة المقصودة.
- القرار السابق: يجب ألا ينخفض المخزون المتبقي عن 20 وحدة.
- القرار الجديد: تُصرف دفعة فورًا دون تحديد عدد وحداتها.
- سبب الإجابة المقترحة: يلزم حجم الصرف لحساب المخزون المتبقي.

### English

- Context: Current stock is 60 units, with no deliveries during the period concerned.
- Existing decision: Remaining stock must not fall below 20 units.
- New decision: A batch is issued immediately without specifying its unit count.
- Proposed answer rationale: The issue quantity is needed to calculate remaining stock.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0252 — travel / report deadline

عائلة المراجعة: F015 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المقارنة تخص موعد تسليم تقرير المهمة النهائي، محسوبًا بعد العودة بالأيام التقويمية.
- القرار السابق: يجب تسليم التقرير خلال خمسة أيام بعد العودة، ويشمل ذلك اليوم الخامس.
- القرار الجديد: يُسلّم التقرير في اليوم الخامس بعد العودة.
- سبب الإجابة المقترحة: التسليم عند الحد المشمول بالمهلة.

### English

- Context: The comparison concerns submission of the final mission report, measured in calendar days after return.
- Existing decision: The report must be submitted within five days after return, including day five.
- New decision: The report is submitted on the fifth day after return.
- Proposed answer rationale: Submission is at the included deadline boundary.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0253 — projects / two independent limits

عائلة المراجعة: F098 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الزيادة تقاس مقابل الميزانية الأساسية 100000 وحدة. التأخير يقاس بالأيام التقويمية.
- القرار السابق: يُسمح بالتغيير فقط إذا لم يزد التكلفة بأكثر من 5% ولم يؤخر الموعد بأكثر من ثلاثة أيام.
- القرار الجديد: يُعتمد تغيير يزيد التكلفة 4000 وحدة، وأثره على الموعد غير مقدر.
- سبب الإجابة المقترحة: يلزم أثر الجدول لتقييم الشرط الثاني.

### English

- Context: The increase is measured against a base budget of 100000 units. Delay is measured in calendar days.
- Existing decision: A change is allowed only if it increases cost by no more than 5% and delays the deadline by no more than three days.
- New decision: A change adding 4000 units is approved, and its effect on the deadline has not been estimated.
- Proposed answer rationale: The schedule impact is needed to assess the second condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0254 — finance / reporting period scope

عائلة المراجعة: F044 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: بند Q1 يخص الربع الأول وبند Q2 الربع الثاني، والفترتان غير متداخلتين.
- القرار السابق: تُمنع أي مصروفات جديدة على بند Q1 بعد إقفاله.
- القرار الجديد: يُسجل مصروف جديد على Q2 المفتوح بعد إقفال Q1.
- سبب الإجابة المقترحة: الحظر على Q1 لا يمتد إلى Q2 المفتوح.

### English

- Context: Budget line Q1 covers the first quarter and Q2 the second quarter; the periods do not overlap.
- Existing decision: New expenses against Q1 are prohibited after it is closed.
- New decision: A new expense is posted against open Q2 after Q1 closes.
- Proposed answer rationale: The Q1 restriction does not extend to open Q2.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0255 — logistics / segregated storage

عائلة المراجعة: F094 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الفئتان X وY يجب فصلهما إداريًا لمنع خلط الجرد، دون افتراض خطر مادي.
- القرار السابق: يُمنع وضع أصناف X وY داخل الحاوية نفسها.
- القرار الجديد: توضع X في حاوية وY في حاوية أخرى داخل الغرفة نفسها.
- سبب الإجابة المقترحة: الحظر يخص الحاوية المشتركة، لا الغرفة المشتركة.

### English

- Context: Categories X and Y must be separated administratively to prevent inventory mix-ups; no physical hazard is assumed.
- Existing decision: Items from X and Y must not be placed in the same container.
- New decision: X is placed in one container and Y in another within the same room.
- Proposed answer rationale: The prohibition concerns a shared container, not a shared room.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0256 — expenses / per-person versus total

عائلة المراجعة: F023 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الوجبة لخمسة مشاركين، وتقسم التكلفة بالتساوي. المبالغ شاملة كل الرسوم.
- القرار السابق: الحد الأقصى لمصروف الوجبة 100 وحدة لكل مشارك.
- القرار الجديد: تُعتمد تكلفة وجبة أخرى قيمتها 600 وحدة؛ عدد المشاركين فيها غير محدد.
- سبب الإجابة المقترحة: يلزم عدد المشاركين لحساب التكلفة للفرد.

### English

- Context: The meal is for five participants, with cost divided equally. Amounts include all charges.
- Existing decision: The meal expense cap is 100 units per participant.
- New decision: Another meal costing 600 units is approved; its participant count is unspecified.
- Proposed answer rationale: The participant count is needed to calculate the per-person cost.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0257 — payroll / allowance effective interval

عائلة المراجعة: F086 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: البدل الشهري كان 300 وحدة حتى نهاية يونيو، وأصبح 400 من أول يوليو بقرار إحلال صريح. لا يطبق بأثر رجعي.
- القرار السابق: يُحسب بدل يونيو بـ300 وحدة وبدل يوليو بـ400 وحدة للموظف نفسه.
- القرار الجديد: يُحسب بدل يوليو بـ400 وحدة.
- سبب الإجابة المقترحة: القيمة تطابق الفترة التي بدأ فيها سريانها.

### English

- Context: The monthly allowance was 300 units through June and becomes 400 from July 1 under an explicit replacement decision. It is not retroactive.
- Existing decision: The same employee's June allowance is 300 units and July allowance is 400 units.
- New decision: July's allowance is calculated as 400 units.
- Proposed answer rationale: The amount matches the period in which it became effective.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0258 — recruitment / conflict of interest recusal

عائلة المراجعة: F083 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: عضو اللجنة M قريب للمرشح A وفق تعريف القرابة المعتمد. العضو N ليس قريبًا له.
- القرار السابق: يجب امتناع عضو لجنة التوظيف عن تقييم أي مرشح تربطه به القرابة المحددة.
- القرار الجديد: يتولى M تقييم المرشح A وإعطاءه الدرجة النهائية.
- سبب الإجابة المقترحة: المقيّم تربطه القرابة التي توجب الامتناع.

### English

- Context: Panel member M is related to candidate A under the adopted relationship definition. Member N is not related to A.
- Existing decision: A hiring-panel member must abstain from evaluating a candidate with the specified family relationship.
- New decision: M evaluates candidate A and assigns the final score.
- Proposed answer rationale: The evaluator has the relationship requiring abstention.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0259 — projects / finish-to-start dependency

عائلة المراجعة: F096 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الاختبار A والنشر B مرحلتان منفصلتان. اكتمال A حدث محدد وليس مجرد بدء اختباره.
- القرار السابق: لا يبدأ النشر B إلا بعد اكتمال الاختبار A بنجاح.
- القرار الجديد: يبدأ B بعد تسجيل اكتمال A بنجاح.
- سبب الإجابة المقترحة: الترتيب يحقق الاعتماد بين المرحلتين.

### English

- Context: Testing A and deployment B are separate stages. Completion of A is a specific event, not merely the start of testing.
- Existing decision: Deployment B must not start until testing A has been completed successfully.
- New decision: B starts after successful completion of A is recorded.
- Proposed answer rationale: The sequence satisfies the dependency between stages.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0260 — procurement / approved suppliers

عائلة المراجعة: F018 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: السجل الحالي يحدد المورد P معتمدًا والمورد Q غير معتمد. حالة المورد Z غير متاحة.
- القرار السابق: لا يُصدر أمر شراء إلا لمورد معتمد في السجل الحالي.
- القرار الجديد: يُصدر أمر شراء للمورد P.
- سبب الإجابة المقترحة: المورد مدرج بوصفه معتمدًا.

### English

- Context: The current register lists supplier P as approved and supplier Q as unapproved. Supplier Z's status is unavailable.
- Existing decision: A purchase order may be issued only to a supplier approved in the current register.
- New decision: A purchase order is issued to supplier P.
- Proposed answer rationale: The supplier is listed as approved.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0261 — payroll / aggregate deduction ceiling

عائلة المراجعة: F089 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: هذه قاعدة داخلية افتراضية للاختبار. الراتب الأساسي 5000 وحدة، والحد يشمل مجموع الخصومات المذكورة.
- القرار السابق: لا يتجاوز مجموع هذه الخصومات 10% من الراتب الأساسي في الشهر.
- القرار الجديد: يُطبق خصمان في الشهر نفسه، كل منهما 300 وحدة، ولا خصومات أخرى.
- سبب الإجابة المقترحة: المجموع 600 أكبر من الحد 500.

### English

- Context: This is a fictional internal test rule. Basic salary is 5000 units, and the cap covers the total of the stated deductions.
- Existing decision: The total of these deductions must not exceed 10% of monthly basic salary.
- New decision: Two deductions of 300 units each are applied in the same month, with no other deductions.
- Proposed answer rationale: The total of 600 exceeds the cap of 500.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0262 — training / prerequisite completion

عائلة المراجعة: F056 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الدورة المتقدمة T تتطلب إكمال الأساسيات. التسجيل في الأساسيات وحده لا يعد إكمالًا.
- القرار السابق: لا يبدأ الموظف الدورة T قبل إكمال دورة الأساسيات.
- القرار الجديد: يبدأ الموظف T، وسجل إكمال الأساسيات غير متاح.
- سبب الإجابة المقترحة: يلزم التحقق من إكمال الدورة السابقة.

### English

- Context: Advanced course T requires completion of the basics. Merely enrolling in the basics does not count as completion.
- Existing decision: An employee must not start course T before completing the basics course.
- New decision: The employee starts T, and the basics completion record is unavailable.
- Proposed answer rationale: Prior-course completion must be established.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0263 — information_security / removable media exception

عائلة المراجعة: F034 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: حالة وحدة USB A مشفرة ومعتمدة، ووحدة B غير مشفرة. حالة C غير موثقة.
- القرار السابق: لا تُنسخ ملفات العمل إلى وحدات USB إلا إذا كانت مشفرة ومعتمدة معًا.
- القرار الجديد: تُنسخ ملفات العمل إلى A.
- سبب الإجابة المقترحة: الوحدة تحقق التشفير والاعتماد معًا.

### English

- Context: USB drive A is encrypted and approved; drive B is unencrypted. C's status is undocumented.
- Existing decision: Work files may be copied to USB drives only if the drives are both encrypted and approved.
- New decision: Work files are copied to A.
- Proposed answer rationale: The drive meets both encryption and approval conditions.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0264 — recruitment / anonymous screening stage

عائلة المراجعة: F084 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الفرز الأولي يسبق المقابلات. أسماء المرشحين محجوبة في الفرز ومسموحة للمقابلين عند المقابلة.
- القرار السابق: تُحجب أسماء المرشحين عن المقيمين أثناء الفرز الأولي فقط.
- القرار الجديد: تُعرض الأسماء على المقابلين عند بدء المقابلات بعد انتهاء الفرز.
- سبب الإجابة المقترحة: مرحلة المقابلات خارج الحجب المحدد ومسموح فيها الكشف.

### English

- Context: Initial screening precedes interviews. Candidate names are hidden during screening and available to interviewers at interview time.
- Existing decision: Candidate names must be hidden from assessors during initial screening only.
- New decision: Names are shown to interviewers when interviews start after screening ends.
- Proposed answer rationale: Interviews are outside the specified anonymity stage and disclosure is allowed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0265 — training / delivery modality exception

عائلة المراجعة: F059 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الوحدة P عملية وتتطلب معدات فعلية، والوحدة T نظرية. نوع الوحدة X غير موثق.
- القرار السابق: تُقدم الوحدات العملية حضوريًا فقط، ويجوز تقديم الوحدات النظرية عن بعد.
- القرار الجديد: تُقدم الوحدة X كاملة عن بعد.
- سبب الإجابة المقترحة: يلزم تحديد نوع الوحدة X.

### English

- Context: Module P is practical and requires physical equipment; module T is theoretical. Module X's type is undocumented.
- Existing decision: Practical modules must be delivered in person only; theoretical modules may be delivered remotely.
- New decision: Module X is delivered entirely remotely.
- Proposed answer rationale: Module X's type is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0266 — logistics / delivery identity

عائلة المراجعة: F091 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المستلم المعين للشحنة هو A. تسليم الشحنة لشخص آخر يتطلب تفويضًا مكتوبًا من A.
- القرار السابق: لا تُسلم الشحنة إلا إلى A أو شخص يحمل تفويضًا مكتوبًا منه.
- القرار الجديد: تُسلم الشحنة إلى B، دون بيان وجود تفويض مكتوب.
- سبب الإجابة المقترحة: يلزم التحقق من وجود التفويض.

### English

- Context: The shipment's designated recipient is A. Delivery to another person requires written authorization from A.
- Existing decision: The shipment may be delivered only to A or a person carrying written authorization from A.
- New decision: The shipment is delivered to B without stating whether written authorization exists.
- Proposed answer rationale: The existence of authorization must be established.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0267 — leave / explicit exception

عائلة المراجعة: F009 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: كل الطلبات تستوفي شروط الإجازة الأخرى. نوع الإجازة هو العامل الوحيد محل المقارنة.
- القرار السابق: تُمنع الإجازات خلال أسبوع الجرد، باستثناء إجازة الوفاة التي يسمح بها خلاله.
- القرار الجديد: تُمنح إجازة سياحية خلال أسبوع الجرد.
- سبب الإجابة المقترحة: الإجازة السياحية ليست ضمن الاستثناء المحدد.

### English

- Context: All requests satisfy the other leave conditions. Leave type is the only factor under comparison.
- Existing decision: Leave is prohibited during inventory week, except bereavement leave, which is allowed during that week.
- New decision: Vacation leave is granted during inventory week.
- Proposed answer rationale: Vacation leave is outside the stated exception.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0268 — procurement / approved suppliers

عائلة المراجعة: F018 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: السجل الحالي يحدد المورد P معتمدًا والمورد Q غير معتمد. حالة المورد Z غير متاحة.
- القرار السابق: لا يُصدر أمر شراء إلا لمورد معتمد في السجل الحالي.
- القرار الجديد: يُصدر أمر شراء للمورد Z.
- سبب الإجابة المقترحة: حالة اعتماد Z غير معلومة.

### English

- Context: The current register lists supplier P as approved and supplier Q as unapproved. Supplier Z's status is unavailable.
- Existing decision: A purchase order may be issued only to a supplier approved in the current register.
- New decision: A purchase order is issued to supplier Z.
- Proposed answer rationale: Z's approval status is unknown.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0269 — procurement / split orders

عائلة المراجعة: F017 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحد هو 8000 وحدة للحاجة الواحدة. الغرض من التقسيم مذكور صراحة عند توفره.
- القرار السابق: يُمنع تقسيم حاجة شرائية واحدة إلى طلبات أصغر بهدف تجاوز مراجعة الحد المالي.
- القرار الجديد: يُقدّم طلب واحد بقيمة 12000 لحاجة واحدة ويخضع للمراجعة.
- سبب الإجابة المقترحة: الحاجة لم تُجزأ لتجاوز الحد.

### English

- Context: The threshold is 8000 units per purchasing need. The purpose of splitting is stated explicitly when available.
- Existing decision: A single purchasing need must not be split into smaller orders to bypass the financial-threshold review.
- New decision: One request worth 12000 is submitted for one need and undergoes review.
- Proposed answer rationale: The need is not split to bypass the threshold.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0270 — logistics / route approval specific scope

عائلة المراجعة: F095 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الطريق A معتمد للشاحنات الثقيلة فقط، والطريق B معتمد للمركبات الخفيفة فقط.
- القرار السابق: يجب أن تسلك كل مركبة الطريق المعتمد لفئتها فقط.
- القرار الجديد: تسلك مركبة خفيفة الطريق B.
- سبب الإجابة المقترحة: الطريق يطابق فئة المركبة.

### English

- Context: Route A is approved only for heavy trucks; route B is approved only for light vehicles.
- Existing decision: Each vehicle must use only the route approved for its category.
- New decision: A light vehicle uses route B.
- Proposed answer rationale: The route matches the vehicle category.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0271 — procurement / approved suppliers

عائلة المراجعة: F018 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: السجل الحالي يحدد المورد P معتمدًا والمورد Q غير معتمد. حالة المورد Z غير متاحة.
- القرار السابق: لا يُصدر أمر شراء إلا لمورد معتمد في السجل الحالي.
- القرار الجديد: يُصدر أمر شراء للمورد Q.
- سبب الإجابة المقترحة: المورد غير معتمد صراحة في السجل.

### English

- Context: The current register lists supplier P as approved and supplier Q as unapproved. Supplier Z's status is unavailable.
- Existing decision: A purchase order may be issued only to a supplier approved in the current register.
- New decision: A purchase order is issued to supplier Q.
- Proposed answer rationale: The supplier is explicitly unapproved in the register.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0272 — expenses / submission window

عائلة المراجعة: F025 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المهلة تقاس بالأيام التقويمية المنقضية بعد تاريخ المصروف. لا توجد إعفاءات.
- القرار السابق: لا تُقبل مطالبة مقدمة بعد أكثر من 30 يومًا من تاريخ المصروف.
- القرار الجديد: تُقبل مطالبة قُدمت بعد 30 يومًا بالضبط.
- سبب الإجابة المقترحة: الحظر يخص أكثر من 30 يومًا.

### English

- Context: The window is measured in elapsed calendar days after the expense date. No exemptions apply.
- Existing decision: A claim submitted more than 30 days after the expense date must not be accepted.
- New decision: A claim submitted exactly 30 days later is accepted.
- Proposed answer rationale: The prohibition applies only beyond 30 days.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0273 — facilities / overlapping reservations

عائلة المراجعة: F047 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحجزان يتطلبان الاستخدام الحصري للقاعة نفسها. الفترات من البداية المشمولة إلى النهاية غير المشمولة.
- القرار السابق: القاعة محجوزة حصريًا للفريق A من 09:00 إلى 10:00 يوم 2030-09-12.
- القرار الجديد: تُحجز القاعة للفريق B لمدة ساعة في اليوم نفسه دون تحديد وقت البداية.
- سبب الإجابة المقترحة: يلزم وقت البداية لمعرفة التداخل.

### English

- Context: Both bookings require exclusive use of the same room. Intervals include their start and exclude their end.
- Existing decision: The room is reserved exclusively for Team A from 09:00 to 10:00 on 2030-09-12.
- New decision: The room is reserved for Team B for one hour that day without a start time.
- Proposed answer rationale: The start time is needed to determine overlap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0274 — customer_service / refund eligibility OR

عائلة المراجعة: F068 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الحالة مستوفية لشروط الاسترداد الأخرى. العيب المثبت والتسليم الخاطئ سببان بديلان.
- القرار السابق: يحق للعميل الاسترداد عند وجود عيب مثبت أو تسليم صنف خاطئ؛ وفي غير ذلك يُرفض الاسترداد.
- القرار الجديد: يُقبل الاسترداد دون بيان وجود عيب مثبت أو تسليم خاطئ.
- سبب الإجابة المقترحة: يلزم معرفة تحقق أحد السببين على الأقل.

### English

- Context: The case satisfies the other refund conditions. A confirmed defect and wrong delivery are alternative qualifying reasons.
- Existing decision: A customer is entitled to a refund for either a confirmed defect or delivery of the wrong item; otherwise a refund is denied.
- New decision: A refund is accepted without stating whether there is a confirmed defect or wrong delivery.
- Proposed answer rationale: It is necessary to know whether at least one qualifying reason is satisfied.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0275 — training / assessment threshold

عائلة المراجعة: F060 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: النجاح يعتمد على الدرجة النهائية من 100، ولا توجد إعفاءات أو درجات إضافية.
- القرار السابق: لا تُمنح شهادة الاجتياز إلا لمن حصل على 80 درجة على الأقل.
- القرار الجديد: تُمنح شهادة الاجتياز لموظف درجته النهائية 79.
- سبب الإجابة المقترحة: الدرجة دون عتبة 80.

### English

- Context: Passing depends on the final score out of 100, with no exemptions or additional points.
- Existing decision: A completion certificate may be awarded only to someone scoring at least 80.
- New decision: A completion certificate is awarded to an employee whose final score is 79.
- Proposed answer rationale: The score is below the threshold of 80.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0276 — expenses / per-person versus total

عائلة المراجعة: F023 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الوجبة لخمسة مشاركين، وتقسم التكلفة بالتساوي. المبالغ شاملة كل الرسوم.
- القرار السابق: الحد الأقصى لمصروف الوجبة 100 وحدة لكل مشارك.
- القرار الجديد: تُعتمد تكلفة الوجبة الإجمالية البالغة 450 وحدة.
- سبب الإجابة المقترحة: حصة الفرد 90 وحدة ضمن الحد.

### English

- Context: The meal is for five participants, with cost divided equally. Amounts include all charges.
- Existing decision: The meal expense cap is 100 units per participant.
- New decision: The meal's total cost of 450 units is approved.
- Proposed answer rationale: Each person's share is 90 units, within the cap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0277 — communications / recommendation versus prohibition

عائلة المراجعة: F064 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: القناة A مفضلة لكنها ليست إلزامية، والقناتان A وB معتمدتان ومتاحتان لهذه الرسائل.
- القرار السابق: يُنصح باستخدام A عند الإمكان، ويظل استخدام B مسموحًا دون موافقة إضافية. يُمنع استخدام أي قناة غير معتمدة.
- القرار الجديد: تُرسل رسالة عبر B رغم توفر A.
- سبب الإجابة المقترحة: التفضيل توصية، واستخدام B مسموح صراحة.

### English

- Context: Channel A is preferred but not mandatory; channels A and B are both approved and available for these messages.
- Existing decision: Use of A is recommended when possible, while B remains allowed without additional approval. Use of any unapproved channel is prohibited.
- New decision: A message is sent through B even though A is available.
- Proposed answer rationale: The preference is advisory, and B is explicitly allowed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0278 — inventory / quarantine status

عائلة المراجعة: F080 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الدفعة Q في الحجر الداخلي للفحص، ولا يوجد إشعار إفراج عنها حتى الآن.
- القرار السابق: لا تُستخدم دفعة محجوزة للفحص قبل صدور إشعار الإفراج عنها.
- القرار الجديد: يُؤجل استخدام Q حتى صدور إشعار الإفراج.
- سبب الإجابة المقترحة: الاستخدام مشروط بتحقق الإفراج.

### English

- Context: Batch Q is in internal inspection quarantine, with no release notice issued yet.
- Existing decision: A batch held for inspection must not be used before a release notice is issued.
- New decision: Use of Q is deferred until a release notice is issued.
- Proposed answer rationale: Use is conditional on release being issued.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0279 — training / assessment threshold

عائلة المراجعة: F060 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: النجاح يعتمد على الدرجة النهائية من 100، ولا توجد إعفاءات أو درجات إضافية.
- القرار السابق: لا تُمنح شهادة الاجتياز إلا لمن حصل على 80 درجة على الأقل.
- القرار الجديد: تُمنح شهادة الاجتياز لموظف درجته النهائية 80.
- سبب الإجابة المقترحة: المساواة تحقق شرط على الأقل.

### English

- Context: Passing depends on the final score out of 100, with no exemptions or additional points.
- Existing decision: A completion certificate may be awarded only to someone scoring at least 80.
- New decision: A completion certificate is awarded to an employee whose final score is 80.
- Proposed answer rationale: Equality satisfies the at-least condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0280 — inventory / quarantine status

عائلة المراجعة: F080 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: الدفعة Q في الحجر الداخلي للفحص، ولا يوجد إشعار إفراج عنها حتى الآن.
- القرار السابق: لا تُستخدم دفعة محجوزة للفحص قبل صدور إشعار الإفراج عنها.
- القرار الجديد: تُستخدم دفعة أخرى R اليوم، وحالة حجزها أو الإفراج عنها غير متاحة.
- سبب الإجابة المقترحة: يلزم تحديد حالة الدفعة R.

### English

- Context: Batch Q is in internal inspection quarantine, with no release notice issued yet.
- Existing decision: A batch held for inspection must not be used before a release notice is issued.
- New decision: Another batch R is used today, and its quarantine or release status is unavailable.
- Proposed answer rationale: Batch R's status is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0281 — meetings / quorum

عائلة المراجعة: F051 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: اللجنة سبعة أعضاء، والحضور يحسب بالأشخاص لا بعدد الأصوات المفوضة.
- القرار السابق: لا يصدر قرار اللجنة إلا بحضور أربعة أعضاء على الأقل.
- القرار الجديد: يصدر قرار اللجنة بحضور ثلاثة أعضاء فقط.
- سبب الإجابة المقترحة: الحضور أقل من النصاب المطلوب.

### English

- Context: The committee has seven members, and attendance counts people rather than delegated votes.
- Existing decision: A committee decision may be issued only with at least four members present.
- New decision: The committee decision is issued with only three members present.
- Proposed answer rationale: Attendance is below the required quorum.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0282 — logistics / segregated storage

عائلة المراجعة: F094 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الفئتان X وY يجب فصلهما إداريًا لمنع خلط الجرد، دون افتراض خطر مادي.
- القرار السابق: يُمنع وضع أصناف X وY داخل الحاوية نفسها.
- القرار الجديد: توضع أصناف X وY معًا في حاوية واحدة مع بطاقات تعريف منفصلة.
- سبب الإجابة المقترحة: اختلاف البطاقات لا يحقق فصل الحاويات.

### English

- Context: Categories X and Y must be separated administratively to prevent inventory mix-ups; no physical hazard is assumed.
- Existing decision: Items from X and Y must not be placed in the same container.
- New decision: X and Y items are placed together in one container with separate labels.
- Proposed answer rationale: Separate labels do not satisfy container separation.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0283 — information_security / storage encryption

عائلة المراجعة: F031 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الملف يحتوي بيانات موظفين سرية. تشفير النقل وحده لا يشفر الملف المخزن.
- القرار السابق: يجب تشفير الملفات السرية عند تخزينها.
- القرار الجديد: يُخزن الملف دون تشفير، مع استخدام اتصال مشفر أثناء رفعه فقط.
- سبب الإجابة المقترحة: تشفير النقل لا يحقق تشفير التخزين.

### English

- Context: The file contains confidential employee data. Transport encryption alone does not encrypt the stored file.
- Existing decision: Confidential files must be encrypted at rest.
- New decision: The file is stored unencrypted, using an encrypted connection only during upload.
- Proposed answer rationale: Transport encryption does not satisfy encryption at rest.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0284 — information_security / incident reporting window

عائلة المراجعة: F033 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المهلة تبدأ عند اكتشاف الحادث وتُحسب بساعات متصلة، بما فيها الليل.
- القرار السابق: يجب الإبلاغ عن الحادث خلال ساعتين من اكتشافه.
- القرار الجديد: يتم أول إبلاغ 12:00، ووقت اكتشاف الحادث غير مسجل.
- سبب الإجابة المقترحة: يلزم وقت الاكتشاف لحساب التأخير.

### English

- Context: The deadline starts at incident discovery and is measured in continuous hours, including overnight.
- Existing decision: An incident must be reported within two hours of discovery.
- New decision: The first report is made at 12:00, and the incident discovery time is unrecorded.
- Proposed answer rationale: The discovery time is needed to calculate the delay.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0285 — payroll / proportional allowance

عائلة المراجعة: F087 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: البدل الكامل 800 وحدة، والموظف يعمل بنصف دوام طوال الشهر.
- القرار السابق: يُصرف البدل بنسبة الدوام فقط؛ نصف الدوام يستحق نصف البدل الكامل.
- القرار الجديد: يُصرف لهذا الموظف بدل 800 وحدة عن الشهر.
- سبب الإجابة المقترحة: المبلغ الكامل يخالف النسبة المطلوبة، وهي 400.

### English

- Context: The full allowance is 800 units, and the employee works half-time throughout the month.
- Existing decision: The allowance is paid strictly in proportion to working fraction; half-time receives half the full allowance.
- New decision: This employee receives an allowance of 800 units for the month.
- Proposed answer rationale: The full amount violates the required proportion, which is 400.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0286 — meetings / voting denominator

عائلة المراجعة: F053 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: اللجنة عشرة أعضاء، والقاعدة تعتمد كامل العضوية حتى عند الغياب.
- القرار السابق: إقرار المقترح يتطلب موافقة أكثر من نصف جميع أعضاء اللجنة.
- القرار الجديد: يُعلن إقرار المقترح بموافقة أغلبية الحاضرين، دون ذكر عددهم أو الأصوات.
- سبب الإجابة المقترحة: أغلبية الحاضرين لا تحدد عدد الموافقين من كامل العضوية.

### English

- Context: The committee has ten members, and the rule uses the entire membership even when some are absent.
- Existing decision: Adopting a proposal requires approval by more than half of all committee members.
- New decision: The proposal is declared adopted by a majority of attendees, without stating attendance or vote counts.
- Proposed answer rationale: A majority of attendees does not establish the approval count across the full membership.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0287 — communications / bilingual simultaneous release

عائلة المراجعة: F062 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الإعلان رسمي، والمطلوب نسختان عربـية وإنجليزية كاملتان. الملخص لا يعد نسخة كاملة.
- القرار السابق: يجب نشر النسختين العربية والإنجليزية من كل إعلان رسمي في الوقت نفسه.
- القرار الجديد: تُنشر النسختان الكاملتان معًا الساعة 14:00 اليوم.
- سبب الإجابة المقترحة: النسختان منشورتان في الوقت نفسه.

### English

- Context: The announcement is official, and full Arabic and English versions are required. A summary is not a full version.
- Existing decision: The Arabic and English versions of every official announcement must be published at the same time.
- New decision: Both full versions are published together at 14:00 today.
- Proposed answer rationale: Both versions are published at the same time.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0288 — projects / two independent limits

عائلة المراجعة: F098 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: الزيادة تقاس مقابل الميزانية الأساسية 100000 وحدة. التأخير يقاس بالأيام التقويمية.
- القرار السابق: يُسمح بالتغيير فقط إذا لم يزد التكلفة بأكثر من 5% ولم يؤخر الموعد بأكثر من ثلاثة أيام.
- القرار الجديد: يُعتمد تغيير يزيد التكلفة 4000 وحدة ويؤخر الموعد خمسة أيام.
- سبب الإجابة المقترحة: التكلفة ضمن الحد لكن التأخير يتجاوز الحد الآخر.

### English

- Context: The increase is measured against a base budget of 100000 units. Delay is measured in calendar days.
- Existing decision: A change is allowed only if it increases cost by no more than 5% and delays the deadline by no more than three days.
- New decision: A change adding 4000 units and delaying the deadline by five days is approved.
- Proposed answer rationale: Cost is within its limit, but delay exceeds the other limit.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0289 — leave / explicit exception

عائلة المراجعة: F009 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: كل الطلبات تستوفي شروط الإجازة الأخرى. نوع الإجازة هو العامل الوحيد محل المقارنة.
- القرار السابق: تُمنع الإجازات خلال أسبوع الجرد، باستثناء إجازة الوفاة التي يسمح بها خلاله.
- القرار الجديد: تُمنح إجازة وفاة خلال أسبوع الجرد.
- سبب الإجابة المقترحة: نوع الإجازة مشمول بالاستثناء الصريح.

### English

- Context: All requests satisfy the other leave conditions. Leave type is the only factor under comparison.
- Existing decision: Leave is prohibited during inventory week, except bereavement leave, which is allowed during that week.
- New decision: Bereavement leave is granted during inventory week.
- Proposed answer rationale: This leave type is covered by the explicit exception.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0290 — records / destruction witnesses

عائلة المراجعة: F040 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: إتلاف السجلات يتطلب حضور شهود فعليين، وتوقيع غائب لا يعد حضورًا.
- القرار السابق: يجب حضور شاهدين على الأقل عند إتلاف السجلات.
- القرار الجديد: يتم الإتلاف بحضور لجنة، ولا يُذكر عدد أعضائها الحاضرين.
- سبب الإجابة المقترحة: يلزم عدد الشهود الحاضرين فعليًا.

### English

- Context: Record destruction requires witnesses to be physically present; an absent person's signature does not count as attendance.
- Existing decision: At least two witnesses must be present during record destruction.
- New decision: Destruction occurs in the presence of a committee, without stating how many members attend.
- Proposed answer rationale: The actual number of witnesses present is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0291 — expenses / receipt requirement

عائلة المراجعة: F021 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: المطالبة تخص وجبة عمل. المستند الإلكتروني الرسمي يعد إيصالًا، وكشف البطاقة وحده لا يعد إيصالًا.
- القرار السابق: لا تُسدد مطالبة الوجبة إلا بوجود إيصال معتمد.
- القرار الجديد: تُسدد المطالبة بإيصال إلكتروني رسمي معتمد.
- سبب الإجابة المقترحة: نوع المستند يحقق الشرط.

### English

- Context: The claim concerns a business meal. An official electronic receipt counts as a receipt; a card statement alone does not.
- Existing decision: A meal claim must not be reimbursed without an accepted receipt.
- New decision: The claim is reimbursed with an accepted official electronic receipt.
- Proposed answer rationale: The document type satisfies the condition.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0292 — projects / explicit authority does not erase conflict

عائلة المراجعة: F100 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: كلا المصدرين مخول بإصدار توجيهات للمشروع P. التوجيه الجديد صادر من جهة أعلى، لكنه لا يتضمن إلغاءً أو استثناءً للتوجيه الساري. نقيّم تعارض المتطلبات، لا أولوية التنفيذ.
- القرار السابق: يجب على المشروع P الاحتفاظ بسجلات الاختبار حتى إقفاله، ويُمنع حذفها قبل الإقفال. هذا التوجيه لا يفرض الاحتفاظ بعد الإقفال.
- القرار الجديد: تأمر الجهة الأعلى بحذف سجلات اختبار P الآن مع بقاء المشروع مفتوحًا.
- سبب الإجابة المقترحة: الحذف والاحتفاظ يتعارضان؛ رتبة المصدر لا تمحو التعارض الدلالي.

### English

- Context: Both issuers are authorized to direct project P. The new directive comes from a higher authority but contains no repeal or exception to the effective directive. Assess requirement conflict, not implementation priority.
- Existing decision: Project P must retain its test records until closure, and deletion before closure is prohibited. This directive imposes no retention requirement after closure.
- New decision: The higher authority orders P's test records deleted now while the project remains open.
- Proposed answer rationale: Deletion and retention conflict; issuer rank does not erase the semantic conflict.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0293 — travel / advance settlement

عائلة المراجعة: F014 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: السلفة السابقة A تخص الموظف نفسه، والسلفة الجديدة B طلب منفصل.
- القرار السابق: لا تُصرف سلفة سفر جديدة قبل إقفال السلفة السابقة محاسبيًا.
- القرار الجديد: تُصرف B اليوم، ولم تُرفق حالة إقفال A.
- سبب الإجابة المقترحة: يلزم التحقق من حالة إقفال السلفة السابقة.

### English

- Context: Previous advance A belongs to the same employee, and new advance B is a separate request.
- Existing decision: A new travel advance must not be paid before the previous advance is closed in the accounts.
- New decision: B is paid today, and A's closure status was not provided.
- Proposed answer rationale: The previous advance's closure status is needed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0294 — expenses / currency conversion

عائلة المراجعة: F024 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الحد بالعملة X. سعر التحويل المعتمد هو وحدة Y واحدة تساوي وحدتين X.
- القرار السابق: يجب ألا يتجاوز إجمالي التعويض 1000 وحدة X بعد التحويل.
- القرار الجديد: يُعوض الموظف بمبلغ 450 وحدة Y.
- سبب الإجابة المقترحة: 450 Y تساوي 900 X ضمن الحد.

### English

- Context: The cap is in currency X. The approved exchange rate is one Y unit equals two X units.
- Existing decision: Total reimbursement must not exceed 1000 X units after conversion.
- New decision: The employee is reimbursed 450 Y units.
- Proposed answer rationale: 450 Y equals 900 X, within the cap.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0295 — attendance / exact start time

عائلة المراجعة: F002 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: المقارنة تخص وردية واحدة للفريق B بتاريخ 2030-05-02. جميع الأوقات محلية.
- القرار السابق: تبدأ وردية الفريق B الساعة 08:00 بالضبط.
- القرار الجديد: تبدأ الوردية نفسها الساعة 09:00 بالضبط.
- سبب الإجابة المقترحة: لا يمكن أن يكون للوردية وقتا بدء مختلفان.

### English

- Context: The comparison concerns one Team B shift on 2030-05-02. All times are local.
- Existing decision: Team B's shift starts at exactly 08:00.
- New decision: The same shift starts at exactly 09:00.
- Proposed answer rationale: The shift cannot have two different exact start times.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0296 — records / original versus copy

عائلة المراجعة: F039 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الأصل الورقي والنسخة الممسوحة سجلان متميزان. إنشاء النسخة لا يلغي وجوب حفظ الأصل.
- القرار السابق: يجب حفظ العقد الورقي الأصلي، ويجوز إنشاء نسخة إلكترونية للاستخدام اليومي.
- القرار الجديد: تُستخدم النسخة الإلكترونية يوميًا مع حفظ الأصل الورقي.
- سبب الإجابة المقترحة: القرار يحقق حفظ الأصل ويسمح باستخدام النسخة.

### English

- Context: The paper original and scanned copy are distinct records. Creating a copy does not waive original retention.
- Existing decision: The original paper contract must be retained; an electronic copy may be created for daily use.
- New decision: The electronic copy is used daily while the paper original is retained.
- Proposed answer rationale: The decision retains the original while using the permitted copy.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0297 — facilities / maintenance closure

عائلة المراجعة: F048 | الإجابة المقترحة: معلومات غير كافية (insufficient_information)

### العربية

- السياق: المبنى N مغلق كامل يوم 2030-10-15. المبنى M مفتوح ومستقل عنه.
- القرار السابق: يُمنع عقد أي اجتماع حضوري داخل N أثناء إغلاقه.
- القرار الجديد: يُعقد الاجتماع ظهر 2030-10-15 في القاعة 4 دون تحديد مبناها.
- سبب الإجابة المقترحة: يلزم تحديد مبنى القاعة.

### English

- Context: Building N is closed throughout 2030-10-15. Building M is open and separate.
- Existing decision: No in-person meeting may be held inside N while it is closed.
- New decision: The meeting is held at noon on 2030-10-15 in Room 4 without identifying its building.
- Proposed answer rationale: The room's building must be identified.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0298 — attendance / prior approval

عائلة المراجعة: F004 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: الموظف R سيؤدي ساعتين إضافيتين مساء اليوم. لا توجد استثناءات من شرط الموافقة.
- القرار السابق: لا يبدأ العمل الإضافي إلا بعد تسجيل موافقة المدير.
- القرار الجديد: يبدأ R العمل الإضافي بعد تسجيل الموافقة؛ وقد سُجلت بالفعل.
- سبب الإجابة المقترحة: شرط الموافقة السابقة متحقق.

### English

- Context: Employee R will work two overtime hours this evening. There are no exceptions to the approval requirement.
- Existing decision: Overtime must not start until the manager's approval is recorded.
- New decision: R starts overtime after approval is recorded; it has already been recorded.
- Proposed answer rationale: The prior-approval condition is satisfied.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0299 — inventory / first-expiring first-out

عائلة المراجعة: F078 | الإجابة المقترحة: تعارض (conflict)

### العربية

- السياق: دفعتا A وB من الصنف نفسه ومتاحتان وصالحتان للصرف في المواعيد المقصودة. تنتهي A في يناير وB في مارس من السنة نفسها.
- القرار السابق: يجب صرف الدفعة الأقرب انتهاءً أولًا ما دامت متاحة وصالحة.
- القرار الجديد: تُصرف B أولًا مع بقاء A متاحة وصالحة.
- سبب الإجابة المقترحة: تم تجاوز الدفعة الأقرب انتهاءً.

### English

- Context: Batches A and B contain the same item and are available and valid for issue at the relevant times. A expires in January and B in March of the same year.
- Existing decision: The earliest-expiring batch must be issued first while it is available and valid.
- New decision: B is issued first while A remains available and valid.
- Proposed answer rationale: The earliest-expiring batch is bypassed.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


## ADM-0300 — procurement / separation of duties

عائلة المراجعة: F020 | الإجابة المقترحة: لا تعارض (no_conflict)

### العربية

- السياق: كل رمز موظف يشير إلى شخص مختلف. لا توجد استثناءات لفصل المهام.
- القرار السابق: يجب أن يكون معتمد طلب الشراء شخصًا غير منشئ الطلب.
- القرار الجديد: ينشئ E1 الطلب ويعتمده E2.
- سبب الإجابة المقترحة: المعتمد شخص مختلف عن المنشئ.

### English

- Context: Each employee identifier denotes a different person. There are no separation-of-duties exceptions.
- Existing decision: The purchase request approver must be someone other than its creator.
- New decision: E1 creates the request and E2 approves it.
- Proposed answer rationale: The approver is different from the creator.

مراجعة بشرية: لم تُجرَ بعد. المراجع: ______ | الحكم المستقل: ______ | ملاحظات: ______


