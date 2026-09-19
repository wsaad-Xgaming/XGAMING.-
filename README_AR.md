# X Gaming Server — جاهز للاستضافة المجانية

هذا السيرفر مبني بـ Node.js + Express ومجهز للعمل على Render Free.

## تشغيل محلي
1. ثبّت Node.js.
2. نفّذ `npm install`.
3. ضع `ADMIN_TOKEN` كمتغير بيئة.
4. نفّذ `npm start`.

## استضافة مجانية على Render
1. ارفع هذا المجلد إلى مستودع GitHub خاص بك.
2. افتح Render وأنشئ Web Service من المستودع.
3. اختر خطة Free.
4. Build Command: `npm install`
5. Start Command: `npm start`
6. أضف Environment Variable باسم `ADMIN_TOKEN` وضع قيمة سرية قوية.
7. بعد النشر سيظهر لك رابط مثل `https://xgaming-server.onrender.com`.
8. في التطبيق اجعل `SERVER_API` يساوي `https://xgaming-server.onrender.com/api`.

## فحص السيرفر
افتح `/api/health` في المتصفح. يجب أن يرجع JSON فيه `ok: true` و `status: online`.

ملاحظة: خطة Render المجانية توقف الخدمة بعد 15 دقيقة من عدم وجود طلبات، ثم تعيد تشغيلها عند وصول طلب جديد. كما أن الملفات المحلية مؤقتة؛ لذلك هذا الإصدار مناسب للتجربة، وليس لتخزين بيانات مهمة بشكل دائم.
