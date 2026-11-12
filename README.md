Why do food orders arrive late, and can we predict it before it happens? 🚚

I just finished an end-to-end data project to answer exactly that.

📊 The data: ~45,000 delivery orders (weather, traffic, courier details, locations)

🧹 Cleaning + feature engineering: distance, order hour, prep time, and a "late order" label

🤖 Three models compared:
• Random Forest: F1 0.84 | ROC-AUC 0.97 ✅
• XGBoost: F1 0.83 | ROC-AUC 0.97
• Logistic Regression: F1 0.71 | ROC-AUC 0.91

💡 What I found:
• Evening hours (7–9 PM) have the highest late rate
• Heavy traffic and bad weather push delivery time up
• Orders with multiple deliveries at once are more likely to be late
• Courier rating is a strong predictor, but it's more likely a result of delays than a cause (a good reminder that correlation is not causation)

📈 I turned the results into an interactive dashboard with data-driven recommendations, like adding couriers before peak hours and adding time buffers in bad weather.

🛠 Stack: Python, Pandas, Scikit-learn, XGBoost, React, Recharts, Framer Motion, Vercel

🔗 Live dashboard: [(https://index-html-j0vyxsrpy-alaaelhadedys-projects.vercel.app/)]

I'd love your feedback, especially from anyone working in logistics or delivery. What would you add?

#DataAnalysis #MachineLearning #Python #DataScience #React #Logistics #Portfolio

الفكرة
شركات التوصيل بتخسر فلوس وعملاء بسبب التأخير. المشروع بيجاوب على سؤالين: إيه العوامل اللي بتسبب تأخر الطلبات؟ وهل نقدر نتوقع الطلب المتأخر قبل ما يحصل؟

البيانات
حوالي 45,000 طلب توصيل من dataset على Kaggle (Gaurav Malik)، فيها الطقس وكثافة المرور وبيانات المندوب والمواقع وزمن التوصيل.

المراحل

التنظيف: معالجة القيم المفقودة والمكررة، وتوحيد التواريخ والأوقات، وحذف الإحداثيات والقيم الشاذة.
Feature Engineering: المسافة بين المطعم والعميل، وساعة الطلب، ويوم الأسبوع، وويك إند، ووقت التحضير.
تعريف التأخير: أي طلب فوق الـ 75 percentile في زمن التوصيل.
EDA: تأثير الزحام والطقس والمدينة والساعة على التأخير.
النمذجة: مقارنة 3 نماذج مع معالجة عدم توازن الفئات (class weights).
Dashboard: أرقام رئيسية ورسومات تفاعلية وتوصيات تلقائية من البيانات.

نتائج النماذج

النموذج	F1	ROC-AUC
Random Forest	0.84	0.97
XGBoost	0.83	0.97
Logistic Regression	0.71	0.91

أهم النتايج

ساعات المساء أعلى نسبة تأخير.
الزحام والطقس السيئ بيزودوا زمن التوصيل.
تقييم المندوب مؤشر قوي، بس غالباً نتيجة للتأخير مش سبب له.

التوصيات الناتجة
زيادة المناديب قبل ساعات الذروة، وتقدير وقت أذكى عند الزحام، وهامش وقت في الطقس السيئ، وحد أقصى للطلبات المتزامنة للمندوب.

الأدوات
Python وPandas وScikit-learn وXGBoost للتحليل والنماذج، وReact وRecharts وFramer Motion للـ Dashboard، وVercel للنشر
