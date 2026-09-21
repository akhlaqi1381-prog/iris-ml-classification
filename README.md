# iris-ml-classification
Iris Classification 🌸

این پروژه رو برای تمرین مباحث Machine Learning و Classification انجام دادم.

هدف این بود که با استفاده از مشخصات یک گل، گونه‌ی اون رو پیش‌بینی کنیم.

دیتاست

دیتاست Iris شامل 150 نمونه است و 3 نوع گل داره:

* Setosa
* Versicolor
* Virginica

برای هر گل هم 4 ویژگی داریم:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

داده‌ها رو به دو بخش تقسیم کردم:

* 80٪ برای آموزش
* 20٪ برای تست

برای اینکه تعداد نمونه‌های هر کلاس در Train و Test متعادل بمونه، از stratify استفاده کردم.

کارهایی که روی داده انجام دادم

اول Features و Target رو از هم جدا کردم.

بعد اسم کلاس‌ها رو با LabelEncoder به عدد تبدیل کردم:

setosa → 0
versicolor → 1
virginica → 2

برای مدل‌هایی که به Scaling نیاز دارن هم از StandardScaler استفاده کردم.

نکته‌ای که توی این پروژه رعایت کردم این بود که scaler فقط روی داده‌های Train آموزش داده بشه و بعد همون scaler برای Test و داده‌های جدید استفاده بشه.

مدل‌هایی که بررسی کردم

برای مقایسه چند مدل مختلف رو امتحان کردم:

* Logistic Regression
* Random Forest
* Gradient Boosting
* MLP Classifier

برای تنظیم پارامترهای مدل‌ها هم از GridSearchCV و Cross-Validation پنج‌تایی استفاده کردم.

نتایج

نتایج روی Test Set:

Model	Test Accuracy
Logistic Regression	96%
Random Forest	96.67%
Gradient Boosting	96.67%
MLP	100%

مدل MLP روی این تقسیم‌بندی از داده‌ها بهترین نتیجه رو داشت و هر 30 نمونه‌ی Test رو درست پیش‌بینی کرد.

البته چون دیتاست Iris کوچک و نسبتاً ساده است، این نتیجه به معنی عملکرد 100 درصدی مدل روی داده‌های جدید در دنیای واقعی نیست.

پیش‌بینی گل جدید

بعد از آموزش مدل، یک تابع نوشتم که میشه با دادن مشخصات یک گل جدید، گونه‌ی اون رو پیش‌بینی کرد.

مثلاً:

predict_zanbagh(5.1, 3.5, 1.4, 0.2)

خروجی:

Predicted species: setosa
setosa: 99.12%
versicolor: 0.87%
virginica: 0.01%

یعنی مدل این نمونه رو setosa تشخیص داده و احتمال تعلقش به هر کلاس رو هم نمایش داده.

چیزهایی که توی این پروژه تمرین کردم

* Train/Test Split
* Label Encoding
* Feature Scaling
* Cross-Validation
* GridSearchCV
* Logistic Regression
* Random Forest
* Gradient Boosting
* MLP
* Accuracy
* Confusion Matrix
* Classification Report
* ROC-AUC
* Predict کردن نمونه‌های جدید

ابزارها

Python
Pandas
NumPy
Scikit-learn
Matplotlib

این پروژه بیشتر برای تمرین Workflow کامل یک پروژه Classification انجام شده و مرحله بعدی می‌خوام همین مباحث رو روی دیتاست‌های واقعی‌تر و بزرگ‌تر پیاده کنم.