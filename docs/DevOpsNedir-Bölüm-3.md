# DevOps Nedir? | Bölüm 3: İnsanlar, Süreç ve Teknoloji

DevOps kültürünüzün nasıl görüneceğine dair net bir fikre sahip olduğunuzda, mevcut süreçlerinizi gözden geçirmenin ve geleceğe yönelik iyileştirmeleri değerlendirmenin zamanı gelmiştir. DevOps üç ana odak noktasına sahiptir: insanlar, süreç ve teknoloji. Süreç, DevOps dönüşümünde kültürden sonra ikinci en önemli unsurdur.

![image](https://github.com/user-attachments/assets/2daafb15-6ddb-4526-830a-02f9ca1ebed1)

Süreç, yazılım teslim hızınızı artırmada en fazla nicel iyileşmeyi göreceğiniz alandır. Ancak bu bölüm, süreçlerinizi nasıl iyileştireceğinize odaklanmamaktadır. Şimdilik, ekibinizin yazılım geliştirme süreçlerine bütünsel bir bakış açısıyla yaklaşın. Bunu, teknolojiyi uygulayan bir insan ekosistemi olarak görün.

Gereksiz süreçler, müşterinin deneyimini doğrudan etkilemeyen herhangi bir faaliyet anlamına gelir. Eğer bir eylem, etkinlik veya süreç müşterilerinize doğrudan değer katmıyorsa, bu bir israftır. DevOps ile ekibinizin hızını artırmak, gereksiz eylem ve süreçleri belirleyip ortadan kaldırmanızı gerektirir.

Geliştirme sürecinizde ne kadar fazla gereksiz eylem bulunduğunu öğrendiğinizde şaşırabilirsiniz. İngiltere'deki Cardiff Üniversitesi Lean Enterprise Research Centre (LERC), geliştiriclerin rutin olarak gerçekleştirdiği faaliyetlerin %60'ının israf olduğunu ve son kullanıcıya hiçbir etkisinin olmadığını ortaya koymuştur. Bu rahatsız edici bir durum değil mi ? Belki katılmıyor olabilirsiniz sizde süreçleriniz gözden geçirin can sıkıcı tekrarlayan işler yada gereksiz süreç uzatan prosedürler verimliliği düşürmüyor mu ? Buraya bir not düşmek istiyorum iş kaltesini artıracak, güvenliğini sağlayacak hatayı öneleyecek süreçlerden bahsetmiyorum!!!

Farklı eylem ve süreç türlerini anlamak, sisteminizin kolayca iyileştirilebilecek stratejinizi belirlemenize yardımcı olur. Bu bir başlangıç listesidir. DevOps dönüşümünüzde hızlı kazanımlar elde etmenizi sağlayan "kolay adımları" temsil eder. DevOps'un avantajlarını ne kadar hızlı uygularsanız, dönüşümünüz o kadar sorunsuz ilerler.

Bu makalemde, karmaşık sistemlerdeki yedi gereksiz süreçi keşfedeceğiz, veri toplayarak darboğazları tespit etmeyi öğrenecek ve müşteri odaklı bir şekilde süreçlerinizi önceliklendireceksiniz.

Birçok DevOps prensibi, yalın üretime dayanır. Yalın üretim, gereksiz süreçlerin belirlenmesi ve ortadan kaldırılması yoluyla üretim hızının artırılmasını amaçlayan bir ilkedir. Yalın üretim, yedi tür süreci tanımlar. Bu bölümdeki süreçler, en fazla etkileyenden en az etkileyene doğru sıraladım. Başka bir deyişle, listelenen ilk süreç türü, en kolay giderilebilecek olan ve öncelikli olarak ele almanız gereken olabilir.

## Gereksiz Süreçler

Süreçler, DevOps'un büyük bir parçasıdır çünkü iş akışını, davranışları ve beklentileri her iş alanında düzenler. Ancak süreçler hızla bir düşmana dönüşebilir. Mühendisleriniz her hafta kaç toplantıya katılmak zorunda? Günlük toplantılarınız on dakikadan az mı sürüyor, yoksa harcanan zaman gerçekten gerekli mi? Gereksiz süreçlerin bir diğer tehlikeli yönü de, ürün gereksinimlerinin baştan netleştirilmemesi sonucu işin tekrar tekrar revize edilmesi ihtiyacıdır.

## Bekleme

Geliştirme yaşam döngüsünün herhangi bir aşamasındaki hareketsizlik bir yazılım parçasını geliştirme planından canlıya alma aşamasına kadar geçen süre bir israf türüdür. Ancak, organizasyonunuz muhtemelen bekleme süreleriyle doludur. Mühendisler, kalite ekibinin kodu test etmesini bekler. Altyapı ekipleri, geliştiricilerin ürünlerini dağıtabilmesi için sistemlerin kurulmasını bekler. Birde bilgi güvenliği ekipleri de işin içine girdimi vay halimize… tekrar etmek istiyorum bunların hepsi zorunlu süreçler ama nerede hata yapıyoruz neden bekliyoruz? Kahvem bitsin geliyorum :)  Herkes, birbirinden izole çalışan ekiplerin işlerini tamamlamasını bekler. Bekleme süreleri yaygındır ve mücadele edilmesi zor bir sorundur.

## Hareket

Hareket, iş yapıyor gibi görünmekle ilgili bir kavramdır. Siz ve ekibiniz tarafından yapılan ancak gerçek bir değer yaratmayan tüm çabalardır. SRE ekiplerinde, bu tür çalışmalar "toil" olarak adlandırılır. Eğer bir faaliyet müşterileriniz üzerinde doğrudan bir etkiye sahip değilse, amacı "görünmek" olabilir. Bu tür işler genellikle verimsiz süreçlerden kaynaklanır. Örneğin, süreçlerinizi gözden geçirme yöntemleriniz ve teşvik sistemleriniz bu tür gereksiz işlere yol açabilir. Öte yandan, bazı hareketler otomasyon kullanılarak ekip verimliliğini artıracak şekilde iyileştirilebilir. Otomasyon, otomasyon ve otomasyon… PowerShell öğrenmeye beni iten ana sebep sürekli hareket halinde çalışmama rağmen aynı işleri sürekli tekrar etmesi bir süre sonra can sıkıcı ve verimsiz hale geliyordu. Bir süre sonra hata ihtimalinide artrımaya başladığını gördüm. Otomatize edilmiş tekrarlayan işler hata payını ciddi seviyede ortanda kaldırdığı gibi kaybedilen zamanıda telafi edecektir.

## Hata Maliyetleri

Hatalar, en kolay fark edilen süreç türlerinden biridir. Otomotiv üretiminde, hatalı ürünler hurda metal olarak kabul edilir. Yazılımda ise hata israfı; hata düzeltmelerini, teknik borçları ve hizmet kesintilerini içerir. Tamamlanmış bir işin düzeltilmesi gerektiğinde, teknik miras kapımızı çalımış olabilir. “Geliştiricileri daha iyi hale getirmek” yaklaşımını tek başına yeterli görmüyorum çünkü her zaman bilinmeyenler ve uç senaryolar olacaktır. Ekibinizin yazılım mimarisinde esnekliği ve hızlı iterasyonları destekleyecek davranışlar sergilemesini sağlamalısınız. Müşterileri etkileyen "patlama alanını" olabildiğince küçük tutmalı ve her geliştiricinin hatalara hızlıca yanıt verebilmesini sağlamalısınız.

## Aşırı Üretim

Üretimde aşırı üretim, müşterinin kullanamayacağı veya satın almak istemediği fazla parçalar veya ürünler anlamına gelir. Yazılımda ise bu, pazarda karşılığı olmayan veya müşteri ihtiyaçlarını karşılamayan kod ve ürünlerle ortaya çıkar. Yazılım geliştiricilerin, var olmayan sorunları çözmek için aşırı mühendislik yapmasını önlemek istiyor olabilirsiniz. Aynı zamanda, ürettiğiniz ürünlerin/yazılımın/uygulamanın gerçekten hedeflediğiniz müşteriler tarafından istenmesini sağlamalısınız.

## Taşıma

Taşıma israfı, bir ürünün, kişinin veya aracın bir yerden başka bir yere taşınmasıyla ortaya çıkar. Otomotiv sektörü için bu süreç, montaj tesislerinden bayilere araba taşımak anlamına gelmektedir. Yazılımda ise kodun sunucular ve repolar arasında taşınması şeklinde gerçekleşir. Ayrıca ekipler arasında insan kaydırma işlemleri yapılır ki bu da insanların işe alışmasını ve hız kazanmasını gerektiren bir süreçtir.

## Envanter

Muhtemelen envanter, sizin ve şirketiniz için bir otomobil üreticisine kıyasla çok daha az sorun teşkil ediyordur. Günümüzde çok az şirket fiziksel yazılım envanteri tutuyor ve bu nedenle envanter yönetimi daha az problem haline geliyor. Ancak yine de envanteriniz olabilir ve satılmayı veya kullanılmayı bekleyen her değerli ürün israf anlamına gelir. Örneğin, yeni çalışanları işe almayı beklediğiniz için ofisinizde boşta duran beş dizüstü bilgisayarı düşünün. Ayrıca, fiziksel envanter kavramını genişleterek organizasyonunuzdaki tescilli bilgileri ve kodları da envanter olarak değerlendirebilirsiniz. Ne, nerede, ne zaman, nasıl ve kim sorularının cevabı dokumanlarınızda olmalı.

Süreçler ile mücadele ederken göz önünde bulundurmanız gereken en önemli noktalardan biri, verimliliği artırmak için optimizasyon ve basitleştirme yapmaktır. Ancak unutmayın ki atıklar genellikle kötü niyetle ortaya çıkmaz, aksine çoğu zaman alışkanlıktan kaynaklanır. Mühendislik organizasyonlarında en büyük düşman alışkanlıklardır. “Biz bunu hep böyle yaptık” ifadesi, yenilikçiliği kökünden çürüten bir zehirdir. Ekibinizin zihniyetinden bu tür cümleleri çıkarmaya çalışın. Yavaşlatan süreçleri ortadan kaldırdığınızda, kaliteyi artırır, geliştirme süresini kısaltır ve maliyetleri düşürürsünüz.

Başarılı teknoloji şirketleri, müşteri sorunlarını anlar ve iyi tasarlanmış ürünlerle bu ihtiyaçlara yanıt verir. Sürekli kaliteyi artırmak, kendini geliştiren şirketleri, başarısız olanlardan ayıran en önemli unsurdur. Yazılım teslim süreçleri zaman alır, ancak pazara çıkış sürenizi kısaltabilirseniz, mühendislik maliyetlerini azaltabilir ve pazar payınızı artırma olasılığınızı yükseltebilirsiniz. Müşterilere mümkün olan en kısa sürede ulaşmak, geri bildirim ve iterasyon fırsatları sunar.

Yalın üretimde tanımlanan her süreç türünün bir maliyeti vardır. Bu süreçlerin her birini ele almak, organizasyonunuzun finansal sonuçlarını önemli ölçüde iyileştirebilir ve toplam maliyetlerinizi azaltmanıza yardımcı olabilir.

En sinsi süreç türlerinden biri darboğazlardır. Darboğaz, bir süreçte tıkanıklık veya yavaşlama anlamına gelir. Bir şişenin boynunun daralması gibi, süreçler de daralabilir ve akışı kısıtlayabilir.

Bunu bir örnekle düşünelim: 5 şeritli bir yol düşünün aynı anda 5 şeritten arka arkaay arabalar  yan yana ilerleyebiliyorsa, bu akıcı bir süreçtir. Ancak yol bir noktada 1 şerite daralırsa arabalar artık yalnızca tek sıra halinde ilerlemek zorunda kalır. Bu durum sıkışıklık yaratır ve akışı yavaşlatır ya da tamamen durdurur. Bugün belkide işten eve dönerken yada evden işe giderken yaşadınız değil mi ?

İdeal olarak, kendi süreçlerinizde darboğazları belirlemeli ve mühendislerin DevOps'u kullanarak "yolu genişletmelerine" ve aynı anda daha fazla işin akmasına olanak tanımalısınız.

Darboğazlar her noktada ortaya çıkabilir. En yaygın darboğaz türlerinden ikisi:

Onay süreçleri: Tek bir yöneticinin sürüm onayı vermesi gerektiğinde süreç tıkanabilir.

Manuel görevler: Dağıtım sürecinin yalnızca belirli bir kişiye bağlı olması (o kişi meşgul olduğunda veya tatile çıktığında süreç durur. Bu arkadaşı hatırladınız mı ? :) ).

Sıkışıklık, yazılım teslim yaşam döngüsünün erken aşamalarında sorunları ele almamak nedeniyle de ortaya çıkabilir. Eğer güvenlik doğrulaması için kodu son aşamada (staging ortamında) test etmeyi bekliyorsanız, hatalar nedeniyle kodu en baştan geliştirme aşamasına geri göndermek zorunda kalabilirsiniz.

## Güvenlik Konularını Planlama Sürecinde Ele Almak

Güvenlikle ilgili sorunları planlama aşamasında ele almak, geliştirici kaynaklarını boşa harcamaktan ve gereksiz zaman kaybından kaçınmanıza yardımcı olabilir.

Darboğazları aramaya başladığınızda, mevcut sisteminizde ne kadar çok olduğunu fark etmek sizi bunalmış hissettirebilir.

## Teknoloji Şirketlerinde Darboğaz Türleri

Teknoloji şirketlerinde iki tür darboğaz yaşanır:

Kısa vadeli darboğaz: Geçici bir aksaklık nedeniyle oluşur. Örneğin, en güvenilir geliştiricinizin tatile çıkması.

Uzun vadeli darboğaz: Üretim sürecinde sürekli ve birikerek artan sürtünme nedeniyle oluşur. Örneğin, yavaş çalışan bir makinenin uzun üretim kuyruklarına yol açması. Bunu daha açık anlatmazdım sanırım. Benzetmem için üzgünüm 

Bir darboğazın nedeni genellikle şu üç faktörden birine dayanır:

Bir makine veya araç maksimum kapasitesine ulaşmıştır. Bu durumda makinenin yenilenmesi, değiştirilmesi veya ek kaynakların sisteme dahil edilmesi gerekir. Bazen darboğaz, mühendis eksikliğinden de kaynaklanabilir. Özellikle bir veya iki operasyon mühendisi onlarca geliştiriciyi desteklemek zorunda kaldığında, ekipte beceri dağılımı dengesiz hale gelir ve darboğaz oluşur.

Kaynak tam olarak kullanılmaz. Eğer darboğaz bir makineden kaynaklanıyorsa, yanlış teknoloji kullanılıyor olabilir veya sistemde bir ayar sorunu olabilir. İnsan faktörüne bağlı darboğazlarda ise, bir çalışanın yanlış bir göreve atanması, onun yeteneklerini tam anlamıyla kullanamamasına verimsizliğe neden olabilir.

Yazılım mühendisleri sürekli olarak en yeni teknolojileri öğrenme baskısı altındadır. Bazen bir darboğazı çözmenin en basit yolu, çalışanlara gerekli eğitimleri ve sürekli öğrenme fırsatlarını sunmaktır.

Herhangi bir darboğaz meydana geldiğinde bu ister uzun bekleme süreleri, ister aşırı yüklenmiş makineler veya tükenmiş insanlar nedeniyle olsun üretim yavaşlar. Başka bir deyişle, tek bir darboğaz tüm üretim zincirini tıkar ve işlenmesi gereken iş miktarını artırır. Özellikle yöneticiler baskı altındayken bu durum oldukça stresli olabilir.

Darboğazları belirlediğinizde, bunların etkisini değerlendirin. Önemli darboğazlar mümkün olan en kısa sürede ele alınmalıdır, ancak küçük darboğazlar o kadar da büyük bir endişe kaynağı değildir.

Geliştirme sürecinde mükemmellik imkansızdır. Eğer mükemmeliyeti hedeflerseniz, her küçük darboğazı çözmeye çalışarak asıl büyük sorunları göz ardı edebilirsiniz. Küçük detaylar için endişelenmeyin. Bunun yerine, geliştirme sürecinizi en çok etkileyen bir veya iki büyük soruna odaklanın.

Geliştirme sürecinizde süreçleri azaltmanın ve darboğazları ortadan kaldırmanın en iyi yollarından biri, etkinin en yüksek olduğu alanlara odaklanmaktır. Bunu, müşterileriniz üzerinde doğrudan etkisi olan işleri önceliklendirerek yapabilirsiniz. Eğer bir şey kullanıcılarınız için önemli değilse, sizin için de önemli olmamalıdır. Siz nediyorsunuz ? 

Darboğazları çözmek için birkaç seçeneğiniz vardır:

## Çalışan Sayısını Artırma

Bir darboğazı çözmek için ekibe yeni çalışanlar eklemek kolay bir çıkış yolu gibi görünebilir. Ancak, bazen gerçekten ihtiyaç duyduğunuz şey budur. İnsan odaklı darboğazların ele alınmaması, ekipler için büyük bir zehir gibidir. Geliştiriciler tükenir, moralleri düşer ve tüm ekip bundan etkilenir. Ekibe yeni katkı sağlayan kişiler eklemek (ve yeni fikirler getirmek), iş süreçlerinize yeni bir soluk kazandırabilir.

İnsan kaynağındaki fazlalık, artan talebe yanıt vermede, çalışanların izinlerini yönetmede ve beklenmedik hastalıklar veya planlı aile izinleriyle başa çıkmada yardımcı olur. Ancak Daha fazla çalışan eklemek, iletişim karmaşıklığını artırabilir ve yeni çalışanları hızlandırmak zaman alır. İşe alım ve eğitim hem zaman hem de para gerektirir. Artısı ve eksisi ile değerlendirmek gerekir.

## Bekleme Süresinde Tampon Oluşturun

Ekibinizi asenkron hale getirin. Yani, geliştirme döngünüzde herhangi bir noktada bekleme süresi varsa, mühendislerinizin veya ekibinizin boş durmak yerine yapabileceği işler olduğundan emin olun.

Örneğin, tamamlanması gereken ancak aciliyeti olmayan işler için bir iş listesi (backlog) oluşturmalısınız. Genellikle bu işler teknik borçlarla ilgilidir önceliği düşürülen veya son teslim tarihine yetişmek için ertelenen işler.

Teknik borçlara şu tür çalışmalar dahildir:

  Eksik veya hatalı işlevlerin düzeltilmesi,
  Fonksiyonelliği ve performansı artırmak için testler eklenmesi,
  Yinelenen işlevleri ortadan kaldırmak için paylaşılan kütüphanelerin oluşturulması.

Bir başka seçenek de mühendisleri, bekleme süresi boyunca yeni beceriler öğrenmeye veya yeni teknolojilerle denemeler yapmaya teşvik etmektir. İşte bekleme süresinde ekibe yeni işler sağlarken göz önünde bulundurmanız gerekenler:

Darboğazı hemen kaldıramıyorsanız, bir tampon oluşturmak, tüm üretim sisteminin uyum içinde çalışmasını sağlamak için iyi bir çözümdür. Uzun vadede darboğazı ortadan kaldırmanız gerekecektir, ancak tampon size ek zaman kazandırır. Tabi yine ancak Bağlam değiştirme (context switching) kesinlikle üretkenliği düşürebilir. Bekleme süresi içinde hızlıca çözülebilecek küçük görevler atanabilir, ancak bu aşamada geliştiricilerinize aşırı karmaşık sorunlar yüklemek uygun değildir. Büyük işleri küçük ve yönetilebilir parçalara bölmek çok önemlidir.

## Darboğazları Önlemenin En İyi Yolu: Çalışanları Eğitmek

Sonuç olarak, darboğazları önlemenin en iyi yolu, ekiplerinizi sürecin her yönü hakkında eğitmektir.

Hayır, geliştiricilerin Kubernetes uzmanı olmalarını beklemiyorum. Aynı şekilde, operasyon ekibinin her hafta Java’da yeni özellikler oluşturmasını da beklemiyorum. Ancak çapraz eğitim (cross-training) sağlamak, mühendislerin daha uyumlu ve esnek hale gelmelerini sağlar, böylece alternatif çözümler bulabilir ve sistem kesintilerini azaltabilirler. Ayrıca, bir ekipten diğerine iş devredildiğinde ortaya çıkan karışıklığı da azaltır. 
