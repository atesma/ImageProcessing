# ImageProcessing-
CPE409(1) Image Processing 

1.	Normalizasyon ile standardizasyon arasındaki farklar.
   
Görüntü işleme sürecinde, normalizasyon ve standardizasyon genellikle veri önişleme adımlarında kullanılır. İkisi de veri değerlerini değiştirir, ancak farklı şekillerde yaparlar:

**Normalizasyon:**

Veri değerlerini belirli bir aralığa dönüştürmek için kullanılır. Genellikle [0, 1] veya [-1, 1] aralığında olacak şekilde yapılandırılır.
Görüntü işlemede piksel değerlerini normalize etmek için kullanılabilir. Örneğin, piksel değerlerini 0 ile 1 arasında ölçeklendirerek, aynı ölçekteki değerlere sahip olurlar.
Normalizasyon, veri dağılımını değiştirmez, yalnızca ölçeklendirir.

**Standardizasyon:**

Veri değerlerini ortalaması 0 ve standart sapması 1 olacak şekilde dönüştürür.
Görüntü işlemede, piksel değerlerini standartlaştırmak için kullanılabilir. Bu, her pikselin ortalama değeri çıkarılarak ve standart sapmaya bölünerek yapılabilir.
Standardizasyon, verinin dağılımını değiştirir, ancak genellikle veriyi daha kolay işlemek ve model eğitmek için kullanılır.
Hangi yöntemin kullanılacağı, verinin yapısı, kullanılacak model ve amacınıza bağlı olabilir. Örneğin, derin öğrenme modelleri genellikle normalizasyonu tercih edebilirken, bazı istatistiksel modeller standartizasyonu tercih edebilir.
