# Fish_Classification_ANN


Balık Görüntü Sınıflandırması: Yapay Sinir Ağı (ANN) Yaklaşımı

İçindekiler
•	Proje Özeti
•	Veri Seti
•	Projenin Amacı
•	Model Yapısı
•	Hiperparametre Optimizasyonu
•	Sonuçlar
•	Gelecek Çalışmalar
•	Kaggle Proje Linki

Proje Özeti
Bu proje, İzmir'deki bir süpermarketten toplanan görüntüler kullanılarak 9 farklı deniz ürünü türünün sınıflandırılmasını hedeflemektedir. Veri seti, İzmir Ekonomi Üniversitesi ve bir sanayi kuruluşunun iş birliğiyle yürütülen üniversite-sanayi ortaklık projesi kapsamında toplanmış olup, 2020 yılında ASYU'da yayınlanmıştır. Balık türlerinin sınıflandırılması için yaygın olarak Convolutional Neural Network (CNN) kullanılsa da, bu projede sadece Yapay Sinir Ağı (ANN) kullanılmıştır.

Veri Seti
Veri seti aşağıdaki balık türlerine ait görüntüleri içermektedir:
•	Gilt Head Bream
•	Red Sea Bream
•	Sea Bass
•	Red Mullet
•	Horse Mackerel
•	Black Sea Sprat
•	Striped Red Mullet
•	Trout
•	Shrimp
Her balık türüne ait 1.000 görüntü bulunmaktadır. Bu nedenle veri seti dengelidir ve toplamda 9.000 görüntüden oluşmaktadır.

Projenin Amacı
Bu projenin amacı, ANN kullanarak balık türlerini doğru şekilde sınıflandırmak ve modelin genelleme kabiliyetini artırmaktır. Genelleme kabiliyeti, modelin daha önce görmediği yeni verileri doğru şekilde tahmin edebilme yeteneğidir. Ancak, aşırı öğrenme (overfitting) bu kabiliyeti engelleyebilir. Bu sorunu aşmak için early stopping ve dropout gibi yöntemler kullanılmıştır. Ek olarak, hiperparametre optimizasyonu yapılmıştır.

Model Yapısı
Bu projede, CNN yerine ANN kullanılmıştır. Görüntüler doğrudan ANN'e verilmiş ve özellik çıkarımı aşaması olmadan balık türlerinin doğru şekilde sınıflandırılması sağlanmıştır. Modelin genel yapısı şu şekildedir:
1.	Girdi Katmanı: Görüntü pikselleri doğrudan ANN'e beslenir.
2.	Yoğun Katmanlar (Dense Layers): Tam bağlı katmanlar sınıflandırma işlemini yapar.
3.	Çıktı Katmanı: Softmax aktivasyon fonksiyonu ile çoklu sınıf sınıflandırması yapılır.

Hiperparametre Optimizasyonu
Modelin performansını artırmak ve aşırı öğrenmeyi engellemek amacıyla Random Search yöntemiyle hiperparametre optimizasyonu yapılmıştır. Random Search, hiperparametre uzayından rastgele örnekler seçerek arama yapar. Bu yöntem, arama uzayının büyük olduğu durumlarda daha hızlı sonuç alınmasını sağlar, ancak optimum hiperparametre kombinasyonunu bulmak her zaman garanti değildir.
Alternatif Yöntemler:
•	Grid Search: Hiperparametre kombinasyonlarının tamamı taranarak en iyi sonuca ulaşılır, fakat çok fazla hesaplama gücü ve zaman gerektirir.
•	Bayesian Optimization: Daha az denemeyle optimum sonuca ulaşabilir ve zaman tasarrufu sağlar. Ancak, çok büyük arama uzaylarında yine de uzun sürebilir.
📌 Yapılan hiperparametre aramaları sonucunda modelde belirgin bir iyileşme gözlenmemiştir, bu durum Random Search’ün rastgele seçimler yapmasından kaynaklanmaktadır.

Sonuçlar
•	Eğitim Doğruluğu: %99.7
•	Doğrulama Doğruluğu: %97.6
Model, eğitim ve doğrulama setlerinde iyi bir performans göstermiştir. Aşırı öğrenme engellenmiş ve genel olarak güçlü bir model elde edilmiştir.


Gelecek Çalışmalar
•	Özellik çıkarımı için CNN'leri deneyerek performans karşılaştırması yapılabilir.
•	Daha gelişmiş hiperparametre optimizasyon yöntemleri (örneğin, Bayesian Optimization) uygulanabilir.
•	Veri çoğaltma (data augmentation) teknikleri kullanılarak veri seti çeşitlendirilebilir.

Kaggle Proje Linki
Projenin Kaggle sayfasına ulaşmak için şu bağlantıyı kullanabilirsiniz:

