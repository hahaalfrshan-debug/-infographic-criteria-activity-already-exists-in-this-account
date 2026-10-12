<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>تحدي معايير الإنفوجرافيك</title>
<style>
body {
  font-family: Tahoma, Arial, sans-serif;
  background: #f5f0ff;
  color: #30234d;
  text-align: center;
  padding: 15px;
}
.container {
  max-width: 650px;
  margin: auto;
  background: white;
  padding: 25px;
  border-radius: 20px;
  box-shadow: 0 4px 15px #ddd;
}
h1 { color: #7952b3; }
.question {
  background: #f7f3ff;
  padding: 15px;
  margin: 15px 0;
  border-radius: 12px;
  text-align: right;
}
button {
  background: #7952b3;
  color: white;
  border: none;
  padding: 12px 20px;
  border-radius: 10px;
  cursor: pointer;
  font-size: 16px;
  margin: 5px;
}
button:hover { background: #5c3b91; }
label { display: block; margin: 10px 0; cursor: pointer; }
#result {
  font-size: 20px;
  font-weight: bold;
  margin-top: 20px;
}
</style>
</head>
<body>
<div class="container">
<h1>🎨 تحدّي معايير الإنفوجرافيك</h1>
<p>اختبري معلوماتك واكتشفي مدى معرفتك بمعايير تصميم الإنفوجرافيك!</p>
<div style="font-size:55px">🖼️ 🎨 📊</div>
<form id="quiz">
<div class="question">
<strong>1. ما أهم خطوة قبل تصميم الإنفوجرافيك؟</strong>
<label><input type="radio" name="q1" value="0"> اختيار الألوان</label>
<label><input type="radio" name="q1" value="1"> تحديد الهدف وتنظيم المحتوى</label>
<label><input type="radio" name="q1" value="0"> إضافة الصور فقط</label>
</div>
<div class="question">
<strong>2. كيف نختار الألوان المناسبة؟</strong>
<label><input type="radio" name="q2" value="1"> استخدام ألوان متناسقة وواضحة</label>
<label><input type="radio" name="q2" value="0"> استخدام جميع الألوان</label>
<label><input type="radio" name="q2" value="0"> اختيار ألوان متشابهة جدًا مع الخلفية</label>
</div>
<div class="question">
<strong>3. ما مواصفات الخط المناسب؟</strong>
<label><input type="radio" name="q3" value="0"> صغير ومزخرف</label>
<label><input type="radio" name="q3" value="0"> استخدام أنواع كثيرة من الخطوط</label>
<label><input type="radio" name="q3" value="1"> واضح وسهل القراءة</label>
</div>
<div class="question">
<strong>4. ما دور الصور والرموز؟</strong>
<label><input type="radio" name="q4" value="1"> توضيح المعلومات وتسهيل فهمها</label>
<label><input type="radio" name="q4" value="0"> زيادة الزخرفة فقط</label>
<label><input type="radio" name="q4" value="0"> ملء المساحات الفارغة</label>
</div>
<div class="question">
<strong>5. كيف ننظم عناصر الإنفوجرافيك؟</strong>
<label><input type="radio" name="q5" value="0"> توزيعها عشوائيًا</label>
<label><input type="radio" name="q5" value="1"> ترتيبها بتسلسل واضح ومريح للعين</label>
<label><input type="radio" name="q5" value="0"> وضع المعلومات كلها في مكان واحد</label>
</div>
<div class="question">
<strong>6. ماذا نفعل قبل نشر الإنفوجرافيك؟</strong>
<label><input type="radio" name="q6" value="1"> مراجعة المعلومات والتأكد من جودة التصميم</label>
<label><input type="radio" name="q6" value="0"> نشره دون مراجعة</label>
<label><input type="radio" name="q6" value="0"> حذف عنوانه</label>
</div>
<button type="button" onclick="checkAnswers()">اعرضي نتيجتي 🌟</button>
<button type="reset" onclick="document.getElementById('result').innerHTML=''">إعادة المحاولة 🔄</button>
</form>
<div id="result"></div>
</div>
<script>
function checkAnswers() {
  let score = 0;
  for (let i = 1; i <= 6; i++) {
    let answer = document.querySelector('input[name="q' + i + '"]:checked');
    if (!answer) {
      document.getElementById('result').innerHTML =
        '💜 أجيبي عن جميع الأسئلة أولًا!';
      return;
    }
    score += Number(answer.value);
  }
  let message = score === 6
    ? 'ممتازة! أنتِ خبيرة في معايير الإنفوجرافيك 🏆'
    : score >= 4
    ? 'أحسنتِ! لديكِ معرفة جيدة بالمعايير 👏'
    : 'بداية جميلة! راجعي المعايير وحاولي مرة أخرى 💜';
  document.getElementById('result').innerHTML =
    'نتيجتك: ' + score + ' من 6 🎯<br>' + message;
}
</script>
</body>
</html>
