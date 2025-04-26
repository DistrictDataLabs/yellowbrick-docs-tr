.. -*- mode: rst -*-

Kullanıcı Testi Talimatları
==========================

Yellowbrick projesinin alfa testini yapmamıza yardımcı olacak kişiler arıyoruz!
Yardım etmek basittir: Bu *Başlarken* kılavuzundaki kavramları seçtiğiniz küçük ila orta büyüklükteki bir veri kümesine uygulayan bir not defteri oluşturun. Örnekleri veri kümesiyle birlikte inceleyin ve seçenekleri değiştirmeye ve mümkün olduğunca özelleştirmeye çalışın. Örneklerinizle kodu çalıştırdıktan sonra `alfa test anketimize <https://goo.gl/forms/naoPUMFa1xNcafY83>`__ yanıt verin!

Birinci Adım: Anket
~~~~~~~~~~~~~~~~~~~~~~
Lütfen anketi açın ve almak istediğimiz
geri bildirimleri öğrenin. Yellowbrick'teki hataları belirlemekle çok ilgileniyoruz. Lütfen jupyter not defterinize hata üreten tüm hücreleri ekleyin, böylece sorunu yeniden üretebiliriz.

İkinci Adım: Veri Seti
~~~~~~~~~~~~~~~~~~

Kendi çok değişkenli veri setinizi seçin; Yellowbrick'te çalıştırabileceğimiz veri setleri ne kadar çoksa (örneğin farklıysa), uç durumları ve istisnaları keşfetme olasılığımız o kadar artar! Veri setinizin Scikit-Learn ile modellemeye uygun olması gerektiğini unutmayın. Özellikle, hedefi aşağıdaki denetlenen
öğrenme görevlerine uygun bir veri kümesi seçmenizi öneririz:

- `Regression <https://en.wikipedia.org/wiki/Regression_analysis>`__
(hedef sürekli bir değişkendir)
- `Classification <https://en.wikipedia.org/wiki/Classification_in_machine_learning>`__
(hedef ayrık bir değişkendir)

Her iki analiz türüne de uygun veri kümeleri vardır;
her iki durumda da bu not defterindeki test metodolojisini her iki görev türü için de (veya her ikisi için de) kullanabilirsiniz. Bir veri kümesi bulmak için, aşağıdaki yerleri denemenizi öneririz:

- `UCI Makine Öğrenmesi Deposu <http://archive.ics.uci.edu/ml/>`__
- `MLData.org <http://mldata.org/>`__
- `Harika Genel
Veri Kümeleri <https://github.com/caesar0301/awesome-public-datasets>`__

Kendi veri kümenizi seçmenizden memnuniyet duyarız, ancak en azından test sonuçlarınızı içeren not defterini incelememiz için
kamuya açık hale getirmenizi rica ediyoruz. Veriler de kamuya açıksa (veya
birincil katkıda bulunanlarla paylaşmaya istekliyseniz) bu, hataları ve gerekli özellikleri çok daha kolay bir şekilde anlamamıza yardımcı olacaktır!

Üçüncü Adım: Not Defteri
~~~~~~~~~~~~~~~~~~~~~

GitHub deposunda bir not defteri oluşturun. Aşağıdakileri öneriyoruz:

1. Yellowbrick deposunu çatallandırın
2. ``examples`` dizininde, GitHub kullanıcı adınızla adlandırılmış bir dizin oluşturun
3. ``testing`` adlı bir not defteri oluşturun, yani examples/USERNAME/testing.ipynb

Alternatif olarak, bize Gist veya kendi
deponuz aracılığıyla bir not defteri gönderebilirsiniz. Ancak, Yellowbrick'i çatallandırırsanız, örneğinizin galerimize eklenmesi için bir çekme
isteği başlatabilirsiniz!

Dördüncü Adım: Yellowbrick ve Scikit-Learn ile modelleme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Aşağıdakileri not defterine ekleyin:

- Markdown'da bir başlık
- Veri setinin açıklaması ve nereden elde edildiği
- Verileri bir Pandas veri çerçevesine veya NumPy matrisine yükleyen bir bölüm

Ardından aşağıdaki modelleme etkinliklerini gerçekleştirin:

- Scikit-Learn ve Yellowbrick kullanarak özellik analizi
- Scikit-Learn ve Yellowbrick kullanarak tahmin edici uydurma

``examples`` dizinimizi takip edebilirsiniz (`examples.ipynb <https://github.com/DistrictDataLabs/yellowbrick/blob/master/examples/examples.ipynb>`__ adresine bakın)
veya kendi özel görselleştiricilerinizi bile oluşturabilirsiniz! Amaç, veri yüklemesinden tahmin edicilere kadar görselleştiricilerle uçtan uca bir model oluşturmanızdır.

**ÖNEMLİ**: Lütfen üçüncü adım için aldığınız tüm hataları ve
tüm geri izlemeleri kaydettiğinizden emin olun!

Beşinci Adım: Geri Bildirim
~~~~~~~~~~~~~~~~~~~

Son olarak, oluşturduğumuz Google Formu aracılığıyla geri bildirim gönderin:

https://goo.gl/forms/naoPUMFa1xNcafY83

Bu form, sorunların oluşturulmasını ve yönetimini koordine edebilmemiz için birden fazla gönderimi ve hatayı bir araya getirmemize olanak tanır. Bir hatayı veya özellik isteğini bildiren ilk kişi siz olursanız, oluşturulan sorun hakkında bilgilendirildiğinizden emin olacağız (sizi Github kullanıcı adınızı kullanarak etiketleyeceğiz)!

Altıncı Adım: Teşekkürler!
~~~~~~~~~~~~~~~~~

Yellowbrick'i daha iyi hale getirmemize yardımcı olduğunuz için teşekkür ederiz! Kütüphaneyi genişleteceğini düşündüğünüz özellikler için çekme
istekleri görmeyi çok isteriz. Ayrıca, sizin de katılmanızı isteyeceğimiz bir kullanıcı çalışması yapacağız. Yellowbrick'ten daha fazla harika şey için bizi izlemeye devam edin!