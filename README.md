# Fish_Classification_ANN

<div class="alert alert-block" style="background-color: #00b7eb;">
  <span style="color:#2c3e50; font-weight: bold; font-size: 26px;">🎣 Balık Görüntü Sınıflandırması: Yapay Sinir Ağı (ANN) Yaklaşımı</span>
</div>

<h3>İçindekiler</h3>
<ul>
  <li>Proje Özeti</li>
  <li>Veri Seti</li>
  <li>Projenin Amacı</li>
  <li>Model Yapısı</li>
  <li>Hiperparametre Optimizasyonu</li>
  <li>Sonuçlar</li>
  <li>Gelecek Çalışmalar</li>
  <li>Kaggle Proje Linki</li>
</ul>

<h3>Proje Özeti</h3>
<p>Bu proje, İzmir'deki bir süpermarketten toplanan görüntüler kullanılarak 9 farklı deniz ürünü türünün sınıflandırılmasını hedeflemektedir. Veri seti, İzmir Ekonomi Üniversitesi ve bir sanayi kuruluşunun iş birliğiyle yürütülen üniversite-sanayi ortaklık projesi kapsamında toplanmış olup, 2020 yılında ASYU'da yayınlanmıştır. Balık türlerinin sınıflandırılması için yaygın olarak Convolutional Neural Network (CNN) kullanılsa da, bu projede sadece Yapay Sinir Ağı (ANN) kullanılmıştır.</p>

<h3>Veri Seti</h3>
<p>Veri seti aşağıdaki balık türlerine ait görüntüleri içermektedir:</p>
<ul>
  <li>Gilt Head Bream</li>
  <li>Red Sea Bream</li>
  <li>Sea Bass</li>
  <li>Red Mullet</li>
  <li>Horse Mackerel</li>
  <li>Black Sea Sprat</li>
  <li>Striped Red Mullet</li>
  <li>Trout</li>
  <li>Shrimp</li>
</ul>
<p>Her balık türüne ait 1.000 görüntü bulunmaktadır. Bu nedenle veri seti dengelidir ve toplamda 9.000 görüntüden oluşmaktadır.</p>

<h3>Projenin Amacı</h3>
<p>Bu projenin amacı, ANN kullanarak balık türlerini doğru şekilde sınıflandırmak ve modelin genelleme kabiliyetini artırmaktır. Genelleme kabiliyeti, modelin daha önce görmediği yeni verileri doğru şekilde tahmin edebilme yeteneğidir. Ancak, aşırı öğrenme (overfitting) bu kabiliyeti engelleyebilir. Bu sorunu aşmak için early stopping ve dropout gibi yöntemler kullanılmıştır. Ek olarak, hiperparametre optimizasyonu yapılmıştır.</p>

<h3>Model Yapısı</h3>
<p>Bu projede, CNN yerine ANN kullanılmıştır. Görüntüler doğrudan ANN'e verilmiş ve özellik çıkarımı aşaması olmadan balık türlerinin doğru şekilde sınıflandırılması sağlanmıştır. Modelin genel yapısı şu şekildedir:</p>
<ul>
  <li>Girdi Katmanı: Görüntü pikselleri doğrudan ANN'e beslenir.</li>
  <li>Yoğun Katmanlar (Dense Layers): Tam bağlı katmanlar sınıflandırma işlemini yapar.</li>
  <li>Çıktı Katmanı: Softmax aktivasyon fonksiyonu ile çoklu sınıf sınıflandırması yapılır.</li>
</ul>

<h3>Hiperparametre Optimizasyonu</h3>
<p>Modelin performansını artırmak ve aşırı öğrenmeyi engellemek amacıyla Random Search yöntemiyle hiperparametre optimizasyonu yapılmıştır. Random Search, hiperparametre uzayından rastgele örnekler seçerek arama yapar. Bu yöntem, arama uzayının büyük olduğu durumlarda daha hızlı sonuç alınmasını sağlar, ancak optimum hiperparametre kombinasyonunu bulmak her zaman garanti değildir.</p>

<h4>Alternatif Yöntemler:</h4>
<ul>
  <li>Grid Search: Hiperparametre kombinasyonlarının tamamı taranarak en iyi sonuca ulaşılır, fakat çok fazla hesaplama gücü ve zaman gerektirir.</li>
  <li>Bayesian Optimization: Daha az denemeyle optimum sonuca ulaşabilir ve zaman tasarrufu sağlar. Ancak, çok büyük arama uzaylarında yine de uzun sürebilir.</li>
</ul>
<p>📌 Yapılan hiperparametre aramaları sonucunda modelde belirgin bir iyileşme gözlenmemiştir, bu durum Random Search’ün rastgele seçimler yapmasından kaynaklanmaktadır.</p>

<h3>Sonuçlar</h3>
<ul>
  <li>Eğitim Doğruluğu: %..</li>
  <li>Doğrulama Doğruluğu: %..</li>
</ul>
<p>Model, eğitim ve doğrulama setlerinde iyi bir performans göstermiştir. Aşırı öğrenme engellenmiş ve genel olarak güçlü bir model elde edilmiştir.</p>

<h3>Gelecek Çalışmalar</h3>
<ul>
  <li>Özellik çıkarımı için CNN'leri deneyerek performans karşılaştırması yapılabilir.</li>
  <li>Daha gelişmiş hiperparametre optimizasyon yöntemleri (örneğin, Bayesian Optimization) uygulanabilir.</li>
  <li>Veri çoğaltma (data augmentation) teknikleri kullanılarak veri seti çeşitlendirilebilir.</li>
</ul>

<h3>Kaggle Proje Linki</h3>
<p>Projenin Kaggle sayfasına ulaşmak için şu bağlantıyı kullanabilirsiniz: <a href="#">Kaggle Link</a></p>
