<div align="center">

# ✨ Project Face — مستشارة العناية بالبشرة بالذكاء الاصطناعي ✨
### *AI-Powered Real-Time Interactive Skincare Consultant Powered by Gemini Live*

[![React](https://img.shields.io/badge/React-19.2-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-7.2-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v4-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Gemini Live API](https://img.shields.io/badge/Google_Gemini-Live_Multimodal_API-4285F4?logo=google&logoColor=white)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<br/>

<p align="center">
  <b>«چوليا» خبيرة ومستشارة العناية بالبشرة التفاعلية التي تتحدث معك صوتياً وصورياً بالعامية المصرية وتوجهك لروتين عناية مخصص لبشرتك بدقة فائقة!</b>
</p>

[English Overview](#-english-overview) • [المميزات الرئيسية](#-المميزات-الرئيسية) • [طريقة التشغيل](#-طريقة-التشغيل-والتثبيت) • [معمارية المشروع](#-معمارية-المشروع-project-architecture) • [معاينة التصميم](#-معاينة-الشاشات)

---

</div>

## 📖 نبذة عن المشروع (About the Project)

**Project Face** هو تطبيق ويب تفاعلي ذكي فائق السرعة يعمل كمستشار شخصي للعناية بالبشرة عبر الذكاء الاصطناعي التوليدي الحقيقي (Real-Time Multimodal AI). يستند المشروع إلى نموذج **Gemini Live Multimodal API** (`gemini-2.5-flash-native-audio-preview`) الذي يوفر اتصال WebSocket مباشر ثنائي الاتجاه لنقل الصوت وتحليل الصور والتنقل الذكي الفوري داخل واجهة التطبيق.

تتجسد مستشارة العناية في شخصية افتراضية اسمها **«چوليا»**، تتحدث باللهجة المصرية العامية بطريقة طبيعية ودودة، وتتعرف على جنس المستخدم (ذكر / أنثى) لتكييف الحوار والقواعد اللغوية، وتقوم بفحص ملامح الوجه وحالة البشرة عبر الكاميرا لتقديم منتجات وروتين يومي مخصص.

---

## 🌟 المميزات الرئيسية (Key Features)

- 🎙️ **محادثة صوتية تفاعلية حية (Real-time Bidirectional Audio):**
  - تدفق صوتي مباشر منخفض الكمون (Low-latency Audio Streaming) بمعدل 16kHz PCM مدخل و24kHz مخرج.
  - خوارزمية ذكية لاكتشاف النشاط الصوتي (Voice Activity Detection - VAD) والتوقف التلقائي عند مقاطعة المستخدم للحديث.
- 👁️ **تحليل بصري متقدم للبشرة (Multimodal Vision Skin Diagnosis):**
  - التقاط صورة فورية للوجه عبر كاميرا الويب وإرسالها مشفرة بصيغة Base64 إلى نموذج Gemini Live لفحص المسام، الحبوب، الهالات السوداء، التجاعيد، ونوع البشرة.
- ⚡ **تحكم تلقائي في واجهة المستخدم عبر Function Calling:**
  - النموذج الذكي يستدعي دالة `go_to_next_step` بعد الاستماع لرد المستخدم صوتياً لينتقل التطبيق ذاتياً للسؤال التالي دون الحاجة للضغط على أي أزرار.
- 🗣️ **دعم كامل للهجة المصرية والتخصيص بحسب الجنس (Gender Adaptation):**
  - تخصيص الخطاب تلقائياً بصيغة المذكر أو المؤنث بناءً على اختيار المستخدم لضمان تجربة حوار طبيعية وممتعة.
- 🧴 **توصيات مخصصة بالمنتجات والروتين اليومي:**
  - اقتراح مستحضرات عناية معتمدة مع تفاصيل الاستخدام الصباحي والمسائي وتوقعات التحسن الزمني.
- 📱 **تكامل ومتابعة سريعة عبر الـ QR Code:**
  - إمكانية مسح كود QR أو إدخال رقم الهاتف لمتابعة الروتين عبر تطبيق الهاتف.
- 🎨 **واجهة مستخدم عصرية وأنيقة:**
  - تصميم متجاوب، أنيميشن سلس باستخدام Framer Motion، ومؤثرات صوتية ومرئية لأفاتار ذكي متوهج (`GradientAvatar`) يتفاعل حركياً أثناء الاستماع والتحدث.

---

## 🛠️ التقنيات المستخدمة (Tech Stack)

| التقنية | الاستخدام |
| :--- | :--- |
| **React 19** & **TypeScript** | بناء الواجهة الأمامية والتحكم بحالة التطبيق بنمط قوي وموثوق |
| **Vite 7** | بيئة بناء وتطوير سريعة مع تحديث فوري (HMR) |
| **Tailwind CSS v4** & **Radix UI** | تصميم عصري متجاوب ومكونات واجهة مستخدم متقدمة |
| **Framer Motion** | حركات تفاعلية وانتقالات سلسة بين مراحل الاختبار |
| **@google/genai** | الربط مع واجهة Gemini Live API التفاعلية للوسائط المتعددة |
| **Web Audio API** | معالجة دفق الصوت الحقيقي والـ Buffers و VAD |
| **Wouter** | توجيه مسارات خفيف وسريع داخل التطبيق |

---

## 🚀 طريقة التشغيل والتثبيت (Getting Started)

### المتطلبات الأساسية (Prerequisites)
- تثبيت **Node.js** (الإصدار 18 أو أحدث)
- تثبيت مدير الحزم **npm** أو **pnpm** أو **yarn**
- مفتاح **Gemini API Key** صالح ويدعم Gemini Live API (Google AI Studio)

### 1. استنساخ المستودع (Clone the Repository)
```bash
git clone https://github.com/Omar-0O/project-face.git
cd project-face
```

### 2. تثبيت الحزم والمكتبات (Install Dependencies)
```bash
npm install
```

### 3. إعداد المتغيرات البيئية (Environment Variables)
قم بنسخ ملف `.env.example` إلى ملف `.env`:
```bash
cp .env.example .env
```
افتح ملف `.env` وضع مفتاح الـ API الخاص بك:
```env
VITE_GEMINI_API_KEY=AIzaSy...your_gemini_api_key_here
```

### 4. تشغيل خادم التطوير (Run Development Server)
```bash
npm run dev
```
افتح المتصفح على الرابط الافتراضي: `http://localhost:5173` واسمح للتطبيق بالوصول إلى الميكروفون والكاميرا.

### 5. بناء المشروع للإنتاج (Build for Production)
```bash
npm run build
```

---

## 📂 معمارية المشروع (Project Architecture)

```
project-face/
├── Design/                  # لقطات شاشات وتصاميم الواجهة الأصلية
├── public/                  # الصور الثابتة، الأيقونات، وصور المنتجات
│   ├── products/            # صور منتجات العناية بالبشرة
│   └── custom-qr.png        # باركود المتابعة
├── src/
│   ├── components/          # المكونات المشتركة ومكونات العناية
│   │   ├── skincare/        # مكونات الأفاتار المتوهج، كروت المنتجات، جدول الروتين
│   │   └── ui/              # مكونات Radix UI و Tailwind (الأزرار، التنبيهات، القوائم)
│   ├── hooks/
│   │   ├── use-live-api.ts  # React Hook لإدارة دورة حياة الاتصال الصوتي والبصري بـ Gemini
│   │   └── use-toast.ts     # هوك إدارة الرسائل المنبثقة
│   ├── lib/
│   │   ├── gemini-live.ts   # محرك خدمة Gemini Live (WebSockets, AudioContext, VAD, Tools)
│   │   ├── audio-player.ts  # مشغل تدفق الصوت PCM 24kHz
│   │   └── utils.ts         # أدوات مساعدة وتنسيق الكلاسات
│   ├── pages/
│   │   ├── WelcomePage.tsx     # شاشة الترحيب والتعريف بالخدمة
│   │   ├── GenderSelection.tsx # شاشة تحديد الجنس لضبط سياق الحديث
│   │   ├── SkincareWizard.tsx  # الشاشة الرئيسية الشاملة (الكاميرا، الأسئلة، المنتجات، الروتين)
│   │   └── Home.tsx            # منسق المراحل الرئيسي
│   ├── App.tsx              # نقطة دخول المكونات والتوجيه
│   └── main.tsx             # تهيئة تطبيق React
├── .env.example             # نموذج المتغيرات البيئية
├── package.json             # الحزم والتبعيات
└── vite.config.ts           # إعدادات Vite ومسارات الـ alias
```

---

## 🖼️ معاينة الشاشات (Design & UI Showcase)

<div align="center">
  <table>
    <tr>
      <td align="center"><b>1. ترحيب چوليا (Welcome Stage)</b></td>
      <td align="center"><b>2. اختيار الجنس (Gender Selection)</b></td>
    </tr>
    <tr>
      <td><img src="Design/Desktop - 1.png" width="400" alt="Welcome Page"/></td>
      <td><img src="Design/Desktop - 2.png" width="400" alt="Gender Selection"/></td>
    </tr>
    <tr>
      <td align="center"><b>3. فحص الكاميرا (Camera Skin Scan)</b></td>
      <td align="center"><b>4. الأسئلة الصوتية التفاعلية (Voice Q&A)</b></td>
    </tr>
    <tr>
      <td><img src="Design/Desktop - 3.png" width="400" alt="Camera Capture"/></td>
      <td><img src="Design/Desktop - 4.png" width="400" alt="Q&A Wizard"/></td>
    </tr>
    <tr>
      <td align="center"><b>5. المنتجات المقترحة (Products)</b></td>
      <td align="center"><b>6. الروتين والتعليمات (Skin Routine)</b></td>
    </tr>
    <tr>
      <td><img src="Design/Desktop - 5.png" width="400" alt="Recommended Products"/></td>
      <td><img src="Design/Desktop - 6.png" width="400" alt="Routine Instructions"/></td>
    </tr>
  </table>
</div>

---

## 🌐 English Overview

**Project Face** is a cutting-edge real-time AI skincare consultant web application powered by **Google's Gemini Live Multimodal API**. It introduces **"Julia"**, an interactive AI consultant who communicates fluently in Egyptian Arabic, offering real-time conversational audio advice, visual face analysis via web camera, and automated wizard progression via Gemini function calling.

### Key Highlights:
- **Low-Latency Bidirectional Audio Streaming:** Seamless voice conversation over WebSockets.
- **Multimodal Visual Analysis:** Analyzes facial pores, acne, texture, and fine lines in real time.
- **Dynamic Gender Awareness:** Adapts dialogue grammar and recommendations for both men and women.
- **Automated Workflow with Function Calling:** Automatically transitions through consultation questions as you speak.
- **Tailored Skincare Regimen:** Delivers personalized product recommendations and day/night care schedules.

---

## 👨‍💻 Author & Maintainer

- **Omar** ([@Omar-0O](https://github.com/Omar-0O))

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
