# Bulut Üssü

Bu proje, **CTF (Capture The Flag)** için hazırlanmış basit bir açılış sayfasıdır.  
Sayfa üzerinde **"Verileri Getir"** butonuna basıldığında, bir **Cloudflare Worker API** üzerinden veriler çekilip tablo halinde gösterilmektedir.

## 📂 Proje İçeriği

- `index.html` → Ana sayfa dosyası  
- Basit bir frontend içerir:  
  - **Header** → Proje başlığı ve kısa açıklama  
  - **Card Bölümü** → API’den veri çekme butonu ve sonuçların görüntülendiği alan  
  - **JavaScript** → Fetch API ile verileri çekip tablo halinde yazdırır  

## ⚙️ Çalışma Mantığı

1. Kullanıcı **"Verileri Getir"** butonuna tıklar.  
2. JavaScript, `API_URL` ve `API_KEY` ile API isteği gönderir.  
3. API’den gelen JSON verisi tablo formatına dönüştürülerek ekranda gösterilir.  
4. Eğer hata olursa kullanıcıya uygun mesaj döner.  

## 🔑 Ortam Değişkenleri

Kod içerisinde değiştirilmesi gereken alanlar:

```js
const API_URL = "https://young-sound-1572.abidinsamet0cay.workers.dev/"; // Cloudflare Worker URL
const API_KEY = "kayseri-ankara"; // Worker tarafında tanımlı API anahtarı
+-----------+-----------+-----------+
| id        | name      | value     |
+-----------+-----------+-----------+
| 1         | test      | 123       |
| 2         | deneme    | 456       |
+-----------+-----------+-----------+
