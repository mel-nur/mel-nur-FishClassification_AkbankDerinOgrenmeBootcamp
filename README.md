# mel-nur-FishClassification_AkbankDerinOgrenmeBootcamp

Fish Classification with Artificial Neural Networks (ANN)
Proje Özeti
Bu proje, Akbank Deep Learning Bootcamp kapsamında geliştirilmiştir. Projenin amacı, farklı balık türlerini içeren bir görüntü veri seti kullanarak balık sınıflandırması yapmak ve bu süreçte yapay sinir ağı (ANN) modeli kullanarak yüksek doğrulukta bir sınıflandırıcı model geliştirmektir.

İçerik
Bu projede gerçekleştirdiğimiz adımlar şu şekildedir:

1. Veri Hazırlama ve Keşifsel Veri Analizi (EDA)
Veri Setinin Yüklenmesi: Kaggle'dan alınan balık görüntü veri seti projenin temelini oluşturur. Veri setindeki balık türleri farklı klasörlerde tutulur.
Veri Seti Organizasyonu: Her bir balık türüne ait görüntü dosyalarının yolları ve sınıf etiketleri (balık türleri), Python kullanarak organize edilmiştir. Dosya yolları ve etiketler bir Pandas DataFrame'e dönüştürülmüştür.
Veri Keşfi (EDA):
Veri setinde kaç farklı balık türü olduğu ve her sınıftaki görüntü sayısı analiz edilmiştir.
Her sınıfa ait görüntülerin dengesi gözlemlenmiş, gerekirse veri artırma (data augmentation) işlemleri yapılabilecek şekilde planlama yapılmıştır.
2. Veri Ön İşleme
Görüntülerin Etiketlenmesi: Veri setindeki balık türleri etiketlenmiş ve bu etiketler model eğitiminde kullanılmak üzere düzenlenmiştir.
Veri Setinin Bölünmesi: Eğitim ve test verileri olarak ayrılmıştır. Eğitim seti, modelin öğrenmesi için kullanılırken test seti, modelin performansını değerlendirmek için kullanılmıştır.
Veri Artırma (Augmentation): Eğitim verisi üzerinde dönüşüm (rotation, flip gibi) işlemleri gerçekleştirilerek modelin daha fazla veri görmesi sağlanmıştır. Bu işlem, modelin genelleme yeteneğini artırmak için kullanılır.
3. Model Geliştirme ve Eğitim
Yapay Sinir Ağı (ANN) Modeli: TensorFlow ve Keras kullanılarak bir yapay sinir ağı modeli oluşturulmuştur. Model, balık görüntülerini sınıflandırmak için yapılandırılmıştır.
Model Mimarisi:
Katman sayısı, aktivasyon fonksiyonları (ReLU, Softmax vb.), optimizer (Adam gibi) ve loss fonksiyonu (categorical crossentropy) gibi bileşenler belirlenmiş ve modelin eğitimi optimize edilmiştir.
Modelin Eğitimi: Model, eğitim seti üzerinde eğitilmiş ve doğrulama seti ile performansı izlenmiştir. Eğitim sırasında doğruluk (accuracy) ve kayıp (loss) gibi metrikler takip edilmiştir.
4. Model Değerlendirme
Başarı Metrikleri: Eğitim sonunda modelin performansı şu metriklerle değerlendirilmiştir:
Accuracy (Doğruluk): Modelin genel başarı oranı.
Confusion Matrix (Karmaşıklık Matrisi): Her sınıf için doğru ve yanlış sınıflandırmalar.
Classification Report (Sınıflandırma Raporu): Precision, recall, F1-score gibi sınıflandırma başarı metrikleri.
Model Optimizasyonu: Eğitim sırasında overfitting'in önüne geçmek için düzenli olarak doğrulama seti ile test edilmiştir. Gerekirse erken durdurma (early stopping) ve model düzenleme (regularization) yöntemleri uygulanmıştır.
5. Sonuçlar ve Yorumlar
Bu projede geliştirilen ANN modeli, veri seti üzerindeki balık görüntülerini başarılı bir şekilde sınıflandırmıştır.
Model, veri artırma ve optimizasyon teknikleri ile geliştirilmiş, elde edilen sonuçlar başarı ile değerlendirilmiştir.
Sonuç olarak, balık görüntülerini sınıflandırmada etkili bir çözüm geliştirilmiş olup, bu proje balık türlerini otomatik olarak ayırt etmek için kullanılabilir.
Kullanılan Teknolojiler
Python: Veri işleme, model geliştirme ve analiz.
TensorFlow & Keras: Yapay sinir ağı modeli oluşturma ve eğitme.
Pandas & NumPy: Veri manipülasyonu ve düzenleme.
Matplotlib & Seaborn: Görselleştirme ve veri analizi.
Sklearn: Model değerlendirme metrikleri (confusion matrix, accuracy, classification report).
