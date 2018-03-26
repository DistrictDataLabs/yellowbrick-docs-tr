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

Yellowbrick, insanların model seçim sürecini yönlendirmeye izin veren "Görselleştirici" adı verilen Scikit-Learn API`sini genişleten görsel tanı araçları paketidir. Kısacası, Yellowbrick, Scikit-Learn`i Matplotlib ile Scikit-Learn dokümantasyonuna gore birleştirirek modelinize göre görselleştirme üretmektedir. Yellowbrick ile ilgili daha fazlası için, lütfen bakınız :doc:`about`.

Eğer Yellowbrick`te yeniyseniz, :doc:`quickstart` ya da bu kısmı geçerek :doc:`tutorial` kısmını ziyaret edebilirsiniz. Yellowbrick, düzenli olarak eklenen birçok görselleştiricisi ile zengin bir kütüphanedir. Spesifik Görselleştiriciler ve genişletilmiş kullanımları ile ilgili detayları  :doc:`api/index` kısmından bulabilirsiniz. Yellowbrick`e katkıda bulunmak ister misiniz? :ref:`contributing guide <contributing>` a göz atin. Şayet kullanıcı testi için başvurduysanız, şu adrese gidiniz :doc:`evaluation` (ve Teşekkür ederiz).

Görselleştiriciler
-----------

Görselleştiriciler, oncelikli amacı model secim islemine icgoru saglamaya izin veren gorsellestirmeleri olusturan tahmin ediciler (veriden ogrenilen nesneler)dir. Scikit-Learn`e gore, Gorsellestiriciler; veri alanini gorsellestirirken, donusturuculere benzeyebilir ya da "ModelCV" (e.g. `RidgeCV <http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RidgeCV.html>`_, `LassoCV <http://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LassoCV.html>`_) methodlarin calismasinda oldugu gibi, bir model tahmin edicisini sarabilmektedir. Yellowbrick`in oncelikli amaci, Scikit Learn benzeri bir mantiksal API olusturmaktir. En popular gorsellestiricilerimizden bazilari sunlardir:

Özellik Görselleştirme
~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/features/rankd`: pairwise ranking of features to detect relationships
- :doc:`api/features/pcoords`: horizontal visualization of instances
- :doc:`Radial Visualization <api/features/radviz>`: separation of instances around a circular plot
- :doc:`api/features/pca`: projection of instances based on principal components
- :doc:`api/features/importances`: rank features by importance or linear coeficients for a specific model
- :doc:`Scatter and Joint Plots<api/features/scatter>`: direct data visualization with feature selection

Klasifikasyon Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/classifier/class_balance`: see how the distribution of classes affects the model
- :doc:`api/classifier/classification_report`: visual representation of precision, recall, and F1
- :doc:`ROC/AUC Curves <api/classifier/rocauc>`: receiver operator characteristics and area under the curve
- :doc:`Confusion Matrices <api/classifier/confusion_matrix>`: visual description of class decision making

Regresyon Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`api/regressor/peplot`: find model breakdowns along the domain of the target
- :doc:`api/regressor/residuals`: show the difference in residuals of training and test data
- :doc:`api/regressor/alphas`: show how the choice of alpha influences regularization

Kümesel Görselleştirme
~~~~~~~~~~~~~~~~~~~~~~~~

- :doc:`K-Elbow Plot <api/cluster/elbow>`: select k using the elbow method and various metrics
- :doc:`Silhouette Plot <api/cluster/silhouette>`: select k by visualizing silhouette coefficient values

Metin Görselleştirmesi
~~~~~~~~~~~~~~~~~~

- :doc:`Term Frequency <api/text/freqdist>`: visualize the frequency distribution of terms in the corpus
- :doc:`api/text/tsne`: use stochastic neighbor embedding to project documents.

... and more! Visualizers are being added all the time; be sure to check the examples (or even the `develop branch <https://github.com/DistrictDataLabs/yellowbrick/tree/develop>`_) and feel free to contribute your ideas for new Visualizers!

Yardım Almak İçin
------------

Yellowbrick is a welcoming, inclusive project in the tradition of Matplotlib and Scikit-Learn. Similar to those projects, we try to follow the `Python Software Foundation Code of Conduct <http://www.python.org/psf/codeofconduct/>`_. Please don't hesitate to reach out to us for help or if you have any contributions or bugs to report!

The primary way to ask for help with Yellowbrick is to post on our `Google Groups Listserv <https://groups.google.com/forum/#!forum/yellowbrick>`_. This is an email list/forum that members of the community can join and respond to each other; you should be able to receive the quickest response here. Please also consider joining the group so you can respond to questions! You can also ask questions on `Stack Overflow <http://stackoverflow.com/questions/tagged/yellowbrick>`_ and tag them with "yellowbrick". Or you can add issues on GitHub. You can also tweet or direct message us on Twitter `@DistrictDataLab <https://twitter.com/districtdatalab>`_.

Açık Kaynak
-----------

The Yellowbrick `license <https://github.com/DistrictDataLabs/yellowbrick/blob/master/LICENSE.txt>`_ is an open source `Apache 2.0 <http://www.apache.org/licenses/LICENSE-2.0>`_ license. Yellowbrick enjoys a very active developer community; please consider joining them and `contributing <https://github.com/DistrictDataLabs/yellowbrick/blob/develop/CONTRIBUTING.md>`_!

Yellowbrick is hosted on `GitHub <https://github.com/DistrictDataLabs/yellowbrick/>`_. The `issues <https://github.com/DistrictDataLabs/yellowbrick/issues/>`_ and `pull requests <https://github.com/DistrictDataLabs/yellowbrick/pulls>`_ are tracked there.


İçindekiler Tablosu
-----------------

The following is a complete listing of the Yellowbrick documentation for this version of the library:

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

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
