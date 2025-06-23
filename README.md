Kiz-Basina-Bootcam-1.-Final-Odevi
Yolcu Memnuniyeti Üzerine Veri Analizi 
Bu proje, Kız Başına Veri Analizi Bootcamp kapsamında yaptığım ilk gerçek veri analizi çalışmasıydı. Amacım, bir havayolu firmasının yolcu memnuniyetini etkileyen faktörleri anlamak ve veriye dayalı bazı içgörüler elde etmekti.

Veri setinde yolcuların yaşı, cinsiyeti, seyahat türü, uçuş sınıfı gibi bilgilerle birlikte, hizmetlerle ilgili puanlamaları (örneğin temizlik, koltuk rahatlığı, check-in deneyimi) ve memnun olup olmadıkları bilgisi yer alıyordu.

Projede Kullanılan Veri Seti
Bu analizde kullanılan veri seti, Kaggle platformunda açık şekilde paylaşılan Airline Passenger Satisfaction Dataset adlı veri setidir.

Veri setinde şunlar yer alıyor:

Yolcuya ait bilgiler: yaş, cinsiyet, müşteri tipi (sadık/sadakatsiz)

Uçuşa ait bilgiler: uçuş mesafesi, uçuş sınıfı, seyahat amacı

Hizmetlere verilen puanlar: koltuk konforu, yiyecek-içecek, temizlik, eğlence, bagaj süreci vb.

Uçuş rötar süreleri: kalkış ve varış gecikmeleri

Hedef değişken: satisfaction → yolcu memnun mu, değil mi?

Toplamda 103.904 yolcuya ait kayıt içermektedir. Hem sayısal hem kategorik veriler bulunmaktadır.

Neler Yaptım?
Veriyle tanıştım. İlk olarak veri setinin boyutunu, sütunlarını ve veri türlerini inceledim. Eksik veriler vardı ama sadece “arrival delay” sütununda ve oranı çok düşüktü. Ortalama ile doldurmak yeterli oldu.

Aykırı değerleri tespit ettim. Özellikle rötar sürelerinde uçuk değerler vardı. Bazı uçuşlar 1500 dakikadan fazla gecikmişti. Bunları silmek istemedim çünkü değerli bilgi olabilir. Bu yüzden IQR yöntemiyle bu değerleri uç sınırlara kırptım.

Görselleştirme yaptım. Sayısal değişkenler için histogram ve boxplot, kategorik değişkenler için bar grafikleri kullandım. Sonuçları satisfaction (memnuniyet) değişkenine göre gruplandırarak daha net görebildim.

Dikkatimi Çekenler
Sadık (loyal) müşteriler, sadık olmayanlara göre çok daha memnun.

İş amaçlı seyahat eden yolcuların memnuniyet oranı, kişisel seyahat edenlerden daha yüksek.

Business class yolcuları genel olarak çok daha olumlu puanlar veriyor.

Rötar süreleri arttıkça memnuniyet azalıyor. En belirgin etki bu kısımdaydı.

Cinsiyetin memnuniyet üzerinde net bir fark yaratmadığını gördüm.

Sayılarla Kısa Bir Özet
Ortalama yaş: 39

Ortalama uçuş mesafesi: 1189 km

Ortalama rötar süresi: 15 dakika

Memnun yolcu oranı: %43
Memnun olmayan veya kararsız: %57

Benim İçin Anlamı
Bu projede sadece teknik bir analiz yapmadım. Aynı zamanda veriye yaklaşımımı, temizleme sürecimi ve görselleştirme ile nasıl hikâye anlatılabileceğini öğrendim. Her grafik bana bir şey öğretti. Her sütun bir yolcunun deneyimi gibiydi. Küçük bir veriyle başlayıp anlamlı sonuçlar çıkarabilmek benim için çok motive ediciydi.

İlk kez bu kadar kapsamlı bir analiz yaptım ve şunu fark ettim:
Sadece veriyi görmek değil, verinin arkasındaki insanı ve durumu anlamak çok önemli.
İleride bu içgörüleri modellerle destekleyerek daha öngörülebilir hale getirmeyi de öğrenmek istiyorum.
