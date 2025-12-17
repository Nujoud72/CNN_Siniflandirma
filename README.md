# CNN Tabanlı Görüntü Sınıflandırma Projesi
Bu projede, evrişimsel sinir ağları (Convolutional Neural Networks – CNN)
kullanılarak bileklik ve saat görsellerinin sınıflandırılması amaçlanmıştır.
Proje, Google Colab ortamında Python ve TensorFlow/Keras kütüphaneleri
kullanılarak geliştirilmiştir.

---

## Proje Amacı
Bu çalışmanın amacı, görüntü işleme ve derin öğrenme alanında yaygın olarak
kullanılan CNN mimarilerini uygulamalı olarak incelemek ve farklı model
yaklaşımlarının sınıflandırma performanslarını karşılaştırmaktır.

Bu kapsamda:
- Temel bir CNN modeli,
- Transfer Learning yaklaşımı,
- Veri artırma (Data Augmentation) ve geliştirilmiş CNN mimarisi

kullanılarak üç farklı model oluşturulmuş ve sonuçları karşılaştırılmıştır.

---

## Veri Seti
- Sınıflar: **Bileklik**, **Saat**
- Her sınıf için yaklaşık **100 adet** görsel kullanılmıştır.
- Görseller farklı açılar, ışık koşulları ve arka planlar içerecek şekilde
  hazırlanmıştır.
- Tüm görseller **128x128** boyutuna yeniden boyutlandırılmıştır.
- Veri seti, eğitim (%80) ve doğrulama (%20) olarak ayrılmıştır.

Klasör yapısı aşağıdaki gibidir:
```text
dataset/
├── Bileklik/
└── Saat/
```

---

## Kullanılan Modeller

### Model-2: Temel CNN
- Conv2D ve MaxPooling katmanlarından oluşan temel bir CNN mimarisi
- ReLU aktivasyon fonksiyonu
- Dropout ile aşırı öğrenmenin azaltılması

### Model-1: Transfer Learning (MobileNetV2)
- ImageNet veri seti ile önceden eğitilmiş MobileNetV2 modeli kullanılmıştır
- Temel model dondurularak yalnızca sınıflandırma katmanları eğitilmiştir
- Daha hızlı ve kararlı öğrenme sağlanmıştır

### Model-3: Geliştirilmiş CNN + Data Augmentation
- Veri artırma (döndürme, kaydırma, yakınlaştırma, yatay çevirme)
- Daha derin CNN mimarisi
- Daha yüksek Dropout oranı
- Genelleme performansının artırılması hedeflenmiştir

---

## Performans Değerlendirmesi
Modeller aşağıdaki yöntemler kullanılarak değerlendirilmiştir:
- Accuracy ve Validation Accuracy grafikleri
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)

Ayrıca, eğitilen model gerçek hayattan alınan tekil bir görsel üzerinde test
edilerek sınıflandırma sonucu gözlemlenmiştir.

---

## Kullanılan Teknolojiler
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

---

## Projeyi Çalıştırma
1. Google Colab ortamında notebook dosyasını açın.
2. Veri setini uygun klasör yapısında yükleyin.
3. Notebook’taki hücreleri sırayla çalıştırın.
4. Eğitilmiş modeli kullanarak test görselleri üzerinde tahmin yapabilirsiniz.

---

## Notlar
Bu proje, akademik amaçlı bir ders ödevi kapsamında hazırlanmıştır.
Kodlar ve açıklamalar, model mimarilerinin ve öğrenme süreçlerinin daha iyi
anlaşılabilmesi amacıyla detaylı şekilde yorumlanmıştır.
