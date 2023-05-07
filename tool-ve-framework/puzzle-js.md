---
description: Ölçeklenebilir ve son derece hızlı web siteleri için mikro frontend framework.
---

# 🧩 Puzzle JS

<figure><img src="../.gitbook/assets/Screenshot 2023-05-07 at 19.07.48.png" alt=""><figcaption><p>Puzzle JS Logo</p></figcaption></figure>

PuzzleJs, micro frontend frameworkü olarak çalışan bir yapıdır. İşleyiş süreci şu şekildedir:

<mark style="background-color:orange;">**Derleme Zamanı(Compile Time)**</mark>:

1. Ağ geçitleri, kendi parçalarını, API'lerini ve ağ geçidi bilgilerini sunmaya başlar.
2. Storefront, kayıtlı ağ geçitlerinin bilgilerini alır.
3. Storefront, gerekli parçaları, bağımlılıkları ve varlıkları indirir ve önbelleğe alır.
4. Storefront, HTML'i en hızlı şablon oluşturma için bellekteki JavaScript işlevine derler.

<mark style="background-color:orange;">**On Request:**</mark>

1. Storefront, derlenmiş işlemin parçalı bir yanıtını gönderir, ancak bağlantıyı kapatmaz. Kullanıcılar şimdi statik içerikler ve yer tutucular ile sitenizi görebilir. Aynı zamanda, ağ geçitlerinden alınan parçaları almak için arka uç istekleri gönderir.
2. Herhangi bir parça ağ geçidinden alındığında, bunu tarayıcıya bir parça olarak gönderir ve daha önce gönderilen yer tutucuyu içerikle değiştirir.
3. Tüm parçalar gönderildiğinde, PuzzleJs bağlantıyı kapatır.

Bu süreç, PuzzleJs'in mikro ön uç çerçevesi olarak nasıl çalıştığını açıklamaktadır.

<mark style="background-color:orange;">**Dökümantasyonundaki Önemli Noktalar**</mark>

Neden? Geleneksel model, modern web siteleri için oldukça verimsizdir.

* Aynı kod üzerinde çalışan birden fazla ekip, her şeyi yönetmeyi zorlaştırır.
* İlk baytın süresi, en yavaş API kadar hızlıdır.
* Arka uç veri toplarken, kullanıcı tarayıcısı ilk baytı beklerken zaman kaybeder.
* Diğer ekiplerin özellikleri henüz hazır olmadığı için, özellikler tamamen geliştirildiğinde ve test edildiğinde çevrimiçi olamaz.
* Mevcut olanın dışında farklı teknolojiler kullanamazsınız.
* Belirli bir süreci ölçeklendiremezsiniz, çünkü tüm sisteme bağımlısınız.

Özellikler:

* İlk Bayta Kadar Süre: PuzzleJs, derleme sürecinde HTML şablonunu javascript işlevine derler. Bu işlem, istekten tamamen bağımsız olduğu için PuzzleJs, bu işlevi kullanarak ilk parçayı gönderebilir.
* SEO Dostu: PuzzleJs, her şeyin sunucu tarafında hazırlandığı ve işlendiği için tamamen SEO dostudur.
* Genişletilebilirlik: PuzzleJs'i özel işlevlerinizle kolayca genişletebilirsiniz.
* Kolay: Bir ağ geçidi veya mağaza önü oluşturabilir ve bunları bir yapılandırma dosyası sağlayarak bağlayabilirsiniz.
* Bağımsız: Ağ geçitlerinizde herhangi bir teknoloji kullanabilirsiniz, PuzzleJs teknolojilerinizden tamamen bağımsızdır. ReactJs, Vue veya başka herhangi bir JavaScript Framework.
* Ölçeklenebilir: PuzzleJs, mağaza önlerini ve ağ geçitlerini birbirinden bağımsız olarak oluşturabilir. Böylece Dockerize ortamlarda tek bir projeyi kolayca ölçeklendirebilirsiniz.
* Korumalı: Bir parçanın gerektirdiği API'niz devre dışı olduğunda, PuzzleJs diğer sayfa parçalarının çalışmaya devam edeceğini garanti eder.

Dökümantasyon: [https://puzzle-js.github.io/puzzle-js/](https://puzzle-js.github.io/puzzle-js/)

GitHub: [https://github.com/puzzle-js/puzzle-js](https://github.com/puzzle-js/puzzle-js)
