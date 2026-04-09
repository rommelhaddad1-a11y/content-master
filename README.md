# Content Master — Romel

مساعد إنتاج المحتوى الشخصي لرومل، مبني على Claude AI.

---

## خطوات النشر (15 دقيقة)

### 1. رفع الملفات على GitHub

1. افتح [github.com](https://github.com) وسجّل دخول
2. اضغط **New Repository**
3. اسمه: `content-master`
4. اختر **Public**
5. اضغط **Create repository**
6. ارفع الملفات الثلاثة:
   - `index.html`
   - `netlify.toml`
   - `netlify/functions/chat.js`

---

### 2. جيب API Key من Anthropic

1. روح على [console.anthropic.com](https://console.anthropic.com)
2. سجّل حساب جديد
3. اضغط **API Keys** → **Create Key**
4. انسخ الـ Key (بدو يبدأ بـ `sk-ant-...`)
5. احفظه بأمان — ما رح تشوفه مرة ثانية

---

### 3. ربط GitHub بـ Netlify

1. روح على [netlify.com](https://netlify.com)
2. سجّل دخول بحساب GitHub
3. اضغط **Add new site** → **Import from GitHub**
4. اختر repo اسمه `content-master`
5. اضغط **Deploy site**

---

### 4. أضف الـ API Key بأمان

1. في Netlify، اضغط على موقعك
2. روح على **Site configuration** → **Environment variables**
3. اضغط **Add a variable**
4. الاسم: `ANTHROPIC_API_KEY`
5. القيمة: الـ Key اللي نسخته
6. اضغط **Save**
7. اضغط **Deploys** → **Trigger deploy** → **Deploy site**

---

### 5. جاهز ✓

رح تحصل على رابط مثل:
`https://content-master-romel.netlify.app`

افتحه من هاتفك — شغّاله كـ Web App كامل.

---

## هيكل الملفات

```
content-master/
├── index.html                  ← التطبيق الكامل
├── netlify.toml                ← إعدادات Netlify
└── netlify/
    └── functions/
        └── chat.js             ← Backend (يخبي الـ API Key)
```

---

## ملاحظة مهمة

الـ API Key محفوظ على Netlify فقط — ما يظهر بالكود ولا على GitHub.
التطبيق آمن للنشر العام.
