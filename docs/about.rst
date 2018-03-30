Hakkında
=====

.. image:: images/yellowbrickroad.jpg

Resim sahibi QuatroCinco_, izniyle kullanılmıştır, Flickr Creative Commons.

Yellowbrick, görsel analiz ve tanımlama araçları ile birlikte Scikit-Learn API_ `yi genişleten açık kaynak kodlu sade bir Python Projesidir. Yellowbrick API, Matplotlib`i  de kapsayarak yayınlamaya hazır figür ve interaktif veri keşfi oluşturmayı sağlarken bir yandan da geliştiricilere ayrıntılı figür kontrolu imkanı sağlamaktadır. Yellowbrick kullanıcılar için; Makine öğrenimi modellerinin performansını geliştirme, güvenirliliğini sağlama, değer tahmininde bulunma ve makine oğrenmesi iş akışında karşılaşılan problemleri teşhis etmede yardımcı olabilmektedir.

Son dönemlerde makine öğrenimi iş akışının büyük bir kısmı; grid search yöntemi, standartlaştırılmıs API ler ve GUI (Kullanıcı Grafik Arayüzü) tabanlı uygulamalar yoluyla otomatize edilmiştir. Bununla birlikte, pratikte insan sezgisi ve rehberliği, kaliteli modeller üzerinde detaylı arama yöntemlerine göre daha efektif odaklanma sağlamaktadir. Görsel model seçim işlemi yoluyla, veri bilimcileri; hatalara ve yanılgılara düşmeden finale, açıklanabilir modellere doğru ilerleyiş gösterebilmektedir.

Yellowbrick kütüphanesi, makine öğrenimi için veri bilimcilerine model seçim sürecine yön vermelerine olanak sağlayan bir tanı görselleştirme platformudur. Yellowbrick, Scikit Learn API`sini yeni bir temel obje ile genişletmiştir: Görselleştirici.  Görselleştiriciler, çok boyutlu verilerin dönüşümü sırasında görsel tanılar sunarak, Scikit-Learn işlem sürecinin bir parçası olarak görsel modellerin uymasını ve dönüşümünü sağlamaktadır. 

Model Seçimi
---------------
Makine öğrenimi tartışmaları sık sık model seçimi üzerine tekil odaklanma ile karakterize edilir. Gerek lojistik regresyon, karar ağaçları, Bayesian methodları veya yapay sinir ağları olsun; makine öğrenmesi uygulayıcıları tercihlerini genellikle hızlı bir şekilde açıklarlar. Bunun nedeni çoğunlukla tarihseldir. Modern üçüncü parti makine öğrenimi kütüphaneleri birçok modelin yayılmasını önemsiz olarak gösterse de, geleneksel olarak bu algoritmalardan birinin bile uygulaması ve ayarlanması yıllar süren çalışma gerektirmiştir. Sonuç olarak makine öğrenmesi uygulayıcıları diğerlerine göre daha belirgin  (ve muhtemelen daha yaygın olan) algoritmaları daha çok tercih etmeye yönelmiştir.

Bununla birlikte, model seçimi basit şekilde "doğru" ya da "yanlış" algoritmayı seçmekten biraz daha nüanslıdır. Pratik olarak iş akışı şunları içermektedir:

  1. en küçük ve en kestirici tahmin kümesi seçimi ya da oluşturumu
  2. bir dizi algoritmaların bir model ailesinden seçimi ve
  3. performans optimizesi için algoritma hiperparametlerinin ayarlanması

Kumar et al tarafından **model seçim üçlüsü** 2015 yılı SIGMOD_ makalesinde ilk defa tanımlanmıştır. In their paper, which concerns the development of next-generation database systems built to anticipate predictive modeling, the authors cogently express that such systems are badly needed due to the highly experimental nature of machine learning in practice. "Model selection," they explain, "is iterative and exploratory because the space of [model selection triples] is usually infinite, and it is generally impossible for analysts to know a priori which [combination] will yield satisfactory accuracy and/or insights."

İsim Kökeni
-----------
Yellowbrick Paketi, Amerikan yazar L. Frank Baum tarafından 1900 yılında yazılan çocuk romanı **The Wonderful Wizard of Oz** (Oz Büyücüsü) içerisinde geçen kurgusal bir elementten adını almıştır. Kitapta, Roman kahramanı Dorothy Gale, Emerald Şehri`ndeki hedefine ulaşabilmesi için sarı tuğlalı yolu (yellowbrick) takip etmesi gerekmektedir.

Wikipedia_ `da şu şekilde geçmektedir:
    "Bu yol ilk olarak Oz Büyücüsü`nün üçüncü bölümünde tanıtılmıştır. Yol, Oz Diyarı`nin doğu çeyreğinin kalbinde bulunan Munchkin ülkesinden başlamaktadır. Bu yol; takip eden herkese,en son varış yeri —kıtanın tam ortasında bulunan Oz emparyel başkenti olan Emerald şehrine kadar rehberlik etmektir. Kitapta, romanın ana karakteri Dorothy, büyücüyü aramaya başlamadan önce bu yolu bulması gerekmektedir. Bunun sebebi çeşitli film adaptasyonlarında gösterilenin aksine, Kansas`ta çıkan hortumun çiftlik evini bu yola yakın biryerde bırakmamasıdır. Munchkins yerlileriyle ve onların sevilen dostu Kuzey'in iyi kalpli cadısı ile yapılan konsey sonrasında, Dorothy bu yolu aramaya başlar ve yakınlarında birçok patikalar ve yolları görür, (Herbiri çeşitli yönlere gitmekte). Neyseki parlak sarı tuğlalarla kaplanmış yolu bulması çok uzun sürmez."

Yellowbrick Ekibi
----

Yellowbrick is is developed by data scientists who believe in open source and the project enjoys contributions from Python developers all over the world. The project was started by `@rebeccabilbro`_ ve `@bbengfort`_ as an attempt to better explain machine learning concepts to their students; they quickly realized, however, that the potential for visual steering could have a large impact on practical data science and developed it into a high-level Python library.

Yellowbrick is incubated by `District Data Labs`_, an organization that is dedicated to collaboration and open source development. As part of District Data Labs, Yellowbrick was first introduced to the Python Community at `PyCon 2016 <https://youtu.be/c5DaaGZWQqY>`_ in both talks and during the development sprints. The project was then carried on through DDL Research Labs (semester-long sprints where members of the DDL community contribute to various data related projects).

Lisans
-------

Yellowbrick açık kaynaklı bir projedir ve `lisansı <https://github.com/DistrictDataLabs/yellowbrick/blob/master/LICENSE.txt>`_ FOSS `Apache 2.0 <http://www.apache.org/licenses/LICENSE-2.0>`_ uygulaması olup Apache Software Foundation lisanslı bir uygulamasıdır. `Sade bir dil <https://tldrlegal.com/license/apache-license-2.0-(apache-2.0)>`_ ile ifade etmek istersek Yellowbrick'i ticari amaçlı kullanabilir, kaynak kodu değiştirilebilir ve paylaşabilirsiniz, hatta alt lisans edinebilirsiniz. Bizler Yellowbrick'i kullanmanızı, yararlanmanızı ve Yellowbrick'le ilgili güzel şeyler yaparsanız geri katkıda bulunmanızı isteriz. 

Bununla birlikte sizden talep ettğimiz birkaç gereksinim bulunmakta. Öncelikle Yellowbrick kaynak kodunu dağıtırken veya paylaşırken yazılım depomuzun dizininde bulunan ve içerisinde telif hakkımız ve lisansımızın bulunduğu `LICENSE.txt <https://github.com/DistrictDataLabs/yellowbrick/blob/master/LICENSE.txt>`_ dosyasını lütfen dahil edin. Ek olarak projemiz içerisinde "NOTICE" dosyası oluşturmuşsak  ayrıca bu dosyayı da kaynak paylaşım dosyanıza eklemeniz gerekmektedir. "NOTICE" dosyası bu projeye emek vermiş kişilere yönelik atıfların ve teşekkürlerin bulunduğu bir dosya olacaktır. Son olarak yazılımımızı kullanımınıza yönelik hiçbir şekilde District Data Labs veya Yellowbrick'e katkıda bulunan kişileri sorumlu olarak tutamazsınız ve yine aynı şekilde isimlerimizi, logolarımızı, markamızı mesul tutamazsınız.

Bu gereksinimlerin adil olduğuna düşünüyoruz ve açık kaynağa gerçekten inanıyoruz. Eğer yazılımımız üzerinde değişiklik yaparsanız, ticari veya akademide kullanın ya da başka bir ilginiz varsa, bunu duymaktan memnun oluruz. 


.. _SIGMOD: http://cseweb.ucsd.edu/~arunkk/vision/SIGMODRecord15.pdf
.. _Wikipedia: https://en.wikipedia.org/wiki/Yellow_brick_road
.. _`@rebeccabilbro`: https://github.com/rebeccabilbro
.. _`@bbengfort`: https://github.com/bbengfort
.. _`District Data Labs`: http://www.districtdatalabs.com/

Sunumlar
-------------

Yellowbrick, birkaç konferans ve sergilerde yer almaktan memnun olmustur. Sunduğumuz videolar,konuşmalar ve sunumların Yellowbrick`i daha iyi anlamanıza yardımcı olacağına inanıyoruz.

Videolar:
    - `Visual Diagnostics for More Informed Machine Learning: Within and Beyond Scikit-Learn (PyCon 2016) <https://youtu.be/c5DaaGZWQqY>`_
    - `Visual Diagnostics for More Informed Machine Learning (PyData Carolinas 2016) <https://youtu.be/cgtNPx7fJUM>`_
    - `Yellowbrick: Steering Machine Learning with Visual Transformers (PyData London 2017) <https://youtu.be/2ZKng7pCB5k>`_

Slaytlar:
    - `Visualizing the Model Selection Process <https://www.slideshare.net/BenjaminBengfort/visualizing-the-model-selection-process>`_
    - `Visualizing Model Selection with Scikit-Yellowbrick <https://www.slideshare.net/BenjaminBengfort/visualizing-model-selection-with-scikityellowbrick-an-introduction-to-developing-visualizers>`_
    - `Visual Pipelines for Text Analysis (Data Intelligence 2017) <https://speakerdeck.com/dataintelligence/visual-pipelines-for-text-analysis>`_

.. _QuatroCinco: https://flic.kr/p/2Yj9mj
.. _API: http://scikit-learn.org/stable/modules/classes.html
