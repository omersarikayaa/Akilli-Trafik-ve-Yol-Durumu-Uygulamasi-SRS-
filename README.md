Yazılım Gereksinim Dokümanı (SRS)
Akıllı Trafik ve Yol Durumu Uygulaması
1. Ön Söz
Hedef Okuyucu Kitlesi
Bu doküman aşağıdaki paydaşlar için hazırlanmıştır: - Mobil uygulama geliştiricileri (Android / iOS) -
Sistem mimarları ve yazılım mühendisleri - Belediyeler ve akıllı şehir çözümleri birimleri - Harita ve
navigasyon servis sağlayıcıları - Proje yöneticileri ve kalite güvence ekipleri
Versiyon Geçmişi
Versiyon Tarih Yazar Yapılan Değişiklikler
1.0 2026-01-05 Ömer Faruk Sarıkaya İlk sürüm – temel gereksinimler
Yeni Sürüm Oluşturma Gerekçesi
Kullanıcı geri bildirimlerinin değerlendirilmesi, trafik verisinin doğruluğunun artırılması, yeni rota
optimizasyon algoritmalarının eklenmesi ve belediye trafik sistemleriyle entegrasyon ihtiyacı nedeniyle
yeni sürümler planlanmaktadır.
2. Giriş
Sistem Gereksinimi
Büyük şehirlerde artan araç sayısı, yol çalışmaları, kazalar ve hava koşulları trafik yoğunluğunu ciddi
şekilde etkilemektedir. Mevcut navigasyon uygulamaları her zaman güncel ve yerel trafik verisini
yeterince sunamamaktadır. Akıllı Trafik ve Yol Durumu Uygulaması; gerçek zamanlı trafik yoğunluğunu
analiz ederek kullanıcılara en uygun ve alternatif rotaları sunmak amacıyla geliştirilmiştir.
Sistem Fonksiyonları
Gerçek zamanlı trafik yoğunluğu görüntüleme
Kaza, yol çalışması ve kapanan yolların bildirilmesi
Alternatif rota önerileri
Tahmini varış süresi hesaplama
Kullanıcı geri bildirimi ve yol durumu bildirme
Diğer Sistemlerle Entegrasyon
Harita servisleri (Google Maps API, OpenStreetMap)
Belediye trafik sensörleri ve kameraları
Hava durumu servisleri
• 
• 
• 
• 
• 
• 
• 
• 
1
Bildirim servisleri (Push Notification)
İş Hedefleri
Trafik yoğunluğunu azaltmaya katkı sağlamak
Kullanıcıların seyahat süresini kısaltmak
Akıllı şehir projelerine veri desteği sunmak
3. Sözlük
Terim Tanım
Trafik Yoğunluğu Yol üzerindeki araç yoğunluk seviyesi
Alternatif Rota Ana yol dışında önerilen farklı güzergâh
ETA Tahmini varış süresi (Estimated Time of Arrival)
GPS Küresel Konumlama Sistemi
Push Bildirim Anlık kullanıcı uyarısı
Sensör Verisi Trafik sensörlerinden alınan veri
4. Kullanıcı Gereksinimleri Tanımı
Kullanıcı Hizmetleri
Harita üzerinden anlık trafik durumunu görüntüleme
Başlangıç ve varış noktası seçerek rota oluşturma
Alternatif rota seçeneklerini karşılaştırma
Yol kapalı, kaza veya yoğunluk bildirimi alma
Favori yolları ve adresleri kaydetme
Fonksiyonel Olmayan Gereksinimler
Performans: Rota hesaplama süresi maksimum 2 saniye
Güvenilirlik: %99 kesintisiz çalışma
Kullanılabilirlik: Mobil cihazlara uyumlu, sade arayüz
Güvenlik: Konum verileri şifrelenmiş şekilde işlenmelidir
Standartlar: ISO 27001, KVKK uyumluluğu
5. Sistem Mimarisi
Yüksek Seviyeli Mimari
Üç katmanlı mimari yapı kullanılacaktır: 1. Sunum Katmanı: Mobil uygulama (Flutter / React Native) 2.
Uygulama Katmanı: Trafik analiz ve rota hesaplama servisleri 3. Veri Katmanı: Trafik verileri ve
kullanıcı bilgileri
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
2
Yeniden Kullanılan Bileşenler
Harita ve navigasyon SDK’ları
Bildirim servis modülü
Kimlik doğrulama altyapısı
6. Sistem Gereksinimleri Spesifikasyonu
Fonksiyonel Gereksinimler
FR1: Kullanıcı trafik yoğunluğunu harita üzerinden görebilmelidir
FR2: Sistem alternatif rota önermelidir
FR3: Yol durumu değiştiğinde kullanıcı bilgilendirilmelidir
FR4: Tahmini varış süresi dinamik olarak güncellenmelidir
Fonksiyonel Olmayan Gereksinimler
NFR1: Sistem yoğun kullanıcı yükünde çalışabilmelidir
NFR2: Mobil veri kullanımını optimize etmelidir
NFR3: Ölçeklenebilir altyapı kullanılmalıdır
7. Sistem Modelleri
Kullanım Senaryoları
Trafik Durumu Görüntüleme
Rota Oluşturma
Alternatif Rota Seçimi
Bildirim Alma
Veri Akış Modeli (Özet)
Kullanıcı konumu → Trafik verisi analizi → Rota hesaplama → Kullanıcıya sonuç gösterimi
8. Sistem Gelişimi
Varsayımlar
Trafik sensör sayısı zamanla artacaktır
Kullanıcı sayısı arttıkça sunucu kapasitesi ölçeklenecektir
Gelecekteki Geliştirmeler
Yapay zekâ destekli trafik tahmini
Toplu taşıma entegrasyonu
Sürücü alışkanlıklarına göre kişisel rota önerileri
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
• 
3
9. Ekler
Donanım Gereksinimleri
Sunucu: Minimum 8 GB RAM, 4 çekirdek CPU
Mobil Cihaz: Android 10+ / iOS 14+
Veritabanı Gereksinimleri
Kullanıcılar
Trafik Verileri
Rota Kayıtları
10. Dizin
Trafik Yoğunluğu
Alternatif Rota
ETA
GPS
Push Bildirim
