📘 Student Scores Prediction Task
🧮 مشروع التنبؤ بدرجات الطلاب
🧠 Objective | الهدف

English:
The goal of this task is to predict students’ scores based on the number of study hours using regression models.
Two models were used and compared:

Linear Regression

Lasso Regression

العربية:
هدف المشروع هو التنبؤ بدرجات الطلاب بناءً على عدد ساعات المذاكرة باستخدام نماذج الانحدار.
تم استخدام ومقارنة نموذجين:

الانحدار الخطي (Linear Regression)

انحدار لاسو (Lasso Regression)

🧹 Data Preparation | تجهيز البيانات

English:

Loaded a dataset with:

hours: number of study hours

score: student score

Cleaned the data by:

Removing zero or negative values

Removing outliers using z-score

Checking for missing values (none found)
After cleaning, 100 valid rows remained.

العربية:

تم تحميل البيانات التي تحتوي على:

hours: عدد ساعات المذاكرة

score: درجة الطالب

تمت عملية التنظيف عن طريق:

إزالة القيم السالبة أو الصفرية

إزالة القيم الشاذة باستخدام z-score

التأكد من عدم وجود بيانات مفقودة
بعد التنظيف، احتوى الملف على 100 صف من البيانات النظيفة.

⚙️ Model Training | تدريب النماذج
🔹 Linear Regression Model | نموذج الانحدار الخطي

English:
A simple linear regression model was trained:

𝑠
𝑐
𝑜
𝑟
𝑒
=
𝑏
0
+
𝑏
1
×
ℎ
𝑜
𝑢
𝑟
𝑠
score=b0+b1×hours

Performance:

MAE: 3.164

RMSE: 3.837

R²: 0.733

العربية:
تم تدريب نموذج انحدار خطي بسيط وفق المعادلة:

𝑠
𝑐
𝑜
𝑟
𝑒
=
𝑏
0
+
𝑏
1
×
ℎ
𝑜
𝑢
𝑟
𝑠
score=b0+b1×hours

النتائج:

متوسط الخطأ المطلق (MAE): 3.164

الجذر التربيعي لمتوسط الخطأ التربيعي (RMSE): 3.837

معامل التحديد (R²): 0.733

🔹 Lasso Regression Model | نموذج انحدار لاسو

English:
Used a pipeline combining:

StandardScaler() for scaling

Lasso(alpha=0.1) for regularization

Performance:

MAE: 3.319

RMSE: 4.060

R²: 0.701

Cross Validation (5-Fold): Avg R² ≈ 0.70 ± 0.03

العربية:
تم استخدام بايبلاين يحتوي على:

StandardScaler() لتوحيد القيم

Lasso(alpha=0.1) لتقليل التأثير الزائد للخصائص (Regularization)

النتائج:

MAE: 3.319

RMSE: 4.060

R²: 0.701

تقييم K-Fold (بخمس تقسيمات): متوسط R² ≈ 0.70 ± 0.03

📊 Results & Analysis | النتائج والتحليل

English:

The Linear Regression model performed slightly better.

Lasso gave slightly lower accuracy but is more stable and helps prevent overfitting.

Both models confirmed a clear positive relationship between hours and scores.

العربية:

نموذج الانحدار الخطي أعطى دقة أعلى نسبيًا.

نموذج لاسو كانت دقته أقل قليلًا، لكنه أكثر استقرارًا ويقلل خطر الـ Overfitting.

كلا النموذجين أظهرا علاقة طردية واضحة بين عدد الساعات والدرجات.

🧩 Next Steps | الخطوات القادمة

English:

Try Polynomial Regression for potential non-linear patterns.

Add more features (e.g., difficulty level, study method).

Tune the alpha parameter in Lasso for optimization.

العربية:

تجربة الانحدار المتعدد (Polynomial Regression) لاكتشاف العلاقات غير الخطية.

إضافة خصائص جديدة (مثل صعوبة المادة أو طريقة المذاكرة).

ضبط قيمة alpha في Lasso للحصول على أفضل أداء.

💻 Technologies Used | التقنيات المستخدمة

Python 🐍

pandas

numpy

scikit-learn

matplotlib / seaborn
