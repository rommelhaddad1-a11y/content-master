# Rommel Studio

كوبي رايتر وكاتب سكربتات مبني على Claude AI.

## هيكل الملفات

```
content-master/
├── index.html          ← التطبيق الكامل
├── api/
│   └── chat.js         ← Vercel serverless function
├── vercel.json         ← إعدادات Vercel
└── README.md
```

## النشر على Vercel

1. ارفع الملفات على GitHub
2. ادخل [vercel.com](https://vercel.com) وسجّل بـ GitHub
3. اضغط **New Project** → اختر `content-master`
4. أضف Environment Variable: `ANTHROPIC_API_KEY` = مفتاحك
5. اضغط **Deploy**

## ملاحظة

الـ API Key محفوظ على Vercel فقط — ما يظهر بالكود.
