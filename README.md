# Naive Bayes LAB
 Makine öğrenmesi laboratuvar ödev 1
 Makine Öğrenmesi laboratuvarında verilen naive bayes yöntemi kullanarak ikili sınıflandırma yapılması istenen ödevi nasıl yaptığımı anlatacağım.

İlk olarak naive bayes yöntemi için uygun bir veri seti bulmaya çalıştım.Bu aşamada kaggle üzerinde bir kaç tane veri seti buldum ama içlerinden örenek sayısı,sayısal değerler açısından ödeve uygun olanı seçmeye çalıştım.Seçtiğim veri setinde uygun olmayan verilere değiştimeler yaptım (örneğin glikoz değeri 0 olamazken bunun medyan ile değişmei sağlandı).Bu hazırlıktan sonra kod kısmına geçtim.

scikit-learn kullanarak naive bayes yöntemini uyguladım.Kodda sırasıyla;
1)Veri yükleme ve işleme.
2)Veri eğitim ve test setlerine ayrılır.
3)GaussanNB modeli oluşturulur ve eğitilir.
4)Model test edilir.
5)modelin performansı doğruluk değeri incelenir.
6)karmaşıklık matrisi görselleştirma aşamalarını izledim.

scikit-learn kullanmadan naivee bayes yöntemini uguladım.Kodda sırasıya;
1)Veri işlenir ve eğitim/test ayrımı yapılır.
2)Gaussian Naive Bayes modeli manuel olarak oluşturulur.
3)Eğitim ve tahmin yapılır.
4)Modelin doğruluğu hesaplanır.
5)Karmaşıklık matrisi hesaplanıp görselleştirme aşamalarını izledim.

Karşılaştırmalar:
karşılaştırmaya geçmeden veri setimi %80-%20 olacak şekilde ayırdım bu sayede doğruluk değeri daha optimum seviyeye ulaştı.(70-30,75-25 e göre)

Eğitim süreleri;
Scikit-learn GaussianNB: 0.002003
Kendi GaussianNB Modelimiz:0.001008
Kendi modelimiz biraz daha hızlı eğitilmiş. Bunun sebebi, Scikit-learn modelinin optimizasyon içeren ek işlemler yapması olabilir. Ancak, her iki model de oldukça hızlı eğitim aldığı için bu fark pratikte çok önemli değil.

Test süreleri;
Scikit-learn GaussianNB: 0.000996
Kendi GaussianNB Modelimiz:0.003992
Kendi modelimiz  NumPy dizileri ile Python içinde saf hesaplamalar yaptığı için daha yavaş çalışıyor.

Doğruluk karşılaştırması;
Scikit-learn GaussianNB: %75.32 doğruluk
Kendi GaussianNB Modelimiz: %75.32  doğruluk
Bu kendi modelimizin doğru bir şekilde çalıştığını ve Gaussian Naive Bayes algoritmasını doğru uyguladığımızı gösteriyor.
