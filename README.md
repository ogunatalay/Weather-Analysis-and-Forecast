# Weather-Analysis-and-Forecast
Seattle Hava Durumu Analizi ve Hava Durumu Tahmini Projesi <br>
🎯 Projenin Amacı:<br>
Bu projede, Seattle şehrine ait hava durumu verilerini analiz etmek ve makine öğrenmesi modelleri kullanarak hava durumu türlerini tahmin etmek amaçlanmıştır. Proje kapsamında veri analizi, veri görselleştirme ve çeşitli makine öğrenmesi algoritmalarının performans karşılaştırması yapılmıştır.

📁 1. Veri Seti İncelemesi ve Ön İşleme <br>
📊 a. Veri Seti Hakkında Genel Bilgi<br>
I. Dosya: seattle-weather.csv
II. Değişkenler:
-date: Tarih bilgisi
- temp_min: Minimum sıcaklık
- temp_max: Maksimum sıcaklık
- precipitation: Yağış miktarı
- wind: Rüzgar hızı
- weather: Hava durumu türü (rain, sun, fog vb.)

🛠️ b. Veri Temizleme ve Hazırlama<br>
Eksik değerler ve tekrar eden satırlar kontrol edildi.<br>
Minimum ve maksimum sıcaklık değerlerine göre uç değer analizleri yapıldı.<br>
Tarih sütunu datetime formatına dönüştürüldü ve yıl ve ay sütunları eklendi.<br>
Gereksiz sütunlar (year, month) veri setinden kaldırıldı.<br>
Weather sütunu sayısal değerlere dönüştürüldü (LabelEncoder kullanılarak).<br>

📊 **2. Veri Analizi ve Görselleştirme** <br>
🌡️ a. Sıcaklık Analizi<br>
Minimum ve Maksimum Sıcaklık Dağılımı: Histogram grafikleri ile sıcaklık değerlerinin dağılımı incelendi.<br>
Yıllara Göre Maksimum ve Minimum Sıcaklık Değişimi: Çizgi grafikleri ile sıcaklıkların yıllara ve aylara göre nasıl değiştiği analiz edildi.<br>

☔ b. Yağış ve Rüzgar Analizi<br>
Yağış Miktarı Dağılımı: Yıllara ve aylara göre yağış miktarı dağılımı incelendi.<br>
Rüzgar Hızı Dağılımı: Rüzgar hızının aylara göre değişimi analiz edildi.<br>

🌤️ c. Hava Durumu Türleri Analizi<br>
Hava durumu türlerinin dağılımı sütun grafiği ve pasta grafiği kullanılarak görselleştirildi.<br>
En sık görülen hava durumu türleri belirlendi.<br>

🤖 **3. Makine Öğrenmesi Modelleri ile Tahmin**<br>

📚 a. Bağımsız ve Bağımlı Değişkenlerin Tanımlanması<br>
Bağımsız Değişkenler (X): temp_min, temp_max, precipitation, wind<br>
Bağımlı Değişken (y): weather (Hava durumu türü, sayısal değerlerle temsil edildi)<br>
🔄 b. Veri Setinin Bölünmesi<br>
Veri seti eğitim ve test setleri olarak ayrıldı:<br>
Eğitim Seti: %80<br>
Test Seti: %20<br>

🛠️ **4. Uygulanan Makine Öğrenmesi Modelleri**
Aşağıdaki algoritmalar hava durumu tahmini için kullanıldı:<br>

- Logistic Regression: Basit ve yorumlanabilir bir model.<br>
- Random Forest Classifier: Birden fazla karar ağacı ile çalışan güçlü bir sınıflandırıcı.<br>
- Gradient Boosting Classifier: Ağaç tabanlı bir yöntem, güçlü ve istikrarlı sonuçlar sağlar.<br>
- KNeighbors Classifier: Komşuluk tabanlı sınıflandırma yöntemi.<br>
- Support Vector Classifier (SVC): Daha karmaşık sınıflandırma sınırları çizebilen algoritma.<br>
- Decision Tree Classifier: Karar ağacı tabanlı sınıflandırıcı.<br>

🧪 c. Model Performans Değerlendirme Metrikleri<br>
Her model için aşağıdaki performans metrikleri hesaplandı:<br>
Accuracy (Doğruluk): Genel doğru tahmin oranı.<br>
F1 Score: Precision ve Recall arasındaki dengeyi ölçer.<br>

🔄 d. Çapraz Doğrulama (Cross-Validation)<br>
Her model 10 katlı çapraz doğrulama (cv=10) ile test edilerek güvenilir doğruluk sonuçları elde edildi.

📈 5. Sonuçların Görselleştirilmesi<br>
Model doğruluk ve F1 skorları grafiklerle gösterildi.<br>
Her modelin performansı karşılaştırmalı olarak sunuldu.<br>

🌍 6. Uygulama Alanları<br>
Hava Durumu Tahmini: Günlük ve haftalık hava durumu türlerinin tahmini.<br>
Tarım: Sıcaklık ve yağış analizlerine dayalı tarımsal planlama.<br>
Şehir Planlaması: Aşırı hava olaylarına karşı önlem alınması.<br>

📝 7. Sonuç<br>
Proje kapsamında hava durumu analizleri yapıldı ve çeşitli makine öğrenmesi algoritmaları kullanılarak tahmin modelleri oluşturuldu.<br>
Random Forest Classifier, diğer modellere kıyasla daha başarılı performans gösterdi.<br>
