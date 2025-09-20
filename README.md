# Acquiring and Processing Information on the World's Largest Banks

## 📌 Proje Hakkında
Bu proje, dünyanın en büyük 10 bankasının piyasa değerlerini **Extract – Transform – Load (ETL)** yaklaşımıyla otomatik olarak işleyen bir sistemdir.  

Projede hedef:  
- Veriyi **Wikipedia** üzerinden çekmek  
- Farklı para birimlerine dönüştürmek  
- **CSV** ve **SQLite** veritabanına yüklemek  
- **SQL sorguları** ile raporlama yapmak  

---

## 🚀 Kullanılan Teknolojiler
- **Python 3.11**  
- `requests` → Web sayfası alma  
- `lxml` & `BeautifulSoup` → HTML parsing  
- `pandas` → Veri işleme  
- `numpy` → Sayısal işlemler  
- `sqlite3` → Veritabanı işlemleri  

---

## ⚙️ Çalışma Adımları

### 1. Veri Çekme (Extract)  
Wikipedia’daki *By Market Capitalization* tablosu scrape edilerek bankaların isimleri ve USD cinsinden piyasa değerleri alındı.  

### 2. Dönüştürme (Transform)  
- Sağlanan döviz kuru CSV dosyası kullanılarak **USD → GBP, EUR, INR** dönüşümleri yapıldı.  
- Sonuçlar **2 ondalık basamak** ile yuvarlandı.  

### 3. Yükleme (Load)  
- İşlenen veriler **CSV dosyası** olarak kaydedildi.  
- Aynı veriler **SQLite veritabanına** tablo olarak yüklendi.  

### 4. SQL Sorguları (Queries)  
- Tüm tabloyu listeleme  
- Ortalama piyasa değeri (GBP)  
- İlk 5 bankanın isimleri  

---

## 📂 Çıktılar
- **Largest_banks_data.csv** → İşlenen veriler  
- **Banks.db** → SQLite veritabanı  
- **code_log.txt** → Süreç log dosyası  

---
