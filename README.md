# Fish-Classification-ANN
Projenin kaggle linki : https://www.kaggle.com/code/aycaen/fish-classification/notebook
## Proje Hakkında:
Bu proje balık türlerini sınıflandırmayı amaçlamaktadır. Gerçek balık fotoğraflarından oluşan veri seti, ANN yapay sinir ağı modeli ile eğitilmiş doğrulanmış ve test edilmiştir.
## Veri Seti
- `path`: Balık görüntüsünün dosya yolu.
- `label`: Balığın türü (sınıflandırma için one-hot encoding uygulanmıştır).

## Model Mimarisi
ANN, TensorFlow kullanılarak şu mimari ile inşa edilmiştir:
- **Giriş Katmanı**: Ön işlenmiş balık görüntülerini alır.
- **Gizli Katmanlar**: ReLU aktivasyonu kullanan birden fazla yoğun katman.
- **Çıkış Katmanı**: Çok sınıflı sınıflandırma için softmax katmanı.

### Optimizasyonlar:
- **Erken Durdurma (Early Stopping)**: Modelin doğrulama performansı iyileşmediğinde eğitimi durdurmak için kullanıldı.
## Eğitim
- **Optimizatör**: Adam
- **Kayıp Fonksiyonu**: Categorical Crossentropy
- **Değerlendirme Metrikleri**: Accuracy
- **Batch Boyutu**: 32
- **Epoch Sayısı**: 50
 
