.. -*- mode: rst -*-
.. yellowbrick documentation master file, created by
    sphinx-quickstart on Tue Jul  5 19:45:43 2016.
    You can adapt this file completely to your liking, but it should at least
    contain the root `toctree` directive.

Yellowbrick: Makine Öğrenmesi Görselleştirme
===========================================

Yellowbrick`e hoşgeldiniz.

Şuanda Yellowbrick Türkçe dökümantasyonu üzerinde çalışmaktayız. Lütfen sayfamıza tekrar uğrayınız. 

Ayrıca yardım tekliflerinize açığız. Türkçe tercüme için katkıda bulunmak isterseniz `yellowbrick-docs-tr <https://github.com/DistrictDataLabs/yellowbrick-docs-tr>`_ adresine pull request sorgusu gönderebilirsiniz. Eğer Yellowbrick için katkıda bulunmak isterseniz `codebase <https://github.com/DistrictDataLabs/yellowbrick>`_ adresine pull request sorgusu gönderebilirsiniz. 

.. image:: images/visualizers.png

Yellowbrick, insanların model seçim sürecini yönlendirmeye izin veren "Görselleştirici" adı verilen Scikit-Learn API`sini genişleten görsel tanı araçları paketidir. Kısacası Yellowbrick, Scikit-Learn`i Matplotlib ile Scikit-Learn dökümantasyonuna gore birleştirirek modelinize göre görselleştirme üretmektedir. Yellowbrick ile ilgili daha fazlası için, lütfen bakınız: :doc:`about`.

Eğer Yellowbrick`te yeniyseniz, :doc:'quickstart' :doc:`quickstart` ya da bu kısmı geçerek :doc:`tutorial` kısmını ziyaret edebilirsiniz. Yellowbrick, düzenli olarak eklenen birçok görselleştiricisi ile zengin bir kütüphanedir. Spesifik Görselleştiriciler ve genişletilmiş kullanımları ile ilgili detayları  :doc:`api/index` kısmından bulabilirsiniz. Yellowbrick`e katkıda bulunmak ister misiniz? :ref:`contributing guide <contributing>` sayfasına göz atabilirsiniz. Şayet kullanıcı testi için başvurduysanız, :doc:`evaluation` sayfasına bakınız.(ve Teşekkür ederiz)

Görselleştiriciler
-----------

Görselleştiriciler, öncelikli amacı model seçim işlemine içgörü sağlamaya izin veren görselleştirmeleri oluşturan tahmin edicilerdir(veriden öğrenilen nesneler). Scikit-Learn`e göre, Görselleştiriciler; veri alanını görselleştirirken, dönüstürücülere benzeyebilir ya da "ModelCV" (e.g. `RidgeCV <http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeCV.html>`_, `LassoCV <http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LassoCV.html>`_) metodların calışmasında olduğu gibi, bir model tahmin edicisini sarabilmektedir. Yellowbrick`in öncelikli amacı, Scikit-Learn benzeri bir mantıksal API oluşturmaktır. En populer görselleştiricilerimizden bazıları şunlardır:

Özellik Görselleştirme
~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/features/rankd`: ilişki saptaması için özelliklerin ikili olarak sıralanması
- :doc:`api/features/pcoords`: özelliklerin yatay görselleştirilmesi
- :doc:`Radial Visualization <api/features/radviz>`: örneklerin bir dairesel alanda ayrılması
- :doc:`api/features/pca`: ana bileşenlere göre örneklerin gösterimi
- :doc:`api/features/importances`: spesifik bir model için önem veya doğrusal katsayısına göre özellik sıralaması
- :doc:`Scatter and Joint Plots<api/features/scatter>`: özellik seçimi ile doğrudan veri görselleştirimi

Klasifikasyon Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/classifier/class_balance`: sınıfların dagılımının modeli nasıl etkilediğinin gösterimi
- :doc:`api/classifier/classification_report`: precision, recall, ve F1 görsel temsili
- :doc:`ROC/AUC Curves <api/classifier/rocauc>`: işlem karakteristik eğrisi ve eğri altında kalan alan
- :doc:`Confusion Matrices <api/classifier/confusion_matrix>`: sınıf karar veriminin görsel açıklaması

Regresyon Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/regressor/peplot`: hedef alanı boyunca oluşan model hatalarının bulunması
- :doc:`api/regressor/residuals`: eğitim ve test verisi rezidüellerindeki farkın gösterimi
- :doc:`api/regressor/alphas`: alfa değer seçiminin regülasyonu nasıl etkilediğinin gösterimi

Kümesel Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`K-Elbow Plot <api/cluster/elbow>`: elbow metodu ve çeşitli metriklerin kullanımı ile k seçimi
- :doc:`Silhouette Plot <api/cluster/silhouette>`: siluet katsayısı değerlerinin görselleştirimi ile k seçimi

Metin Görselleştirmesi
~~~~~~~~~~~~~~~~~~

- :doc:`Term Frequency <api/text/freqdist>`: metin gövdesi içinde bulunan terimlerin dağılım sıklığının görselleştirimi
- :doc:`api/text/tsne`: proje dökümanına stokastik yakınsal yerleştirimin kullanılması

... ve daha fazlası! Yeni görselleştiriciler sürekli olarak eklenmekte; örnekleri kontrol ettiğinizden emin olun (ya da hatta `develop branch <https://github.com/DistrictDataLabs/yellowbrick/tree/develop>`_) ve yeni görselleştiricilerle ilgili fikirlerinizle katkıda bulunmaktan lütfen çekinmeyin.

Yardım İçin
------------

Yellowbrick, Matplotlib ve Scikit-Learn geleneğinde olduğu gibi kapsamlı ve herkesi davet eden bir projedir. Bu projelere benzer olarak `Python Software Foundation Code of Conduct <http://www.python.org/psf/codeofconduct/>`_ ölçütlerini takip etmeye çalışıyoruz. Lütfen yardıma ihtiyacınız olduğunda ya da herhangi bir katkıda bulunmak isterseniz veyahut bug bulursanız bizlere çekinmeden ulaşabilirsiniz.

Yellowbrick yardımı için ilk yol bu isteğinizi gönderi olarak `Google Groups Listserv <https://groups.google.com/forum/#!forum/yellowbrick>`_ kısmında paylaşmanız. Topluluk üyelerinin katılım gösterebildiği ve üyelerin birbirlerine cevap verebildigi email liste/forumu olup, burada en hızlı şekilde yanıt alabilirsiniz. Lutfen gruba katılmayı düşünün, boylelikle siz de soruları cevaplayabilirsiniz. Ayrıca `Stack Overflow <http://stackoverflow.com/questions/tagged/yellowbrick>`_ da soru sorabilir ve sorularınızı "yellowbrick" olarak etiketleyebilirsiniz. Ya da Github üzerinde Isssues kısmına ekleme yapabilirsiniz. Veya Twitter hesabımıza `@DistrictDataLab <https://twitter.com/districtdatalab>`_ tweet ya da direk mesaj atabilirsiniz.

Açık Kaynak
-----------

Yellowbrick `license <https://github.com/DistrictDataLabs/yellowbrick/blob/master/LICENSE.txt>`_ açık kaynaklı bir `Apache 2.0 <http://www.apache.org/licenses/LICENSE-2.0>`_ lisansıdır. Yellowbrick çok aktif geliştirici topluluğuna sahip olup; lütfen sizde katılmayı ve `katkıda bulunmayı <https://github.com/DistrictDataLabs/yellowbrick/blob/develop/CONTRIBUTING.md>`_ düşünün!

Yellowbrick `GitHub <https://github.com/DistrictDataLabs/yellowbrick/>`_ üzerinde bulunmaktadır. `issues <https://github.com/DistrictDataLabs/yellowbrick/issues/>`_ ve `pull requests <https://github.com/DistrictDataLabs/yellowbrick/pulls>`_ detaylarını bu linklerden takip edebilirsiniz.


İçindekiler Tablosu
-----------------

Kütüphanenin bu versiyonu için olan Yellowbrick dokümantasyonunun tüm listesini aşağıda bulabilirsiniz:

.. toctree::
   :maxdepth: 2

   quickstart
   tutorial
   api/index
   evaluation
   contributing
   matplotlib
   about
   changelog

Dizinler ve Tablolar
------------------

* :ref:`genindex`
* :ref:`modindex`
