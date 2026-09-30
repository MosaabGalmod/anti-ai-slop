# سجل وسياق المحادثة وتأسيس المشروع (Conversation & Genesis Record)

**معرّف الجلسة (Conversation ID):** `4718c9b0-7afe-42a6-8915-727ad34afd8e`  
**تاريخ الإنشاء:** 30 سبتمبر 2026  
**الموضوع:** مهارة وقواعد مكافحة الابتذال التصميمي للذكاء الاصطناعي (Anti-AI Slop Design Skill)

---

## 1. طلب المستخدم الأصلي (Original User Prompt)

> **User Request:**
>
> Anti-AI Slop Skill/Prompt  
> Paste this at the START of a project, before any UI exists. Keep it in the repo as DESIGN_RULES.md or CLAUDE.md so it applies to every later change. You can paste this as a prompt or hand this file as an .md to treat it as a skill.  
> 
> Prompt: You are building a production web interface. The rules below are constraints, not suggestions. When a rule conflicts with what you were about to generate, the rule wins. The goal is not "avoid a list of things." It is to make a deliberate choice in each place where the default would be decoration. If you remove a banned element and put nothing considered in its place, the result is worse, not better...
>
> [ملخص القواعد: حظر التدرجات البنفسجية، حظر نجوم الـ AI، حظر الإيموجي كعناصر واجهة، حظر الحاويات الملونة للأيقونات، حظر الكلمات التسويقية الرنانة، ضبط أحجام الخطوط وأبعاد المسافات بمضاعفات 4px، والالتزام بقائمة تحقق نهائية من 14 بنداً].
>
> **السؤال:** هاد برومبت بدي افهم شو بيعمل وشو بقدر استفيد منه وهل ممكن اعمله مهارة اضيفه لمهارات التصميم بحيث يعمل تلقائيا مع طلب تصميم أو تعديل اي صفحة؟

---

## 2. التحليل والشرح الفني (Analysis & Value Proposition)

### أ. ما الذي يفعله هذا البرومبت؟
- يكسر الانحياز الإحصائي لنماذج الذكاء الاصطناعي في توليد واجهات الويب (AI Slop).
- يضع قيوداً صارمة (Hard Constraints) تمنع التدرجات الافتراضية، والظلال الوهمية، والأيقونات المحبوسة في مربعات ملونة، والتعبيرات التسويقية المفرطة.
- يفرض منطق الحرفة البشرية الرصينة المشابهة لأسلوب شركات مثل Stripe و Linear و Vercel.

### ب. كيف يستفاد منه؟
1. **المصداقية الفورية:** إزالة "بصمة الـ AI" التي تجعل العملاء ينفرون من المنتجات المصنوعة كقوالب سريعة.
2. **كود أنظف وأخف:** التخلص من تأثيرات الظلال والحركات غير المجدية و wrappers الزائدة.
3. **تكامل كامل مع البساطة وتجنب التعقيد:** متوافق مع فلسفة تقليل الكود (Ponytail / YAGNI).
4. **بوابة جودة حاسمة (Quality Gate):** قائمة تحقق مكونة من 14 نقطة قبل اعتبار أي عمل مكتملاً.

---

## 3. تحويل البرومبت إلى مهارة وحزمة مفتوحة المصدر

- تم تحويل الدليل إلى ملف مهارة موثق `SKILL.md` مع ترويسة YAML متوافقة مع أنظمة الوكلاء الذكية (Antigravity و Claude Code و Cline).
- تم استخراج نسخة مستقلة `DESIGN_RULES.md` لتضمينها في جذور المشاريع كقواعد جاهزة.
- تم تجهيز المستودع للنشر كحزمة مفتوحة المصدر مجانية على GitHub.
- تم تثبيت المهارة محلياً في مجلد مهارات Antigravity العام:  
  `C:\Users\HP\.gemini\config\skills\anti-ai-slop\SKILL.md`

---

## 4. ملفات السجل الخام (Raw Logs)

الملفات الخام لـ JSONL محفوظة في نفس هذا المجلد للرجوع البرمجي:
- `docs/transcript.jsonl`
- `docs/transcript_full.jsonl`
