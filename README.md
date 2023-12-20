# ImageProcessing-
CPE409(1) Image Processing 

**1.	Normalizasyon ile standardizasyon arasındaki farklar.** 
   
Görüntü işleme sürecinde, normalizasyon ve standardizasyon genellikle veri önişleme adımlarında kullanılır. İkisi de veri değerlerini değiştirir, ancak farklı şekillerde yaparlar:

*Normalizasyon:*

Veri değerlerini belirli bir aralığa dönüştürmek için kullanılır. Genellikle [0, 1] veya [-1, 1] aralığında olacak şekilde yapılandırılır.
Görüntü işlemede piksel değerlerini normalize etmek için kullanılabilir. Örneğin, piksel değerlerini 0 ile 1 arasında ölçeklendirerek, aynı ölçekteki değerlere sahip olurlar.
Normalizasyon, veri dağılımını değiştirmez, yalnızca ölçeklendirir.

*Standardizasyon:*

Veri değerlerini ortalaması 0 ve standart sapması 1 olacak şekilde dönüştürür.
Görüntü işlemede, piksel değerlerini standartlaştırmak için kullanılabilir. Bu, her pikselin ortalama değeri çıkarılarak ve standart sapmaya bölünerek yapılabilir.
Standardizasyon, verinin dağılımını değiştirir, ancak genellikle veriyi daha kolay işlemek ve model eğitmek için kullanılır.
Hangi yöntemin kullanılacağı, verinin yapısı, kullanılacak model ve amacınıza bağlı olabilir. Örneğin, derin öğrenme modelleri genellikle normalizasyonu tercih edebilirken, bazı istatistiksel modeller standartizasyonu tercih edebilir.

**2.	Bit plane slicing**
   Bit plane slicing işlemleri, görüntü üzerinde her bir pikselin belli bir bit düzeyini elde etmeyi içerir. Python kullanarak bir görüntüdeki belirli bir bit düzeyini almak için OpenCV kütüphanesini kullanabilirsiniz.
Örnek kod da, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler ve belirtilen bit düzeyini alır. bit_plane_slice fonksiyonu, görüntü üzerinde belirli bir bit düzeyini elde etmek için bitwise and işlemini kullanır. Bu kod, OpenCV ve NumPy kütüphanelerini kullanarak belirli bir bit düzeyinin görüntü üzerinde nasıl alınabileceğini göstermektedir. Çalıştırılacak görüntünün uygun bir şekilde tanımlanması ve yolunun belirtilmesi gerekecektir.

**3.	Histogram eşitleme**

   Histogram eşitleme, bir görüntünün kontrastını artırmak veya görüntüdeki ayırt edilebilir özellikleri vurgulamak için kullanılan bir tekniktir. Bu işlem, bir görüntünün piksel yoğunluk dağılımını değiştirir ve daha geniş bir ton aralığına sahip olmasını sağlar.
   Örnek kod da, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.equalizeHist() fonksiyonu, histogram eşitleme işlemini gerçekleştirir. Sonrasında, orijinal görüntü ile eşitlenmiş görüntüyü bir arada görselleştirir.
   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntünün histogramını eşitleyip sonucu görselleştirmek için kullanılabilir.
   Python'da OpenCV kütüphanesi ile histogram eşitleme işlemi oldukça kolaydır.

**4.	Contrast stretching**
   Contrast stretching (kontrast genişletme), bir görüntünün kontrastını artırmak için kullanılan bir işlemdir. Bu işlem, görüntüdeki piksel değerlerini genişletir ve daha geniş bir ton aralığına yayarak görüntünün daha net veya daha belirgin olmasını sağlar. Python'da bu işlemi OpenCV veya NumPy gibi kütüphanelerle gerçekleştirebiliriz.
   Örnek kod da, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. Contrast stretching için basit bir yöntem kullanır ve piksel değerlerini 0-255 arasına ölçeklendirir. Daha sonra, orijinal görüntü ile kontrastı genişletilmiş görüntüyü bir arada görselleştirir.

   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntünün kontrastını genişletmek için kullanılabilir. Özellikle daha iyi görselleştirme veya daha net bir analiz için kontrastı artırmak istediğinizde bu tür bir işlem kullanılabilir.
   
**5.	Gamma**
   Gamma düzeltme, görüntü parlaklığını veya kontrastını değiştirmek için kullanılan bir tekniktir. Bu teknik, piksel değerlerini bir gamma değeriyle dönüştürerek görüntünün aydınlık veya karanlık bölümlerini vurgulamanıza olanak tanır. Kod örneğinde, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. gamma_correction adlı bir fonksiyon, giriş görüntüsünü belirtilen gamma değeriyle düzelten bir işlem uygular. Daha sonra, orijinal görüntü ile gamma düzeltilmiş görüntüyü bir arada görselleştirir.

   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntü üzerinde gamma düzeltme işlemi yaparak görüntüyü aydınlatma veya karartma için kullanılabilir. Gamma değeri artırıldığında görüntü daha parlak hale gelirken, azaltıldığında daha koyu hale gelir.

**6.	Ortalama filtresi**
   Ortalama filtresi, bir görüntü üzerindeki gürültüyü azaltmak veya pürüzlü bölgeleri yumuşatmak için kullanılan bir düzenleme (smoothing) tekniğidir. Bu filtre, bir pikselin değerini ve çevresindeki piksellerin değerlerini ortalamak suretiyle çalışır.
   Python'da, OpenCV kütüphanesi kullanılarak bir görüntüye ortalama filtre uygulayabiliriz. 
od örneğinde, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.blur() fonksiyonu, görüntü üzerinde ortalama filtre uygular. kernel_size değişkeni, filtre boyutunu belirtir.
   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntü üzerindeki gürültüyü azaltmak veya pürüzlü bölgeleri yumuşatmak için ortalama filtre uygulamak için kullanılabilir. Filtre boyutu arttıkça, daha fazla yumuşatma etkisi elde edilir ancak aynı zamanda görüntü detayları da kaybolabilir.

**7.	Gaussian filtresi**
   Gaussian filtresi, bir görüntüdeki gürültüyü azaltmak veya pürüzlü bölgeleri yumuşatmak için kullanılan bir düzenleme (smoothing) tekniğidir. Bu filtre, görüntü üzerindeki piksel değerlerini, merkezdeki pikselin değerini en çok etkileyerek ağırlıklı bir şekilde yumuşatır.
  Örnek kod, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.GaussianBlur() fonksiyonu, görüntü üzerinde Gaussian filtresi uygular. kernel_size değişkeni, filtre boyutunu ve sigma değişkeni standart sapmayı belirtir.

   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntü üzerindeki gürültüyü azaltmak veya pürüzlü bölgeleri yumuşatmak için Gaussian filtresi uygulamak için kullanılabilir. Filtre boyutunu ve standart sapmayı değiştirerek farklı filtreleme sonuçlarını gözlemleyebilirsiniz

Python'da, OpenCV kütüphanesi ile bir görüntüye Gaussian filtresi uygulamak oldukça kolaydır

**8.	Sobel filtresi**
   Sobel filtresi, kenar tespiti ve görüntü gradyanlarının hesaplanması için kullanılan bir konvolüsyon filtredir. X ve Y yönlerindeki kenarları tespit etmek için ayrı ayrı kullanılabilir. Python'da, OpenCV kütüphanesiyle Sobel filtresini kullanarak kenar tespiti yapabiliriz.
  	Kod örneği, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.Sobel() fonksiyonu, görüntü üzerine Sobel filtresini uygular. ksize parametresi, kullanılan Sobel çekirdeğinin boyutunu belirtir.
   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntü üzerinde Sobel filtresi kullanarak X ve Y yönlerindeki kenarları tespit etmek için kullanılabilir. Sonuçta, X yönünde kenarları temsil eden bir görüntü ve Y yönünde kenarları temsil eden bir görüntü elde edersiniz.

**9.	Blurring operation with Laplace**
   Laplace filtresi, görüntü üzerindeki kenarları tespit etmek için kullanılan bir filtreleme operasyonudur. Bu filtre, kenarları vurgulayarak ve görüntüdeki yoğunluk değişikliklerini belirleyerek çalışır. Python'da, OpenCV kütüphanesi kullanılarak Laplace filtresi uygulanabilir.
   Örnek kod, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.Laplacian() fonksiyonu, görüntü üzerine Laplace filtresini uygular. Elde edilen görüntü, kenarları vurgulayan bir görüntüdür.
   Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, görüntüdeki kenarları tespit etmek ve vurgulamak için Laplace filtresi uygulamak için kullanılabilir.

**10.	Smoothing, sharpening**
 Bir görüntü üzerinde smoothing (yumuşatma) ve sharpening (keskinleştirme) işlemleri için farklı teknikler ve filtreler mevcuttur. Örneğin, bir görüntü üzerinde smoothing işlemi yapmak için genellikle Gaussian veya median filtreleri kullanılırken, keskinleştirme işlemi için Laplace veya farklı kenar vurgulama filtreleri tercih edilir.
Kod örnekleri, 'ornek_goruntu.png' adlı bir görüntüyü yükler. İlk örnek, Gaussian Blur ile bir smoothing işlemi uygularken, ikinci örnek Laplace filtresiyle bir sharpening işlemi uygular. Lütfen görüntü dosyasının yolunu doğru şekilde belirttiğinizden emin olun. Bu kodlar, farklı görüntü işleme tekniklerini kullanarak smoothing ve sharpening işlemlerini gerçekleştirir.

**11.	Gaussian**
   Görüntüdeki gürültüyü azaltmak veya pürüzlü bölgeleri yumuşatmak için kullanılır. Python'da, OpenCV kütüphanesi ile Gaussian filtresini kullanarak bir görüntüyü yumuşatabiliriz.
   Kod örneği, 'ornek_goruntu.png' adlı bir görüntüyü yükler. cv2.GaussianBlur() fonksiyonu, görüntü üzerine Gaussian filtresini uygular. Filtre boyutu (5x5) ve standart sapma (0) parametrelerle belirtilmiştir. Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, bir görüntü üzerinde Gaussian filtresi kullanarak smoothing (yumuşatma) işlemi gerçekleştirir. Filtre boyutunu ve standart sapmayı değiştirerek farklı yumuşatma düzeyleri elde edebilirsiniz.

**12.	Salt and pepper**
   "Salt and pepper" gürültüsü, bir görüntüde rastgele piksellerin beyaz veya siyah renge sahip olmasıyla oluşan bir tür gürültüdür. Bu, görüntünün bazı bölgelerinde belirgin siyah veya beyaz noktaların veya piksellerin oluşmasına neden olur. Bu tür gürültüyü azaltmak için genellikle median filtresi gibi filtreleme teknikleri kullanılır.
   Python'da, OpenCV kullanarak bir görüntüdeki "salt and pepper" gürültüsünü azaltmak için median filtresini kullanabiliriz. 
    Kod örneği, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler ve üzerine "salt and pepper" gürültüsü ekler. Daha sonra cv2.medianBlur() fonksiyonu kullanılarak median filtresi uygulanır. Median filtresi, bu tür rastgele piksel değerlerinin etkisini azaltarak gürültüyü azaltmaya yardımcı olur. Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, bir görüntüdeki "salt and pepper" gürültüsünü azaltmak için median filtresini kullanır.

**13.	Contraharmonic mean**
   Contraharmonic mean filtresi, bir görüntü üzerinde gürültüyü azaltmak için kullanılan bir filtreleme tekniğidir. Bu filtre, bir bölge veya piksel grubu içindeki piksel değerlerinin belirli bir kuvvet ile alınan ortalama değerini hesaplar. Genellikle bir Q parametresi kullanılır; Q pozitif olduğunda filtre, piksel değerlerini daha çok gürültülü piksellere çekerken, Q negatif olduğunda daha çok kenarların korunmasına odaklanır. Python'da, OpenCV kullanarak bir görüntüde Contraharmonic Mean filtresini uygulamak mümkündür.
   Kod örneği, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. Ardından cv2.filter2D() fonksiyonunu kullanarak Contraharmonic Mean filtresini uygular. Q parametresi, filtredeki ortalama hesaplama formülünde kullanılır. Negatif Q değerleri genellikle kenarları korurken, pozitif Q değerleri daha fazla gürültü azaltma eğilimindedir.Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, Contraharmonic Mean filtresi kullanarak bir görüntüde gürültüyü azaltmak için kullanılabilir.

**14.	RGB kullanarak bölütlenme**
   RGB renk uzayı, bir görüntüdeki renkleri temsil etmek için kullanılan bir modeldir. Bir görüntüyü kırmızı (R), yeşil (G) ve mavi (B) bileşenlere ayıran RGB uzayında bölütlenme işlemi, her bir bileşenin değerini kullanarak farklı renk bölümlerini elde etmeyi sağlar. Python'da, bir görüntüyü RGB bileşenlerine ayırmak için genellikle NumPy dizileri kullanılır. Örneğin, bir görüntünün kırmızı, yeşil ve mavi bileşenlerine ayrılabilir ve istenilen bölüm elde edilebilir.
Örnek kod, 'ornek_goruntu.png' adlı bir görüntüyü yükler ve bu görüntüyü kırmızı, yeşil ve mavi bileşenlere ayırır. Sonrasında, her bir bileşenin oluşturduğu bölütleri ayrı ayrı görselleştirir. Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, bir görüntüyü RGB bileşenlerine ayırarak her bir bileşenin oluşturduğu bölütleri gösterir.

**15.	Açma - kapama işlemleri**
    
   Açma ve kapama, morfolojik işlemler olarak bilinir. Bu işlemler, bir görüntü üzerindeki şekil veya yapıları düzenlemek, gürültüyü azaltmak veya nesneleri vurgulamak için kullanılır. Genellikle erozyon (aşındırma) ve genişletme (büyütme) operasyonlarının kombinasyonu olarak gerçekleştirilirler. Python'da, OpenCV kütüphanesi bu tür morfolojik işlemleri gerçekleştirmek için kullanılabilir.
   Kod örneği, 'ornek_goruntu.png' adlı bir gri tonlamalı görüntüyü yükler. cv2.morphologyEx() fonksiyonu kullanılarak açma ve kapama işlemleri uygulanır. kernel değişkeni, bu işlemlerin uygulanacağı kernel boyutunu belirtir. Lütfen 'ornek_goruntu.png' dosya yolunu, kendi görüntünüzün yoluna uygun şekilde değiştirin. Bu kod, bir görüntü üzerinde açma ve kapama işlemlerini gerçekleştirerek şekil veya yapıları düzenlemek veya gürültüyü azaltmak için kullanılabilir.


