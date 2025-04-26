.. -*- mod: ilk -*-

Hızlı Başlangıç
===========

Yellowbrick'te yeniyseniz, bu kılavuzla başlamanıza ve makine kayıtlarınıza iş akışınıza görselleştiricileri dahil depolamaya yardımcı olacaktır. Fakat başlamadan önce, iyileşme ortamlarıyla ilgili düşüşlerin olması gereken birkaç tane bulunmuyor.

Yellowbrick'in iki temel bağlılığı bulunmaktadır: `Scikit-Learn <http://scikit-learn.org/>`_ ve `Matplotlib <http://matplotlib.org/>`_. Şayet bu Python depolarınız yoksa, Yellowbrick'le birlikte kurulacaktır. Yellowbrick, Scikit-Learn 0.18 versiyonu veya üstü ve Matplotlib 2.0 versiyonu ve üstü ile en iyi şekilde gözlemlendiniz. Her iki paketin de derlenmesi için Windows gibi sistemler üzerinde derlenmesi zor olan bazı C kodlarında değişiklik yaşanmaktadır. Sorun yaşıyorsanız `Anaconda <https://anaconda.org>`_ gibi bu paketleri içeren bir Python dağıtım paketini .

Yellowbrick ayrıca `Pandas <http://pandas.pydata.org/>`_ veri çerçevelerinin yanında `Jupyter Notebook <http://jupyter.org/>`_ içinde yaygın olarak kullanılır. Defterler özellikle kod ve görselleştirmeleri koordine etmeyi kolaylaştırır, ancak Yellowbrick'i normal Python betiklerinin içinde de kullanabilir, ya rakamları diske kaydedebilir ya da rakamları bir GUI penceresinde gösterebilirsiniz. Bununla ilgili sorun yaşıyorsanız lütfen Matplotlib'in `arka uçlar belgelerine <https://matplotlib.org/faq/usage_faq.html#what-is-a-backend>`_ bakın.

.. NOT:: Jupyter, Pandas ve metin görselleştiricileri için NLTK gibi diğer yardımcı kütüphaneler Yellowbrick ile birlikte kurulmaz ve ayrı olarak kurulmalıdır.

Kurulum
------------

Yellowbrick, Python 2.7 ve üst dayanıklılık ile uyumludur ancak Yellowbrick'in tüm işlevlerinden faydalanmak için Python 3.5 ve üst dayanıklılığın kullanımı tercih edilmektedir. Yellowbrick`i kurmanın en kolay yolu, PyPI_`den Python`un tercih edilen paket kurulumcusu pip_ kullanımıdır.

.. kod bloğu:: bash 

$ pip sarı tuğlayı yükle

.. _PyPI: https://pypi.python.org/pypi/yellowbrick
.. _pip: https://docs.python.org/3/installing/

Yellowbrick'in aktif bir proje olduğunu ve daha fazla görselleştirici ve güncelleme içeren yeni sürümleri düzenli olarak yayınladığını unutmayın. Yellowbrick'i son sürüme yükseltmek için pip'i aşağıdaki gibi kullanın.

.. code-block:: bash

$ pip install -u yellowbrick

Ayrıca, Yellowbrick ile iyi çalışan Scikit-Learn, matplotlib veya diğer üçüncü taraf yardımcı programlarını en son sürümlerine güncellemek için ``-u`` bayrağını kullanabilirsiniz.

Windows veya Anaconda kullanıyorsanız, `conda <https://conda.io/docs/intro.html>`_ yardımcı programından yararlanarak `Anaconda Yellowbrick paketini <https://anaconda.org/DistrictDataLabs/yellowbrick>`_ yükleyebilirsiniz:

.. code-block:: bash

conda install -c districtdatalabs yellowbrick

.. UYARI:: Anaconda ile Linux'a matplotlib yüklerken `bilinen bir hata <https://github.com/DistrictDataLabs/yellowbrick/issues/205>`_ var. Sorun yaşıyorsanız lütfen GitHub'da bize bildirin.

Kurulduktan sonra Yellowbrick'i hem Python'da hem de Jupyter not defterlerinde hatasız bir şekilde içe aktarabilmeniz gerekir. Matplotlib nedeniyle Yellowbrick'in bazı engelleri aşmadan sanal bir ortamda çalışmadığını unutmayın.

Yellowbrick Kullanımı
-----------------
Yellowbrick API'si özellikle Scikit-Learn ile uyumlu çalışacak şekilde tasarlanmıştır. Bu nedenle birincil arayüz bir ``Görselleştirici``dir -- bir görselleştirme üretmek için verilerden öğrenen bir nesne. Görselleştiriciler Scikit-Learn `Estimator <http://scikit-learn.org/stable/developers/contributing.html#apis-of-scikit-learn-objects>`_ nesneleridir ve çizim yöntemleriyle birlikte benzer bir arayüze sahiptir. Görselleştiricileri kullanmak için, Scikit-Learn modeliyle aynı iş akışını kullanmanız, görselleştiriciyi içe aktarmanız, onu örneklemeniz, görselleştiricinin ``fit()`` yöntemini çağırmanız, ardından görselleştirmeyi işlemek için görselleştiricinin ``poof()`` yöntemini çağırmanız yeterlidir; bu sihiri gerçekleştirir!

Örneğin, bir modeli uydurmadan önce özellik analizi gerçekleştirmek için kullanılan dönüştürücüler gibi davranan birkaç görselleştirici vardır. İşte paralel koordinatlarla yüksek boyutlu bir veri kümesini görselleştirmek için bir örnek:

.. code-block:: python

from yellowbrick.features import ParallelCoordinates

visualizer = ParallelCoordinates()
visualizer.fit_transform(X, y)
visualizer.poof()

Gördüğünüz gibi, iş akışı bir Scikit-Learn dönüştürücüsünü kullanmaya çok benzer ve görselleştiricilerin Scikit-Learn yardımcı programlarıyla birlikte entegre edilmesi amaçlanmıştır. Görselleştirmenin nasıl çizileceğini değiştiren argümanlar, Scikit-Learn modellerine hiperparametrelerin nasıl dahil edildiğine benzer şekilde, örnekleme sırasında görselleştiriciye geçirilebilir.

``poof()`` yöntemi çizimi sonlandırır (başlıklar, eksen etiketleri vb. ekleyerek) ve ardından sizin adınıza görüntüyü işler. Bir Jupyter not defterindeyseniz, görüntü yalnızca görünmelidir. Bir Python betiğindeyseniz, görselleştirmenin etkileşimli biçimde olduğu bir GUI penceresi açılmalıdır. Ancak, aşağıdaki gibi bir dosya yolu geçirerek görüntüyü diske de kaydedebilirsiniz:

.. code-block:: python

visualizer.poof(outpath="pcoords.png")

Dosya adının uzantısı, görüntünün nasıl işleneceğini belirler, .png uzantısına ek olarak, .pdf de yaygın olarak kullanılır.

.. NOT:: Yellowbrick'e veri girişi, Scikit-Learn'e veri girişiyle aynıdır: ``(n,m)`` şeklinde iki boyutlu bir matris olan ``X`` adlı bir veri kümesi; burada ``n`` örnek sayısı (satırlar) ve ``m`` özellik sayısı (sütunlar)dır. ``X`` adlı veri kümesi bir Pandas DataFrame, bir Numpy dizisi veya hatta bir Python liste listesi olabilir. İsteğe bağlı olarak, hedef değişkeni (denetimli öğrenmede) temsil eden bir vektör ``y`` de giriş olarak sağlanabilir. Hedef ``y`` ``n`` uzunluğunda olmalıdır -- ``X`` deki satırlarla aynı sayıda elemana sahip olmalı ve bir Pandas Serisi, Numpy dizisi veya Python listesi olabilir.

Görselleştiriciler ayrıca değerlendirme, hiperparametre ayarlama ve algoritma seçimi için Scikit-Learn modellerini sarabilir. Örneğin, bir sınıflandırma raporunun görsel ısı haritasını oluşturmak, bir sınıflandırıcıdaki her sınıf için hassasiyeti, geri çağırmayı, F1 puanını ve desteği görüntülemek için, tahmin ediciyi aşağıdaki gibi bir görselleştiriciye sarın:

.. code-block:: python

from yellowbrick.classifier import ClassificationReport
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
visualizer = ClassificationReport(model)

visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
visualizer.poof()

Sınıflandırıcı modelinin görsel değerlendirmesini eklemek için yalnızca iki ek kod satırı, sınıflandırma tahmin edicisini saran bir ``ClassificationReport`` görselleştiricisinin örneklenmesi ve ``poof()`` yöntemine bir çağrı gereklidir. Bu şekilde, Görselleştiriciler makine öğrenimi iş akışını kesintiye uğratmadan *geliştirir*.

.. TODO:: Görsel işlem hatları ve metin analizinin incelenmesi.

Sınıf tabanlı API, Scikit-Learn ile doğrudan entegre olmak üzere tasarlanmıştır, ancak bazen sadece hızlı bir görselleştirmeye ihtiyaç duyduğunuz zamanlar olur. Yellowbrick, bundan doğrudan yararlanmak için hızlı işlevleri destekler. Örneğin, iki görsel tanılama bunun yerine aşağıdaki gibi uygulanabilirdi:

.. code-block:: python

from sklearn.linear_model import LogisticRegression

from yellowbrick.features import parallel_coordinates
from yellowbrick.classifier import classification_report

# Paralel koordinatları görüntüler
g = parallel_coordinates(X, y)

# Sınıflandırma raporunu görüntüler
g = classification_report(LogisticRegression(), X, y)

Bu hızlı işlevler, makine öğrenimi iş akışı üzerinde size biraz daha az kontrol sağlar, ancak talep üzerine tanılamaları hızla sağlar ve keşif süreçlerinde çok faydalıdır.

Açıklamalar
-----------

Makine öğrenimi iş akışında görselleştiricilerin kullanımına dair basit bir örnek olarak regresyon analizini ele alalım. `UCI Makine Öğrenimi Deposu <https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset>`_'ne yüklenen veriye dayalı bir `bisiklet paylaşım veri seti <https://s3.amazonaws.com/ddl-data-lake/yellowbrick/bikeshare.zip>`_ kullanarak, mevsim, hava durumu veya tatil olup olmadığı gibi özelliklere göre belirli bir saatte kiralanan bisiklet sayısını tahmin etmek istiyoruz.

.. not:: Pandas'a yüklemeyi biraz daha kolaylaştırmak için UCI ML deposundaki veri setini güncelledik; `Veri kümesinin Yellowbrick versiyonunu <https://s3.amazonaws.com/ddl-data-lake/yellowbrick/bikeshare.zip>`_ indirdiğinizden emin olun.

Veri setini indirip mevcut çalışma dizininize açtıktan sonra, verilerimizi şu şekilde yükleyebiliriz:

.. code-block:: python

import pandas as pd

data = pd.read_csv('bikeshare.csv')
X = data[[
"season", "month", "hour", "holiday", "weekday", "workingday",
"weather", "temp", "feelslike", "humidity", "windspeed"
]]
y = data["riders"]

Makine öğrenimi iş akışı, belirli bir veri setine uyan bir modeli benzersiz bir şekilde tanımlayan özellikler, algoritma ve hiperparametrelerin bir kombinasyonu olan *model seçimi üçlüleri* oluşturma sanatıdır. Özellik seçimimizin bir parçası olarak, birbirleriyle doğrusal bir ilişkiye sahip olan özellikleri belirlemek istiyoruz, bu da modelimize kovaryans katabilir ve OLS'yi bozabilir (bizi özellikleri kaldırmaya veya düzenleme kullanmaya yönlendirir). Tüm özellik çiftleri arasındaki Pearson korelasyonlarını hesaplamak için Rank2D_ görselleştiricisini şu şekilde kullanabiliriz:

.. _Rank2D: http://www.scikit-yb.org/en/latest/api/yellowbrick.features.html#module-yellowbrick.features.rankd

.. code-block:: python

from yellowbrick.features import Rank2D

visualizer = Rank2D(algorithm="pearson")
visualizer.fit_transform(X)
visualizer.poof()

.. image:: images/quickstart/bikeshare_rank2d.png

Bu şekil bize, ızgaradaki her hücrenin x ve y eksenlerinde sırayla tanımlanan ve rengi korelasyonun büyüklüğünü gösteren iki özelliği temsil ettiği özellik çiftleri arasındaki Pearson korelasyonunu gösterir. 1,0'lık bir Pearson korelasyonu, iki özellik arasında güçlü, pozitif ve doğrusal bir ilişki olduğu anlamına gelir.
n değişken çiftleri ve -1.0 değeri güçlü bir negatif, doğrusal ilişkiyi gösterir (sıfır değeri ilişki olmadığını gösterir). Bu nedenle daha fazla tanımlamak için koyu kırmızı ve koyu mavi kutular arıyoruz.

Bu grafikte özellik 7'nin (sıcaklık) ve özellik 9'un (hissedilen) güçlü bir korelasyona sahip olduğunu ve ayrıca özellik 0'ın (mevsim) özellik 1 (ay) ile güçlü bir korelasyona sahip olduğunu görüyoruz. Bu mantıklı görünüyor; dışarıda hissettiğimiz görünen sıcaklık gerçek sıcaklığa ve diğer hava kalitesi faktörlerine bağlıdır ve yılın mevsimi ay ile tanımlanır! Daha derinlemesine incelemek için, bu ilişkileri incelemek üzere `JointPlotVisualizer <http://www.scikit-yb.org/en/latest/api/yellowbrick.features.html#module-yellowbrick.features.jointplot>`_ kullanabiliriz.

.. code-block:: python

from yellowbrick.features import JointPlotVisualizer

visualizer = JointPlotVisualizer(feature='temp', target='feelslike')
visualizer.fit(X['temp'], X['feelslike'])
visualizer.poof()

.. image:: images/quickstart/temp_feelslike_jointplot.png

Bu görselleştirici, y ekseninde görünen sıcaklığın ve x ekseninde ölçülen gerçek sıcaklığın dağılım diyagramını çizer ve basit bir doğrusal regresyon kullanarak en iyi uyumu gösteren bir çizgi çizer. Ek olarak, tek değişkenli dağılımlar, sıcaklık için x ekseninin üstünde ve feellike için y ekseninin yanında histogram olarak gösterilir. ``JointPlotVisualizer``, özelliklerin çok güçlü pozitif korelasyonunun yanı sıra her özelliğin aralığı ve dağılımının genel bir görünümünü sunar. Eksenlerin sıfır ile bir arasındaki boşluğa göre normalleştirildiğini unutmayın; bu, makine öğreniminde bir özelliğin diğerine olan etkisini azaltmak için kullanılan yaygın bir tekniktir.

Bu çizim çok ilginç; ilk olarak, veri setinde feellike'ın yaklaşık olarak 0,25'e eşit olduğu bazı aykırı değerler var gibi görünüyor. Bu örneklerin, veri girişi hatalarını temsil edebilecekleri için son modelin kalitesini iyileştirmek amacıyla manuel olarak kaldırılması gerekebilir. İkinci olarak, daha aşırı sıcaklıkların algılanan sıcaklıkta abartılı bir etki yarattığını görebiliriz; ne kadar soğuksa, insanların buna inanma olasılığı o kadar yüksektir ve ne kadar sıcaksa, o kadar sıcak görünür. Orta sıcaklıklar öyle hissettirir. Bu bize feellike'ın temp'den daha iyi bir özellik olabileceği ve regresyon analizimizde sorunlara neden oluyorsa, muhtemelen temp değişkenini feellike lehine kaldırmamız gerektiği sezgisini verir.

Bu noktada, modelimizi eğitebiliriz; modelimize doğrusal bir regresyon uygulayalım ve artıkları çizelim.

.. code-block:: python

from yellowbrick.regressor import ResidualsPlot
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

# Eğitim ve test setleri oluştur
X_train, X_test, y_train, y_test = train_test_split(
X, y, test_size=0.1
)

visualizer = ResidualsPlot(LinearRegression())
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
visualizer.poof()

.. image:: images/quickstart/bikeshare_ols_residuals.png

Artıklık grafiği, hatayı tahmin edilen değere göre gösterir ve modelde heteroskedastisite aramamızı sağlar; örneğin, hedefte hatanın en büyük olduğu bölgeler. Kalıntıların şekli, OLS'nin (sıradan en küçük kareler) modelimizin bileşenlerinden (özelliklerden) en çok nerede etkilendiğini bize güçlü bir şekilde bildirebilir. Bu durumda, tahmin edilen değer ne kadar düşükse (sürücü sayısı ne kadar düşükse), hatanın o kadar düşük olduğunu, ancak tahmin edilen sürücü sayısı ne kadar yüksekse hatanın da o kadar yüksek olduğunu görebiliriz. Bu, modelimizin hedefin belirli bölgelerinde daha fazla gürültüye sahip olduğunu veya iki değişkenin eş doğrusal olduğunu, yani ilişkilerindeki gürültü değiştikçe hata enjekte ettiklerini gösterir.

Kalıntılar grafiği ayrıca modelin hatayı nasıl enjekte ettiğini gösterir, ``residuals = 0`` noktasındaki kalın yatay çizgi hata olmadığını ve bu çizginin üstünde veya altında herhangi bir nokta hatanın büyüklüğünü gösterir. Örneğin, kalıntıların çoğu negatiftir ve puan ``gerçek - beklenen`` olarak hesaplandığından, bu beklenen değerin çoğu zaman gerçek değerden daha büyük olduğu anlamına gelir, örneğin modelimiz öncelikle gerçek sürücü sayısından daha fazlasını tahmin ediyor. Ayrıca, kalıntı grafiğinin sağ üst kısmında, model uzayında ilginç bir etkiyi gösteren çok ilginç bir sınır var; muhtemelen bazı özellikler o modelin bölgesinde güçlü bir şekilde ağırlıklandırılmıştır.

Son olarak kalıntılar eğitim ve test kümesine göre renklendirilir. Bu, eğitim ve test bölmeleri oluştururken hataları belirlememize yardımcı olur. Test hatası eğitim hatasıyla uyuşmuyorsa, modelimiz ya aşırı uyum sağlar ya da yetersiz uyum sağlar. Aksi takdirde, bölmeleri oluşturmadan önce veri kümesini karıştırmada bir hata olabilir.

Bu model için belirleme katsayımız 0,328 olduğundan, *düzenleme* kullanarak daha iyi bir model uydurup uyduramayacağımıza bakalım ve aynı anda başka bir görselleştiriciyi inceleyelim.

..code-block:: python

import numpy as np

from sklearn.linear_model import RidgeCV
from yellowbrick.regressor import AlphaSelection

alphas = np.logspace(-10, 1, 200)
visualizer = AlphaSelection(RidgeCV(alphas=alphas))
visualizer.fit(X, y)
visualizer.poof()

.. image:: images/quickstart/bikeshare_ridge_alphas.png

Model ailelerini incelerken, dikkate alınması gereken birincil şey modelin nasıl daha *karmaşık* hale geldiğidir. Model karmaşıklık açısından arttıkça, model daha fazla aşırı uyum sağladığı ve görülmeyen verilere genelleştirilemediği için varyans nedeniyle oluşan hata artar. Ancak, model ne kadar basit olursa, önyargı nedeniyle oluşan hata olasılığı o kadar artar; model yetersiz uyum sağlar ve bu nedenle hedefini daha sık ıskalar. Bu nedenle çoğu makine öğreniminin amacı, önyargı ve varyans arasında bir orta yol bularak *tam olarak yeterince karmaşık* bir model oluşturmaktır.

Doğrusal bir model için karmaşıklık, özelliklerin kendisinden ve modele göre atanan ağırlıklarından gelir. Dolayısıyla doğrusal modeller, açıklayıcı bir sonuca ulaşan *en az sayıda özelliği* bekler. Bunu başarmak için bir teknik, katsayıların ağırlıklarını birbirleriyle normalleştiren ve karmaşıklığı cezalandıran alfa adı verilen bir parametrenin tanıtılması olan *düzenlemedir*. Alfa ve karmaşıklık ters bir ilişkiye sahiptir, alfa ne kadar yüksekse modelin karmaşıklığı o kadar düşüktür ve bunun tersi de geçerlidir.

Bu nedenle soru, alfayı nasıl seçeceğinizdir. Bir teknik, çapraz doğrulama kullanarak bir dizi modeli uydurmak ve en düşük hataya sahip alfayı seçmektir. ``AlphaSelection`` görselleştiricisi, düzenlemenin davranışını gösteren görsel bir gösterimle tam olarak bunu yapmanızı sağlar. Yukarıdaki şekilde görebileceğiniz gibi, alfa değeri arttıkça hata, seçtiğimiz değere (bu durumda 3.181) kadar azalır ve hata artmaya başlar. Bu, önyargı/varyans dengelerini hedeflememizi ve düzenleme yöntemlerinin ilişkisini (örneğin Ridge ve Lasso) keşfetmemizi sağlar.

Artık son modelimizi eğitebilir ve ``PredictionError`` görselleştiricisiyle görselleştirebiliriz:

.. code-block:: python

from sklearn.linear_model import Ridge
from yellowbrick.regressor import PredictionError

visualizer = PredictionError(Ridge(alpha=3.181))
visualizer.fit(X_train, y_train)
visualizer.score(X_test, y_test)
visualizer.poof()

.. image:: images/quickstart/bikeshare_ridge_prediction_error.png

Tahmin hatası görselleştiricisi gerçek (ölçülen) ile beklenen (tahmin edilen) değerleri birbirine göre çizer. Noktalı siyah çizgi sıfır hatayı gösteren 45 derecelik çizgidir. Artıklar grafiği gibi bu da hatanın nerede ve hangi büyüklükte meydana geldiğini görmemizi sağlar.

Bu grafikte, örnek yoğunluğunun çoğunun 200'den az sürücü olduğunu görebiliriz. Daha fazla bölgeselliği hesaba katan bir regresyona uyması için ortogonal eşleştirme takibi veya eğrileri denemek isteyebiliriz. Ayrıca, kalıntı grafiğindeki o tuhaf topolojinin Ridge regresyonu kullanılarak düzeltilmiş gibi göründüğünü ve modelimizde büyük ve küçük değerler arasında biraz daha fazla denge olduğunu da not edebiliriz. Potansiyel olarak Ridge düzenlemesi, iki özellik arasında yaşadığımız bir kovaryans sorununu çözdü. Diğer model formlarını kullanarak analizimizde ilerledikçe, sonuçlarımızı hızla karşılaştırmak ve görmek için görselleştiricileri kullanmaya devam edebiliriz.

Umarım bu iş akışı, Görselleştiricileri Scikit-Learn ile makine öğrenimine nasıl entegre edeceğiniz konusunda size bir fikir verir ve bunları işinizde kullanmanız ve kendi çalışmanızı yazmanız için size ilham verir! Yellowbrick ile çalışmaya başlama hakkında ek bilgi için :doc:`tutorial`'a bakın. Bundan sonra :doc:`api/index`'te ayrıntılı olarak açıklanan belirli görselleştiriciler hakkında hızla bilgi edinebilirsiniz.