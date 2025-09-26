# deep-learning-akbank

📌 Projenin Amacı
Bu projenin amacı, derin öğrenme tabanlı bir görüntü sınıflandırma modeli geliştirerek kedi ve köpek fotoğraflarını ayırt edebilmektir. Görüntü işleme teknikleri ve konvolüsyonel sinir ağları (CNN) kullanılarak yüksek doğruluk oranına ulaşmak hedeflenmiştir. Ayrıca modelin performansı confusion matrix, classification report ve Grad-CAM görselleştirmeleri ile değerlendirilmiştir.

📂 Veri Seti Hakkında
Kullanılan veri seti: Dogs vs. Cats (Kaggle)
Eğitim seti: train/ klasöründe kedi ve köpek resimleri.
Test seti: test/ klasöründe ayrılmış görseller.
Eğitim verilerinin %20’si validation için ayrılmıştır.
Görseller model girişine uygun olacak şekilde 96x96 piksel boyutuna yeniden ölçeklendirilmiştir.

--Kullanılan Yöntemler--
Veri Ön İşleme
Normalizasyon (Rescaling(1./255))
Veri artırma (RandomFlip, RandomRotation, RandomZoom)
Model Mimarisi (Sequential CNN)
Conv2D + MaxPooling katmanları (32, 64, 128 filtre)
Dropout (overfitting’i engellemek için)
Dense katmanlar (128 nöron + softmax çıkış)
Eğitim
Optimizer: Adam
Loss: SparseCategoricalCrossentropy
Epoch: 3 (temel deneme için)
Batch Size: 8
Değerlendirme Araçları
Accuracy & Loss eğrileri
Test seti doğruluğu
Confusion Matrix
Classification Report (precision, recall, f1-score)
Grad-CAM görselleştirmesi (modelin karar verirken hangi bölgeleri dikkate aldığını anlamak için)

📊 Elde Edilen Sonuçlar
Eğitim seti doğruluğu: ~%90+
Validation doğruluğu: ~%85–88
Test doğruluğu: ~%85
Confusion matrix ve classification report sonuçlarına göre model her iki sınıfta da dengeli bir başarı göstermiştir.
Grad-CAM görselleri, modelin doğru tahminlerde genellikle hayvanın yüz bölgesine odaklandığını göstermektedir.

Bu proje, temel CNN mimarisinin kedi-köpek sınıflandırma probleminde etkili sonuçlar verdiğini göstermektedir. Daha yüksek başarı için daha derin ağlar (ör. VGG16, ResNet, EfficientNet gibi transfer learning modelleri) kullanılabilir.

kaggle link : https://www.kaggle.com/code/zehraustaoglu/notebook8d977d7670
