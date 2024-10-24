# ANNGLOBALAI_NESLIHANTOPRAK
Bu proje, bir yapay sinir ağı (ANN) kullanarak balık türlerini sınıflandırmak için oluşturulmuştur. Proje, büyük bir balık veri setini (Fish Dataset) kullanarak farklı türlerin görüntülerini analiz eder ve her türü doğru bir şekilde tanımlamak için bir model geliştirir.
pandas: Veri işleme ve analiz için.
numpy: Sayısal hesaplamalar için.
matplotlib: Görselleştirme için.
seaborn: Veri görselleştirmesi için.
tensorflow ve keras: Sinir ağı modelleme için.
scikit-learn: Model değerlendirme ve veri ön işleme için.
PIL: Görsel işleme için
Veri kümesi, farklı balık türlerine ait görüntüler içermektedir. Görüntüler, her tür için ayrı klasörlerde düzenlenmiştir.
Veri Ön İşleme
Veri ön işleme aşamasında, balık görüntüleri okunur ve yeniden boyutlandırılır. Görüntüler, modelin giriş boyutuna uygun hale getirilir ve normalleştirilir. Ayrıca, etiketler sayısal kodlara dönüştürülerek One-Hot Encoding ile vektöre dönüştürülür.

 Model Oluşturma
Yapay sinir ağı modeli, Sequential API kullanılarak oluşturulmuştur. Modelin yapısı şu şekildedir:

Giriş katmanı: (64, 64, 3) boyutunda görüntüler için.
İlk gizli katman: 32 nöronlu Conv2D katmanı.
İkinci gizli katman: 64 nöronlu Conv2D katmanı.
Tam bağlantılı katman: 128 nöronlu Dense katmanı.
Çıkış katmanı: Sınıflandırma için softmax aktivasyon fonksiyonu.
 Model Eğitimi
Model, eğitim verileri kullanılarak eğitilir. Eğitim sırasında EarlyStopping kullanılarak aşırı öğrenme (overfitting) önlenir. Eğitim ve doğrulama kayıpları ile doğruluk değerleri grafik olarak görselleştirilir.

 Model Değerlendirme
Model, test verileri üzerinde değerlendirilir. Test sonuçları, confusion matrix ve classification report kullanılarak analiz edilir.

 Sonuçlar ve Görselleştirme
Modelin performansı, birkaç test görüntüsü üzerinde tahminler yaparak görselleştirilir. Gerçek etiketler ve tahminler karşılaştırılır.
İkinci aşamada hipermetre optimizasyonu yaparak tekrar model eğitimi ve degerlendirme yaptım 

Test Verisi Tahminleri ve Sınıflandırma Raporu:

Model, test verisi üzerinde tahmin yapar ve bu tahminler ile gerçek etiketler karşılaştırılır.
classification_report ile her sınıf için doğruluk, hatırlama ve F1 skoru gibi metrikler hesaplanır.
Karışıklık matrisi (confusion matrix) ile tahmin edilen ve gerçek etiketler arasındaki farklar görselleştirilir.
Test Verisi Değerlendirmesi:

Modelin test verisi üzerindeki kaybı (loss) ve doğruluğu (accuracy) hesaplanır ve yazdırılır.
Rastgele Görüntü Tahminlerinin Görselleştirilmesi:

Test setinden rastgele seçilen 9 görüntü için modelin tahmin ettiği sınıflar ile gerçek sınıflar karşılaştırılır.
Görüntülerin altına tahmin edilen ve gerçek sınıflar yazılır, doğru tahminler yeşil, yanlış tahminler kırmızı ile gösterilir.
https://www.kaggle.com/code/neslihantoprak/ann-classification-neslihan-toprak/edit 
