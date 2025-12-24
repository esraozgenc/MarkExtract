# 🖊️ MarkExtract: İşaretli Metin Tanıma ve Raporlama Sistemi

MarkExtract, fiziksel veya dijital belgeler üzerinde renkli fosforlu kalemlerle (highlighter) işaretlenmiş metinleri otomatik olarak algılayan, ayıklayan ve bunları düzenli bir PDF raporuna dönüştüren bir görüntü işleme projesidir.

## 🚀 Özellikler
- **Çoklu Renk Desteği:** Sarı, mavi, pembe ve yeşil işaretleyicileri tanıyabilir.
- **Format Esnekliği:** Hem `.jpg, .jpeg, .png` gibi görsel formatlarını hem de çok sayfalı `.pdf` dosyalarını destekler.
- **Gelişmiş Metin Tanıma (OCR):** Türkçe ve İngilizce dil desteğiyle EasyOCR kütüphanesini kullanır.
- **Otomatik Raporlama:** Ayıklanan metinleri anlık olarak `MarkExtract_Final_Report.pdf` adıyla yeni bir dosyaya kaydeder.

## 🛠️ Kullanılan Teknolojiler
- **Python 3.9+**
- **OpenCV:** Renk maskeleme (HSV) ve morfolojik işlemler için.
- **EasyOCR:** Metin tanıma işlemleri için.
- **PyMuPDF (fitz):** PDF sayfalarını görsele dönüştürmek için.
- **FPDF:** Sonuç raporunu oluşturmak için.
- **NumPy:** Matris işlemleri ve veri manipülasyonu için.

## 📋 Çalışma Mantığı
1. **Görüntü Önişleme:** Yüklenen belge HSV renk uzayına dönüştürülür.
2. **Renk Maskeleme:** Belirlenen renk aralıklarına göre (örneğin sarı için 20-30 tonları) bir maske oluşturulur.
3. **Kontur Algılama:** Maskelenen alanlar etrafında konturlar çizilerek metin blokları belirlenir.
4. **OCR İşlemi:** Belirlenen bu koordinatlardaki metinler EasyOCR ile okunur.
5. **PDF Çıktısı:** Okunan tüm metinler birleştirilerek temiz bir PDF raporuna yazdırılır.

1. Depoyu klonlayın:
   ```bash
   git clone [https://github.com/kullaniciadi/MarkExtract.git](https://github.com/kullaniciadi/MarkExtract.git)
