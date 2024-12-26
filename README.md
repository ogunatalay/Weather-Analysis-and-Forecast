# Weather-Analysis-and-Forecast
Seattle Hava Durumu Analizi ve Hava Durumu Tahmini Projesi
🎯 Projenin Amacı:
Bu projede, Seattle şehrine ait hava durumu verilerini analiz etmek ve makine öğrenmesi modelleri kullanarak hava durumu türlerini tahmin etmek amaçlanmıştır. Proje kapsamında veri analizi, veri görselleştirme ve çeşitli makine öğrenmesi algoritmalarının performans karşılaştırması yapılmıştır.

📁 1. Veri Seti İncelemesi ve Ön İşleme
📊 a. Veri Seti Hakkında Genel Bilgi
Dosya: seattle-weather.csv
Değişkenler:
date: Tarih bilgisi
temp_min: Minimum sıcaklık
temp_max: Maksimum sıcaklık
precipitation: Yağış miktarı
wind: Rüzgar hızı
weather: Hava durumu türü (rain, sun, fog vb.)

🛠️ b. Veri Temizleme ve Hazırlama
Eksik değerler ve tekrar eden satırlar kontrol edildi.
Minimum ve maksimum sıcaklık değerlerine göre uç değer analizleri yapıldı.
Tarih sütunu datetime formatına dönüştürüldü ve yıl ve ay sütunları eklendi.
Gereksiz sütunlar (year, month) veri setinden kaldırıldı.
weather sütunu sayısal değerlere dönüştürüldü (LabelEncoder kullanılarak).

📊 2. Veri Analizi ve Görselleştirme
🌡️ a. Sıcaklık Analizi
Minimum ve Maksimum Sıcaklık Dağılımı: Histogram grafikleri ile sıcaklık değerlerinin dağılımı incelendi.
Yıllara Göre Maksimum ve Minimum Sıcaklık Değişimi: Çizgi grafikleri ile sıcaklıkların yıllara ve aylara göre nasıl değiştiği analiz edildi.
☔ b. Yağış ve Rüzgar Analizi
Yağış Miktarı Dağılımı: Yıllara ve aylara göre yağış miktarı dağılımı incelendi.
Rüzgar Hızı Dağılımı: Rüzgar hızının aylara göre değişimi analiz edildi.
🌤️ c. Hava Durumu Türleri Analizi
Hava durumu türlerinin dağılımı sütun grafiği ve pasta grafiği kullanılarak görselleştirildi.
En sık görülen hava durumu türleri belirlendi.
🤖 3. Makine Öğrenmesi Modelleri ile Tahmin
📚 a. Bağımsız ve Bağımlı Değişkenlerin Tanımlanması
Bağımsız Değişkenler (X): temp_min, temp_max, precipitation, wind
Bağımlı Değişken (y): weather (Hava durumu türü, sayısal değerlerle temsil edildi)
🔄 b. Veri Setinin Bölünmesi
Veri seti eğitim ve test setleri olarak ayrıldı:
Eğitim Seti: %80
Test Seti: %20

🛠️ 4. Uygulanan Makine Öğrenmesi Modelleri
Aşağıdaki algoritmalar hava durumu tahmini için kullanıldı:

Logistic Regression: Basit ve yorumlanabilir bir model.
Random Forest Classifier: Birden fazla karar ağacı ile çalışan güçlü bir sınıflandırıcı.
Gradient Boosting Classifier: Ağaç tabanlı bir yöntem, güçlü ve istikrarlı sonuçlar sağlar.
KNeighbors Classifier: Komşuluk tabanlı sınıflandırma yöntemi.
Support Vector Classifier (SVC): Daha karmaşık sınıflandırma sınırları çizebilen algoritma.
Decision Tree Classifier: Karar ağacı tabanlı sınıflandırıcı.

🧪 c. Model Performans Değerlendirme Metrikleri
Her model için aşağıdaki performans metrikleri hesaplandı:

Accuracy (Doğruluk): Genel doğru tahmin oranı.
F1 Score: Precision ve Recall arasındaki dengeyi ölçer.
🔄 d. Çapraz Doğrulama (Cross-Validation)
Her model 10 katlı çapraz doğrulama (cv=10) ile test edilerek güvenilir doğruluk sonuçları elde edildi.

📈 5. Sonuçların Görselleştirilmesi
Model doğruluk ve F1 skorları grafiklerle gösterildi.
Her modelin performansı karşılaştırmalı olarak sunuldu.

🌍 6. Uygulama Alanları
Hava Durumu Tahmini: Günlük ve haftalık hava durumu türlerinin tahmini.
Tarım: Sıcaklık ve yağış analizlerine dayalı tarımsal planlama.
Şehir Planlaması: Aşırı hava olaylarına karşı önlem alınması.

📝 7. Sonuç
Proje kapsamında hava durumu analizleri yapıldı ve çeşitli makine öğrenmesi algoritmaları kullanılarak tahmin modelleri oluşturuldu.
Random Forest Classifier, diğer modellere kıyasla daha başarılı performans gösterdi.
