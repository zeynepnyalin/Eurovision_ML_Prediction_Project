# Eurovision Şarkı Yarışması'nda Başarı Tahmini (Makine Öğrenmesi Yaklaşımı)

**SAKARYA ÜNİVERSİTESİ - BİLİŞİM SİSTEMLERİ MÜHENDİSLİĞİ (Yüksek Lisans Dersi Projesi)**

## Proje Özeti
Bu çalışma, Eurovision Şarkı Yarışması'na katılan şarkıların ilk 10'a girip girmeme durumunu tahmin etmek amacıyla Lojistik Regresyon, Random Forest ve XGBoost gibi makine öğrenmesi yöntemlerinin uygulanmasını içermektedir.

Projede, özellikle **sahne sırası, dans edilebilirlik, enerji düzeyi ve şarkı dili** gibi faktörlerin başarı üzerindeki etkileri incelenmiştir.

## Veri Seti
Projede 2009-2023 yılları arasındaki 565 şarkıya ait veriler kullanılmıştır. Veri setindeki sınıf dengesizliği, **SMOTE** yöntemiyle giderilmiştir.
- Kaynak: [Kaggle - Eurovision Song Contest Data](https://www.kaggle.com/datasets/diamondsnake/eurovision-song-contest-data)

## Kullanılan Algoritmalar ve Sonuçlar
- **Algoritmalar:** Lojistik Regresyon, Random Forest, XGBoost
- **Özellik Seçimi:** Recursive Feature Elimination (RFE) yöntemi ile her model için en iyi 10 özellik belirlenmiştir.
- **En İyi Model:** Hiperparametre optimizasyonu ve çapraz doğrulama sonrasında **Lojistik Regresyon** modeli, test verisinde en yüksek F1 skoruyla ($F1=0.59$) genel model tercihi olarak belirlenmiştir.
- **Gerçek Dünya Uygulaması (2024 Tahmini):** Eğitilen Lojistik Regresyon modeli, 2024 Eurovision şarkıları üzerinde test edilmiş ve yaklaşık **%68 doğruluk** oranıyla (top 10 sınıfı için F1 skoru: 0.40) tahmin yapmıştır.

## Proje Dosyaları
- `ProjeRaporu.pdf`: Proje Raporu
- `ProjeKodu.ipynb`: Proje Kodu (Jupyter Notebook)

## Gelecek Çalışmalar İçin Öneriler
1. Şarkı sözleri için Doğal Dil İşleme (NLP) tekniklerinin entegrasyonu.
2. Sahne performansları ve kostümler için Bilgisayarlı Görü (Computer Vision) tekniklerinin kullanılması.
3. Zamansal dinamikleri modellemek için zaman serisi analizleri veya derin öğrenme (RNN) yaklaşımları.
