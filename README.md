# 📚 LGS Deneme Takip

<div align="center">

![LGS Deneme Takip](https://img.shields.io/badge/LGS-Deneme%20Takip-4361ee?style=for-the-badge&logo=bookstack&logoColor=white)
![Versiyon](https://img.shields.io/badge/Versiyon-1.0.0-2a9d8f?style=for-the-badge)
![Lisans](https://img.shields.io/badge/Lisans-MIT-e63946?style=for-the-badge)
![Tek Dosya](https://img.shields.io/badge/Tek%20Dosya-HTML-f77f00?style=for-the-badge&logo=html5&logoColor=white)
![Sunucu Gerektirmez](https://img.shields.io/badge/Sunucu-Gerektirmez-06d6a0?style=for-the-badge)

**LGS sınavına hazırlanan öğrenciler için geliştirilmiş, tamamen tarayıcı tabanlı deneme sınavı takip, tahmini puan hesaplama ve gelişim analizi uygulaması.**

*Hiçbir kurulum, sunucu veya kayıt gerektirmez. Aç ve kullan.*

[🚀 Hemen Kullan](#-hızlı-başlangıç) · [📖 Kullanım Kılavuzu](#-kullanım-kılavuzu) · [🔧 Teknik Dokümantasyon](#-teknik-dokümantasyon)

</div>

---

## 📑 İçindekiler

- [Nedir?](#-nedir)
- [Neden Bu Uygulama?](#-neden-bu-uygulama)
- [Özellikler](#-özellikler)
- [Hızlı Başlangıç](#-hızlı-başlangıç)
- [Kullanım Kılavuzu](#-kullanım-kılavuzu)
- [Teknik Dokümantasyon](#-teknik-dokümantasyon)
- [Tarayıcı Desteği](#-tarayıcı-desteği)
- [Bilinen Sınırlamalar](#-bilinen-sınırlamalar)
- [Sıkça Sorulan Sorular](#-sıkça-sorulan-sorular)
- [Yol Haritası](#-yol-haritası)
- [Katkıda Bulunma](#-katkıda-bulunma)
- [Lisans](#-lisans)
- [Sorumluluk Reddi](#-sorumluluk-reddi)

---

## 📖 Nedir?

**LGS Deneme Takip**, Türkiye'deki 8. sınıf öğrencilerinin LGS (Liselere Geçiş Sınavı) deneme sınavı sonuçlarını kaydetmelerini, tahmini LGS puanlarını hesaplamalarını ve zaman içindeki gelişimlerini detaylı grafikler ve analizlerle takip etmelerini sağlayan bir web uygulamasıdır.

Uygulama **tek bir HTML dosyasından** oluşur. Hiçbir backend, veritabanı, framework veya build aracı gerektirmez. Tüm veriler kullanıcının kendi tarayıcısında (localStorage) saklanır ve hiçbir veri dışarıya gönderilmez.

---

## 🤔 Neden Bu Uygulama?

| Problem | Çözüm |
|---------|-------|
| Deneme sonuçları deftere yazılıyor, kaybolabiliyor | 📱 Dijital kayıt, tarayıcıda kalıcı saklama |
| Puan hesaplama karmaşık ve hata yapılabiliyor | 🧮 Otomatik tahmini puan hesaplama |
| Gelişim takibi zor, hangi derste ilerleme var belli değil | 📈 Ders bazlı trend grafikleri ve karşılaştırma |
| Zayıf yönlerin tespiti subjektif kalıyor | 🔍 Veri odaklı analiz ve otomatik tespit |
| Online araçlar kayıt/giriş gerektiriyor | 🔓 Sıfır kayıt, sıfır veri paylaşımı |
| Çoğu araç internet bağlantısı gerektiriyor | 📴 Çevrimdışı çalışma (ilk yüklemeden sonra) |
| Farklı yayınevlerinin soru sayıları değişiyor | ⚙️ Özelleştirilebilir soru sayıları |

---

## ✨ Özellikler

### 📝 Deneme Girişi ve Puan Hesaplama

- **6 ders** için doğru/yanlış/boş giriş tablosu: Türkçe (varsayılan 20 soru), Matematik (varsayılan 20 soru), Fen Bilimleri (varsayılan 20 soru), T.C. İnkılap Tarihi ve Atatürkçülük (varsayılan 10 soru), Din Kültürü ve Ahlak Bilgisi (varsayılan 10 soru), İngilizce (varsayılan 10 soru)
- **Gerçek zamanlı otomatik boş hesaplama**: Doğru ve yanlış girildiğinde kalan boş soru sayısı otomatik güncellenir
- **Tahmini LGS puanı**: Yaygın kullanılan yaklaşık katsayılara dayalı puan hesaplama (100-500 aralığı)
- **Net formülü**: Net = Doğru - (Yanlış / 3), negatif netler otomatik olarak 0'a sabitlenir
- **Deneme bilgileri**: Ad, tarih ve opsiyonel not alanı
- **Kapsamlı form doğrulama**: Boş alan kontrolü (ad ve tarih zorunlu), soru sayısı aşım kontrolü, negatif değer engeli, NaN koruması, eksik toplam otomatik tamamlama (boş olarak)

### 📊 Sonuç Ekranı

- **Ana metrikler**: Tahmini puan, toplam net, toplam doğru/yanlış/boş
- **Ders bazlı detay tablosu**: Her ders için doğru, yanlış, boş, net, yüzde ve renk kodlu görsel bar grafik
- **Karşılaştırma kartları**: Önceki denemeye göre puan farkı (artış yeşil, düşüş kırmızı) ve en iyi denemeye göre puan farkı
- **Trend göstergesi**: Son 3 denemeye dayalı yükseliş, düşüş veya dalgalı trend
- **Bar grafik renklendirme**: %70 ve üzeri yeşil (güçlü), %40-69 mavi (orta), %40 altı kırmızı (geliştirilmeli)
- Özel soru sayısı kullanıldığında bilgilendirme uyarısı

### 📋 Deneme Geçmişi

- Tüm kayıtlı denemelerin kartlar halinde listesi
- **Arama**: İsim, tarih veya nota göre gerçek zamanlı filtreleme
- **6 farklı sıralama seçeneği**: En yeni, en eski, en yüksek puan, en düşük puan, en yüksek net, en düşük net
- **Rozetler**: En iyi puan rozeti (otomatik) ve düzenlenmiş deneme işareti
- **Hızlı eylemler**: Her deneme için Sonuç Gör, Düzenle ve Sil butonları
- Kayıt sayacı: X/100 kayıt formatında gösterim
- Silme onay modalı (yanlışlıkla silmeyi engeller)
- Düzenleme sırasında orijinal oluşturulma tarihi korunur

### 📈 Gelişim Grafikleri

Chart.js v4.4.7 kütüphanesi kullanılır (CDN üzerinden).

- **Puan gelişim grafiği**: Tüm denemelerin tahmini puanlarının zaman serisi
- **Net gelişim grafiği**: Toplam net trendinin görselleştirilmesi
- **Ders bazlı net trendi**: 6 dersin ayrı renklerle karşılaştırmalı çizgi grafiği. Türkçe mavi, Matematik kırmızı, Fen Bilimleri teal, İnkılap Tarihi turuncu, Din Kültürü mor, İngilizce yeşil
- **Grafik türü seçimi**: Çizgi veya çubuk grafik (ayarlardan değiştirilebilir)
- Tema uyumlu: Karanlık/aydınlık temaya göre otomatik grid ve metin rengi adaptasyonu
- **Akıllı Hedef Puan Sistemi**: En az 2 deneme sonrasında aktif olan kişiselleştirilmiş hedef puan önerisi. Ağırlıklı formül: Son 3 ortalama %40, en iyi puan %30, genel ortalama %10, trend projeksiyonu %20. Tavan sınırı en iyi puanın %105'i veya 500, taban sınırı son 3 ortalamanın altına düşmez.

### 🔍 Detaylı Analiz

- **Otomatik ders tespiti**: En güçlü ders (en yüksek ortalama başarı yüzdesi), gelişime açık ders (en düşük ortalama başarı yüzdesi), en çok yanlış yapılan ders
- **Ders bazlı detaylı istatistik tablosu**: Ortalama net, ortalama yüzde, ortalama yanlış, en iyi net, en düşük net, son trend (son iki deneme arası net farkı ve yön)
- **Otomatik değerlendirme kartları**: Güçlü yön analizi (en başarılı dersteki ortalama, yüzde ve en iyi net bilgisi), gelişim alanı tespiti (%50 altı başarı oranı varsa uyarı ve detay), yanlış analizi (en çok yanlış yapılan dersteki yanlıştan kaynaklanan net kaybı hesabı), genel performans değerlendirmesi (450+ Çok İyi, 380+ İyi, 300+ Orta, 300 altı Geliştirilmeli)

### ⚙️ Ayarlar ve Kişiselleştirme

- **Karanlık/Aydınlık Tema**: Tek tıkla geçiş, tercih localStorage'da kalıcı olarak saklanır, tüm bileşenler ve grafiklere yansır
- **12 Vurgu Rengi Seçeneği**: Mavi, açık mavi, mor, pembe, kırmızı, turuncu, teal, yeşil, koyu mavi, lacivert, gri ve koyu turuncu. Tüm butonlar, başlıklar, grafik renkleri ve vurgular seçilen renge uyum sağlar
- **Ders Soru Sayıları Özelleştirmesi**: Her ders için 1-50 arası bağımsız ayarlama, değişiklik anında giriş tablosuna yansır, puan hesaplama otomatik olarak normalize edilir
- **Grafik Türü**: Çizgi veya çubuk seçimi
- Ayarlar paneli sağdan açılan slide-over tasarımı ve overlay ile arka plan karartması

### 💾 Veri Yönetimi

- **JSON Dışa Aktarma**: Tüm deneme ve ayar verilerini tek bir .json dosyasına indirir. Otomatik dosya adlandırma: lgs-deneme-yedek-YYYY-MM-DD.json. Versiyon bilgisi ve dışa aktarma tarihi dahildir.
- **JSON İçe Aktarma**: Yedek dosyasından verileri geri yükler. Ayarlar (tema, renk, soru sayıları) dahil tüm veriler geri gelir. Dosya format doğrulaması ve hata yönetimi içerir. Maksimum 100 deneme sınırı uygulanır.
- **Toplu Silme**: Onay adımıyla korunur. Tüm denemeler ve sonuç ekranı temizlenir, ayarlar korunur.

---

## 🚀 Hızlı Başlangıç

### Yöntem 1: Doğrudan Dosyadan Açma (Önerilen)

Depoyu klonlayın veya ZIP olarak indirin, klasöre girin ve index.html dosyasını tarayıcınızda açın.
Windows'ta start index.html, macOS'ta open index.html, Linux'ta xdg-open index.html komutuyla açabilirsiniz.

Yöntem 2: GitHub Pages Üzerinden
Eğer repoyu GitHub Pages ile yayınladıysanız doğrudan (https://egementoklucu.github.io/LGS/) adresinden erişebilirsiniz.

Yöntem 3: Sadece Dosyayı İndirin
Bu sayfadaki index.html dosyasına tıklayın, "Raw" butonuna tıklayın, sayfayı Ctrl+S veya Cmd+S ile kaydedin ve kaydedilen dosyayı tarayıcınızda açın.

Not: İnternet bağlantısı yalnızca Chart.js CDN'inin ilk yüklemesinde gereklidir. Grafik kütüphanesi tarayıcı tarafından önbelleğe alındıktan sonra çevrimdışı da çalışır (grafikler dahil). Grafikler olmadan temel işlevler tamamen çevrimdışı çalışır.

📖 Kullanım Kılavuzu
1. Yeni Deneme Girişi
"Deneme Gir" sekmesine tıklayın (varsayılan olarak açıktır). Deneme adını yazın (ör: "MEB Denemesi 3", "Kanguru Yayınları #5"). Tarihi seçin (bugünün tarihi otomatik gelir). Her ders için doğru ve yanlış sayısını girin; boş soru sayısı otomatik hesaplanır ve toplam soru sayısını aşamaz. İsterseniz not ekleyin (ör: "Geometri sorularına dikkat"). "Kaydet ve Hesapla" butonuna tıklayın. Otomatik olarak Sonuç sekmesine yönlendirilirsiniz.

2. Sonuçları İnceleme
Tahmini LGS puanınızı ana kartta görün. Ders bazlı netleri tabloda inceleyin. Renk kodlu bar grafiklerle her dersin başarı oranını görselleştirin. Önceki denemeye ve en iyi denemeye göre fark karşılaştırmasını kontrol edin.

3. Geçmişi Yönetme
"Geçmiş" sekmesinde tüm denemelerinizi görün. Arama kutusuna yazarak filtreleme yapın. Sıralama menüsünden istediğiniz sıralamayı seçin. Sonuç Gör butonu ile herhangi bir denemenin detaylı sonucunu tekrar görüntüleyin. Düzenle butonu ile denemeyi düzenleyin (giriş formuna yükler). Sil butonu ile denemeyi silin (onay istenir).

4. Gelişim Takibi
"Gelişim" sekmesinde puan ve net trendlerinizi grafiklerle izleyin. Akıllı hedef puanınızı en üstte görün (2 veya daha fazla deneme gerektirir). Ders bazlı net trendi grafiğinde hangi derste ilerlediğinizi veya gerilediğinizi karşılaştırın. Ayarlardan grafik türünü değiştirerek farklı görselleştirmeler deneyin.

5. Analiz Okuma
"Analiz" sekmesinde veriye dayalı değerlendirmeleri okuyun. En güçlü ve en zayıf derslerinizi görün. Yanlış analizi ile net kaybınızı anlayın. Genel performans kartıyla durumunuzu öğrenin.

6. Ayarları Özelleştirme
Sağ üstteki ayarlar butonuna tıklayın. Vurgu rengini palette tıklayarak değiştirin. Soru sayılarını derslere göre ayarlayın (farklı yayınevleri için). Grafik türünü seçin. Verinizi yedekleyin veya geri yükleyin.

7. Verileri Yedekleme
localStorage verileri tarayıcı temizleme ile silinebilir, bu nedenle düzenli yedek almanız önerilir. Ayarlar panelini açın. "Verileri Dışa Aktar" butonuna tıklayın. İndirilen .json dosyasını güvenli bir yere saklayın. Geri yüklemek için "Verileri İçe Aktar" butonunu kullanın.

🔧 Teknik Dokümantasyon
Mimari
Uygulama tek bir index.html dosyasından oluşur. İçerisinde style etiketi altında CSS değişkenleri (tema sistemi), genel stiller ve bileşenler ile responsive media queries bulunur. Body bölümünde header (logo, tema, ayarlar), ayarlar paneli (slide-over), tab navigasyonu (deneme giriş formu, sonuç ekranı, geçmiş listesi, gelişim grafikleri, analiz paneli) ve silme onay modalı yer alır. Script bölümünde sabitler ve varsayılanlar, veri yönetimi (localStorage), tema ve renk yönetimi, form işlemleri ve doğrulama, puan hesaplama motoru, CRUD işlemleri (deneme), render fonksiyonları, grafik yönetimi (Chart.js), akıllı hedef algoritması, analiz motoru ve import/export işlemleri bulunur. Tek harici bağımlılık Chart.js v4.4.7'dir ve CDN üzerinden yüklenir.

Tasarım kararları: Tek dosya yapısı dağıtım, paylaşım ve kullanım kolaylığı sağlar. Webpack, Vite, npm gibi araçlara ihtiyaç duymaz. Sunucu, API veya veritabanı gerektirmez. Tüm veriler yalnızca kullanıcının tarayıcısında kalır.

Puan Hesaplama Algoritması
Uygulama, LGS'nin gerçek puan hesaplama formülüne yakın bir tahmini katsayı sistemi kullanır. Formül: Puan = BazPuan + Toplam(ÖlçekliNet × Katsayı). Baz puan 194.752082 olarak sabitlenmiştir.

Katsayı Tablosu:

Ders	Katsayı	Varsayılan Soru	Ağırlık
Türkçe	4.3480	20	4
Matematik	4.2538	20	4
Fen Bilimleri	4.1230	20	4
T.C. İnkılap Tarihi	1.6660	10	1
Din Kültürü	1.8990	10	1
İngilizce	1.5075	10	1
Hesaplama Adımları:

Ham net hesaplama: hamNet = doğru - (yanlış / 3)
Negatif netler 0'a sabitlenir: net = max(0, hamNet)
Başarı oranı (normalize): oran = net / mevcutSoruSayısı (0.0 ile 1.0 arası)
Ölçekleme (orijinal soru sayısına): ölçekliNet = oran × varsayılanSoruSayısı
Ağırlıklı toplam: ağırlıklıToplam += ölçekliNet × katsayı
Final puan: puan = 194.752082 + ağırlıklıToplam, min 100 max 500 arasında sınırlanır
Tam Puan Doğrulama: Tüm sorular doğru yapıldığında (varsayılan soru sayılarıyla): 194.752 + (20×4.348) + (20×4.2538) + (20×4.123) + (10×1.666) + (10×1.899) + (10×1.5075) = 194.752 + 86.96 + 85.076 + 82.46 + 16.66 + 18.99 + 15.075 = 499.973 ≈ 500

Akıllı Hedef Puan Algoritması
2 veya daha fazla deneme sonrasında aktif olan ağırlıklı formül: hedef = (son3Ortalama × 0.40) + (enİyiPuan × 0.30) + (genelOrtalama × 0.10) + ((sonPuan + trend) × 0.20). Tavan sınırı min(500, enİyiPuan × 1.05), taban sınırı son3Ortalama. Hedef tavan ve taban arasında sınırlanır.

Ağırlık gerekçeleri: Son 3 ortalama %40 ile güncel performansı en ağır yansıtır. En iyi puan %30 ile öğrencinin ulaşabileceği potansiyeli gösterir. Trend projeksiyonu %20 ile yükseliş/düşüş momentumunu yakalar. Genel ortalama %10 ile uzun vadeli tutarlılığı dengeler. Tavan gerçekçi olmayan hedefleri, taban ise motivasyon kırıcı düşük hedefleri engeller.

Normalize Edilmiş Net Ölçekleme
Problem: Orijinal katsayılar sabit LGS soru yapısına (20-20-20-10-10-10) göre kalibre edilmiştir. Kullanıcı soru sayısını değiştirdiğinde (ör: Türkçe 10 soru) 10 sorudan 10 doğru yapıldığında net 10 olur ve 10 × 4.348 = 43.48 çıkar ki bu yanlış bir sonuçtur (yarı puan). Oysa 20 sorudan 20 doğru yapıldığında net 20 olur ve 20 × 4.348 = 86.96 doğru puanı verir.

Çözüm: Neti başarı oranına dönüştürüp orijinal ölçeğe geri çevirmek. 10 sorudan 10 doğru yapıldığında net 10, oran 10/10 = 1.0 (%100 başarı), ölçekliNet = 1.0 × 20 = 20, sonuç 20 × 4.348 = 86.96 doğru puan.

Kenar durumlar: Soru sayısı 0 olan dersler katkı sağlamaz (sıfıra bölme engeli). Oran 1.0'dan büyükse 1.0'a sabitlenir. Negatif net 0'a sabitlenir. Final puan 100'den düşükse 100'e, 500'den büyükse 500'e sabitlenir.

Veri Yapısı
localStorage'da iki anahtar kullanılır: lgs_exams (deneme kayıtları dizisi) ve lgs_settings (kullanıcı ayarları nesnesi).

Deneme nesnesi şu alanlardan oluşur: benzersiz id, deneme adı (name), tarih (date), not (note), dersler nesnesi (subjects, her ders için doğru/yanlış/boş), sonuç nesnesi (result, puan/toplam net/toplam doğru/yanlış/boş ve ders bazlı netler), oluşturulma tarihi (createdAt) ve güncelleme tarihi (updatedAt).

Ayarlar nesnesi şu alanlardan oluşur: tema (theme, light veya dark), vurgu rengi (accent), grafik türü (chartType, line veya bar) ve ders soru sayıları (questionCounts, her ders için sayı).

Dışa aktarma dosyası exams dizisi, settings nesnesi, exportDate ve version alanlarını içerir.

CSS Mimarisi
Tema sistemi CSS Custom Properties kullanır. Aydınlık tema :root'ta, karanlık tema [data-theme="dark"] seçicisi ile tanımlanır. Temel değişkenler: bg (sayfa arka planı), surface (kart arka planı), surface2 (ikincil yüzey), text (ana metin), text2 (ikincil metin), text3 (soluk metin), border (kenarlıklar), accent (vurgu rengi, dinamik), danger (hata/uyarı), success (başarı), warn (ikaz).

Responsive breakpoint'ler: 768px ve altında grafik grid tek sütun, stat grid 3 sütun, form grid tek sütun olur ve tablo input genişliği küçülür. 480px ve altında stat grid 2 sütun olur, container ve kart padding'i azalır.

JavaScript Modül Yapısı
Kod şu ana bölümlerden oluşur: Sabitler ve Varsayılanlar (DEFAULT_SUBJECTS, SCORE_COEFFICIENTS, BASE_SCORE, MIN/MAX_SCORE, MAX_EXAMS, ACCENT_COLORS), Global Durum Değişkenleri (exams dizisi, settings nesnesi, editingId, lastResult, chartInstances), Veri Yükleme/Kaydetme (loadData, saveData, loadSettings, saveSettings), Tema Yönetimi (toggleTheme, applyTheme, applyAccentColor, selectAccentColor), Ayarlar Paneli (openSettings, closeSettings, buildSettingsPanel), Form İşlemleri (buildSubjectTable, onSubjectInput, validateForm, clearForm, setDefaultDate), Puan Hesaplama (calculateScore), CRUD İşlemleri (saveExam, editExam, cancelEdit, deleteExam, generateId), Render Fonksiyonları (renderResult, renderHistory, renderCharts, renderSmartTarget, renderAnalysis), Grafik Yönetimi (chartOptions, destroyChart), Tab Yönetimi (switchTab), Yardımcı Fonksiyonlar (formatDate, showAlert, viewExamResult) ve Import/Export (exportData, importData, confirmClearAll).

🌐 Tarayıcı Desteği
Tarayıcı	Minimum Versiyon	Durum
Chrome	80+	Tam destek
Firefox	75+	Tam destek
Safari	13+	Tam destek
Edge	80+	Tam destek
Opera	67+	Tam destek
Samsung Internet	13+	Tam destek
IE 11	-	Desteklenmiyor
Gerekli Web API'leri: localStorage, CSS Custom Properties, CSS Grid ve Flexbox, ES6+ (arrow functions, template literals, destructuring, spread operator), Blob ve URL.createObjectURL (dışa aktarma için), FileReader (içe aktarma için).

⚠️ Bilinen Sınırlamalar
Sınırlama	Detay	Geçici Çözüm
localStorage boyut limiti	Yaklaşık 5-10 MB (tarayıcıya göre değişir)	100 deneme sınırı bu limitin altında kalır (yaklaşık 200 KB)
Tarayıcı verisi temizleme	Tarayıcı önbellek/veri temizlenirse kayıtlar silinir	Düzenli JSON yedekleme
Çevrimdışı grafik	Chart.js CDN'den yüklenir, ilk açılışta internet gerekir	Tarayıcı önbelleğe aldıktan sonra çevrimdışı çalışır
Tahmini puan doğruluğu	Katsayılar yaklaşıktır, yıldan yıla değişebilir	Puanı referans olarak kullanın, resmi sonuç için MEB'e bakın
Cihazlar arası senkronizasyon	Veriler sadece yerel tarayıcıda	JSON dışa/içe aktarma ile manuel aktarım
Çoklu kullanıcı	Tek kullanıcı desteği	Farklı tarayıcı profilleri kullanılabilir
Yazdırma	Özel yazdırma stili yok	Tarayıcının varsayılan yazdırma özelliğini kullanın
❓ Sıkça Sorulan Sorular
Puanlar gerçek LGS puanıyla ne kadar uyuşur?

Bu uygulama tahmini puanlar üretir. Kullanılan katsayılar yaygın olarak kabul gören yaklaşık değerlerdir ancak MEB'in resmi katsayıları yıldan yıla farklılık gösterebilir. Puanları kesin sonuç olarak değil, göreceli performans takibi aracı olarak değerlendirin.

Verilerim güvende mi?

Evet. Tüm veriler yalnızca sizin tarayıcınızın localStorage'ında saklanır. Hiçbir veri hiçbir sunucuya gönderilmez. Uygulama herhangi bir analitik, izleme veya veri toplama aracı içermez.

Soru sayılarını değiştirince puan neden aynı kalıyor?

Uygulama normalize edilmiş net ölçekleme kullanır. 10 sorudan 10 doğru = 20 sorudan 20 doğru (%100 başarı = aynı puan). Bu tasarım gereğidir; farklı yayınevlerinin farklı soru sayılarında adil karşılaştırma yapılabilmesi için.

Başka bir cihazdan erişebilir miyim?

Veriler tarayıcıya özeldir. Başka bir cihaza aktarmak için ayarlardan "Verileri Dışa Aktar" ile JSON dosyası indirin, dosyayı diğer cihaza aktarın ve ayarlardan "Verileri İçe Aktar" ile yükleyin.

Kaç deneme kaydedebilirim?

Maksimum 100 deneme kaydedilebilir. Bu sınır localStorage boyut limitini aşmamak ve performansı korumak için konulmuştur. Eski denemeleri silerek yer açabilirsiniz.

Tarayıcıyı kapattığımda verilerim silinir mi?

Hayır. localStorage verileri tarayıcı kapatılsa bile kalıcıdır. Ancak tarayıcı verilerini/önbelleğini manuel olarak temizlerseniz veya gizli/özel pencere kullanırsanız veriler silinebilir.

İnternet olmadan kullanabilir miyim?

Grafik kütüphanesi (Chart.js) CDN'den yüklenir, bu nedenle ilk açılışta internet bağlantısı gerekir. Tarayıcı dosyayı önbelleğe aldıktan sonra grafikler dahil tüm özellikler çevrimdışı çalışır. Grafik olmadan temel işlevler (giriş, hesaplama, geçmiş) her zaman çevrimdışı çalışır.

🛣️ Yol Haritası
v1.1 (Planlanan)
PWA (Progressive Web App) desteği, ana ekrana ekleme ve tam çevrimdışı çalışma
Yazdırma dostu stil sayfası
Deneme karşılaştırma modu (2 denemeyi yan yana karşılaştırma)
Konu bazlı detay girişi (ör: Türkçe altında Paragraf, Dil Bilgisi gibi alt başlıklar)
v1.2 (Düşünülen)
PDF rapor oluşturma
Hedef lise ve taban puan karşılaştırması
Çalışma planı önerisi
Ders bazlı zaman analizi (süre giriş seçeneği)
Çoklu profil desteği
v2.0 (Gelecek)
Opsiyonel bulut senkronizasyon (Firebase veya benzeri)
Sosyal karşılaştırma (anonim istatistikler)
Yapay zeka destekli analiz ve öneri sistemi
🤝 Katkıda Bulunma
Katkılarınızı memnuniyetle karşılıyoruz! Proje tek dosyalı bir yapıda olduğundan katkıda bulunmak oldukça kolaydır.

Nasıl Katkıda Bulunulur
Bu depoyu fork'layın
Yeni bir branch oluşturun: git checkout -b ozellik/yeni-ozellik
Değişikliklerinizi yapın
Test edin (tarayıcıda açıp tüm sekmeleri kontrol edin)
Commit atın: git commit -m 'feat: Yeni özellik açıklaması'
Push yapın: git push origin ozellik/yeni-ozellik
Pull Request açın
Katkı Rehberi
Tek dosya yapısını koruyun, harici CSS/JS dosyası eklemeyin
Kodda Türkçe yorum kullanın (kullanıcı arayüzü Türkçe olduğundan)
Değişken ve fonksiyon adları İngilizce kalabilir
Responsive tasarımı bozmayın, 3 breakpoint'te test edin
localStorage yapısında geriye dönük uyumluluk sağlayın
Yeni ders eklerken DEFAULT_SUBJECTS ve SCORE_COEFFICIENTS'ı güncelleyin
Hata Bildirimi
Issues sayfasından hata bildirebilirsiniz. Lütfen tarayıcı ve versiyon, hatanın adım adım tekrarlanması, beklenen ve gerçekleşen davranış ile varsa konsol hata mesajını belirtin.

📄 Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için LICENSE dosyasına bakınız.

⚖️ Sorumluluk Reddi
Bu uygulama bağımsız olarak geliştirilmiş olup MEB (Millî Eğitim Bakanlığı) ile herhangi bir bağlantısı yoktur.

Hesaplanan puanlar tahmini niteliktedir ve yaygın kullanılan yaklaşık katsayılara dayalıdır. LGS puan hesaplama katsayıları her yıl değişebilir ve MEB tarafından resmi olarak açıklanmamaktadır. Bu nedenle puanları kesin sonuç olarak kabul etmeyin, puanları okul tercihi için tek kriter olarak kullanmayın, resmi ve kesin sonuçlar için yalnızca MEB'in açıklamalarına başvurun. Uygulama geliştiricisi puan doğruluğu konusunda herhangi bir garanti vermez.

Bu araç, öğrencilerin göreceli gelişimlerini takip etmeleri ve güçlü/zayıf yönlerini tespit etmeleri amacıyla tasarlanmıştır.

Bu proje işinize yaradıysa yıldız vermeyi unutmayın!

```bash
git clone https://github.com/KULLANICI_ADI/lgs-deneme-takip.git
cd lgs-deneme-takip
