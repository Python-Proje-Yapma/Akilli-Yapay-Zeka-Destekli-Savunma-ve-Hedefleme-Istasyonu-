# Akıllı Yapay Zeka Destekli Savunma ve Hedefleme İstasyonu

Yapay zeka, bilgisayarlı görü ve robotik teknolojilerini harmanlayan otonom bir savunma simülasyonu projesidir. 

## Proje Amacı ve Çalışma Mantığı
Canlı kamera akışını anlık olarak işleyen sistem;
* **Mavi unsurları (Düşman/FPV Dron):** Tehdit olarak algılar ve lazer hedefleme mekanizmasını üzerine kilitler.
* **Kırmızı unsurları (Dost unsur):** Güvenli bölge olarak tanımlar ve hoparlör üzerinden sesli ikaz (örn. "Burası askeri alandır, derhal uzaklaşın!") verir.

## ⚙️ Teknik Detaylar ve İşleyiş
* **HSV Renk Uzayı ve Filtreleme:** Kamera pikselleri gürültüden arındırılarak hedef nesnelerin $(X, Y)$ piksel koordinatları anlık olarak hesaplanır.
* **Otonom Eksen Yönetimi:** Hedefin merkez noktası ile pan-tilt servo motorlarının konumları matris haritalandırmasıyla senkronize edilir.
* **Karar Mekanizması:** Renk ve nesne öncelik matrisine göre sistem otomatik olarak lazer aktivasyonuna veya sesli uyarı protokolüne karar verir.

## Kullanılan Teknolojiler
* **Python**
* **OpenCV & NumPy** (Görüntü İşleme ve Renk Filtreleme)
* **PySerial** (Donanım/Mikrodenetleyici Haberleşmesi)
* **Pygame / TTS** (Sesli Uyarı Sistemi)
