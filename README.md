<div align="center">

# 🎓 Kootaab
مشروع كُتّاب (Kootaab) هو منصة تعليم إلكتروني سحابية متعددة المستأجرين (Multi-Tenant SaaS LMS) موجهة لإدارة وتشغيل الأكاديميات التعليمية، والطلاب، والمشرفين.

### Enterprise Skill-Centric eLearning, built for every academy.

A multi-tenant, Skill-Centric eLearning platform for creating and operating branded academy experiences, from public websites and learner study spaces to academy administration and platform operations.

**Created by [ePlusWeb | eLearning Solutions](https://eplusweb.com)** ·
[Github](https://github.com/ePlusWeb-Solutions) · [Kootaab organization](https://github.com/Kootaab/)

[![License](https://img.shields.io/badge/License-Proprietary-red.svg)](https://github.com/Kootaab/Kootaab/edit/main/README.md#-license--proprietary-notice)
[![TypeScript](https://img.shields.io/badge/TypeScript-Strict-blue.svg?logo=typescript&logoColor=white)](https://github.com/Kootaab/Kootaab/edit/main/README.md#%D8%A7%D9%84%D9%85%D8%B9%D8%A7%D9%8A%D9%8A%D8%B1)
[![Next.js](https://img.shields.io/badge/Next.js-App-black.svg?logo=next.js&logoColor=white)](https://github.com/Kootaab/Kootaab/edit/main/README.md#architectural-relationship)
[![Supabase](https://img.shields.io/badge/Supabase-BaaS-3ECF8E.svg?logo=supabase&logoColor=white)](https://github.com/Kootaab/Kootaab/edit/main/README.md#%D8%A7%D9%84%D8%A8%D9%86%D9%8A%D8%A9-%D8%A7%D9%84%D8%AA%D8%AD%D8%AA%D9%8A%D8%A9)
[![Vercel](https://img.shields.io/badge/Hosted%20on-Vercel-black.svg?logo=vercel&logoColor=white)](https://github.com/Kootaab/Kootaab/edit/main/README.md#cloud-hosting)
[![RTL First](https://img.shields.io/badge/RTL-Supported-orange.svg)](https://github.com/Kootaab/Kootaab/edit/main/README.md#%D8%A7%D9%84%D9%85%D8%B9%D8%A7%D9%8A%D9%8A%D8%B1)
[![Vitest](https://img.shields.io/badge/Tested%20with-Vitest-6E9F18.svg?logo=vitest&logoColor=white)](https://github.com/Kootaab/Kootaab/edit/main/README.md#%D8%A7%D9%84%D9%85%D8%B9%D8%A7%D9%8A%D9%8A%D8%B1)
</div>

### Demos 

#### 🎓 Kootaab - **Academy Website** — public-facing academy website and learning content.
  - Example: https://kootaab.vercel.app

#### 🤵🏻 **Study Dashboard** — learner-facing environment.
  - Example: https://kootaab.vercel.app/study/

#### 🔑 **Academy Admin Panel** — academy-level administration and management.
  - Example: https://kootaab.vercel.app/panel/


---
### للأكاديميات والمراكز
- **هويتك الخاصة:** شعارك، ألوانك الخاصة، وحتى رابط موقعك الخاص (مثل `academy.yourbrand.com`).
- **ملكية البيانات:** بيانات طلابك ملك لك وحدك، مع عزل تام للبيانات عن الأكاديميات الأخرى.
- **تحكم كامل في الدخل:** تحصيل مدفوعات مباشر بدون أي عمولات مقتطعة من المنصة (0% عمولة).
- **التوسع:** مبنية على بنية تحتية سحابية (Supabase) تتوسع تلقائياً مع نمو عدد طلابك.

### للمعلمين المستقلين
- **أدوات قوية:** منشئ دورات بالسحب والإفلات، محرر نصوص غني، وإدارة متقدمة للوسائط.
- **تفاعل ومشاركة:** اختبارات، واجبات، شهادات إتمام، وجلسات خاصة (1-to-1).
- **تحليلات:** رؤى تفصيلية حول تقدم الطلاب وأداء المحتوى التعليمي.

### للطلاب
- **تجربة عصرية:** مشغل دورات شبيه بتجربة نتفليكس، لوحة تحكم سريعة، وتصميم متجاوب مع الجوال.
- **تتبع التقدم:** أشرطة تقدم لحظية، استكمال التعلم من حيث توقفت، وشهادات فورية.
- **المعلم الذكي (AI):** مساعد ذكي مدمج (Gemini AI) يقدم مساعدة سياقية أثناء الدروس.

---

## البنية التحتية

النظام مصمم ليكون مرناً ومستداماً وفق احدث المعايير حيث تعتمد المنصة معمارية الحزم المستقلة متعددة المستأجرين (Package-Based Multi-Tenancy)، حيث يتم الفصل الصارم بين:

- طبقة المنصة المركزية (Platform Layer): تشمل التسويق، وإدارة الاشتراكات، وتوليد الأكاديميات (Provisioning)، وحوكمة النظام.
- طبقة حزم الأكاديميات (Academy Packages): بيئات عمل مستقلة لكل أكاديمية تشمل الموقع، وبوابة التعلم، ولوحة الإدارة.
- طبقة البيانات السحابية (Supabase BaaS Layer): قاعدة بيانات موحدة محكومة بسياسات أمان صارمة على مستوى السطر (RLS).
- خادم الخدمات الخارجية (External Services Server): لمعالجة الوسائط، ترميز الفيديو HLS، والبريد التنبيهي، والبث المباشر.


### تفاصيل المعمارية والتطبيقات
كُتّاب (Kootaab) هي منصة سحابية متقدمة لإدارة التعلم بنظام تعدد المستأجرين (Multi-Tenant SaaS LMS)، مصممة لتمكين الأكاديميات والمراكز التعليمية والمحاضرين المستقلين من تشغيل مدارسهم وأكاديمياتهم الرقمية بهوية مستقلة تماماً (White-Label) مع الحفاظ على عزل تام للبيانات، ودون استقطاع أي عمولات على المبيعات (0% Transaction Fees).

## Architectural Principle

**Kootaab separates the Platform Layer from the Academy Application Layer.**

The platform is responsible for **multi-tenant management, provisioning, onboarding, and shared infrastructure**, while each Academy Package provides the actual **website, learning environment, and academy administration interface**.

This separation allows new academies to be provisioned and deployed as independent packages without duplicating the core platform infrastructure.
:
#### التصميم المعماري والمستودعات الأساسية للمنظومة 

### Academy Application Layer
These three interfaces constitute the **Academy Application Layer** and are deployed as an one Package for each Academy instance .

- **🎓 Academy Website** | : الواجهة العامة التسويقية وعرض الدورات الخاصة بكل أكاديمية.
- **📚 Academy Panel** | : لوحة تحكم مديري الأكاديميات والمحاضرين (إدارة الدورات، الفصول، الفواتير، والشهادات).
- **🤵🏻 Student Dashboard** | : بوابة الطالب التعليمية، مشغل الدروس، الاختبارات، والمساعد الذكي.

### Platform Layer 
Each Academy operates within the multi-tenant data architecture while the platform maintains centralized control over tenant provisioning and management.

- **🔑 SuperAdmin Panel** | : إدارة المنصة الشاملة، الاشتراكات، الخطط، والأكاديميات.
- **🎯 Platform Website** | : الموقع التعريفي والتسويقي للمنصة وتسجيل الأكاديميات الجديدة.
- **📝 Documentation** | : التوثيق الفني، معمارية النظام،

### المحركات

- محرك المقررات (Course Builder)
يدعم تقسيم المقررات إلى وحدات (Modules) ودروس (Lessons).
أنواع متعددة للمحتوى: فيديو (HLS/داخلي/خارجي)، محرر نصوص غني، ملفات PDF، واختبارات.

- محرك الاختبارات (Assessment Engine)
إنشاء بنوك أسئلة متنوعة (اختيار من متعدد، صح وخطأ، إجابات مقالية قصيرة).
تصحيح تلقائي فوري وحساب الدرجات والنسب المئوية لإتمام المادة.

- محرك الشهادات (Certificate Engine)
مصمم شهادات مرئي يتيح استبدال المتغيرات (اسم الطالب، الدورة، التاريخ، كود التحقق).
توليد وتصدير ملفات PDF بصيغة A4 Landscape مع أكواد تحقق فريدة.

- نظام المدفوعات (Payment State Machine)
إدارة طلبات الالتحاق والدفع اليدوي (رفع الإيصالات والتحقق الإداري) والدفع الإلكتروني.
يعتمد على معالجة آمنة عبر Supabase Edge Functions.

المساعد الذكي (AI Tutor)
دمج مساعد ذكي قائم على نماذج Google Gemini داخل مشغل الدروس.
تقديم شروحات سياقية وتلخيص محتوى الدرس والإجابة على استفسارات الطلاب.

### المعايير
- دعم العربية (RTL-First): التزام كامل بتخطيط الاتجاه من اليمين لليسار، مع استخدام خط Cairo للعربية وInter للإنجليزية.
- الصرامة البرمجية: اعتماد TypeScript مع التحقق الصارم (strict: true) لضمان خلو النظام من الأخطاء أثناء البناء.
- الاختبارات: استخدام Vitest لاختبار المكونات والوحدات البرمجية مع حد أدنى لنسبة التغطية (Coverage Floors).
- التوثيق ككود (Docs-as-Code): التزامن الدائم بين المخططات البرمجية وتوثيق الـ APIs ونماذج البيانات.

## Architectural Relationship

```text
                         Kootaab Platform
                               │
              ┌────────────────┴────────────────┐
              │                                 │
      Platform Website                  Super Admin Panel
         (Next.js)                         (Admin)
              │                                 │
              └──────────────┬──────────────────┘
                             │
                       Academy Packages
                             │
                 ┌───────────┴───────────┐
                 │                       │
          Academy Website          Study Dashboard
                 │                       │
                 └───────────┬───────────┘
                             │
                     Academy Admin Panel
                             │
              ┌──────────────┴──────────────┐
              │                             │
           Supabase                       Vercel
       Tenant Data Layer             Package Hosting
              │
              │
       External Services Server
       ├── Video Services
       ├── Events / Registration
       ├── Email Services
       └── Other Add-ons
```

### Cloud hosting

Vercel provides the **deployment and hosting layer for Academy Packages**, serving the Next.js applications for individual academies.

### External Services Server

A separate server hosts **add-on and infrastructure services** that are not part of the core Next.js application, such as:

- Video storage and processing
- Events and registration services
- Email services
- Other specialized platform add-ons and background services
---


## About ePlusWeb

[Kootaab](https://github.com/Kootaab/kootaab-platform) is created by [ePlusWeb | eLearning Solutions](https://eplusweb.com). Explore the [Kootaab GitHub organization](https://github.com/Kootaab) for Kootaab projects and the [ePlusWeb GitHub organization](https://github.com/ePlusWeb-Solutions) for related work.


## 📄 License & Proprietary Notice

This codebase and documentation are proprietary software. All rights reserved © 2026 Kootaab. 

---

<p align="center"><strong>Powered by Kootaab an ePlusWeb Education Technology © 2026</strong></p>
