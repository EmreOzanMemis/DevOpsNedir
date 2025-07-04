#  Bakış Açınızı Değiştirerek Bakın | DevOps Nedir ? 

Her yazılım geliştiricinin kariyerinde bir an gelir ki anlar: Yazılım tasarımı, sadece klavyede kod döşemekten ibaret değildir. Özellikle DevOps kültürü sahneye çıktığından beri, geliştirme ve operasyon el ele verip bir yazılım projesini uçtan uca düşünmek zorundadır. Bu makalede, yeni başlayanlardan kıdemli mühendislere kadar herkesin yüzünü güldürecek (belki yer yer acı acı güldürecek 😅) bir üslupla, yazılım ekiplerinin tasarım aşamasında DevOps ilkelerini nasıl benimseyebileceğini inceleyeceğiz. Hazırsanız kahvenizi kapın, çünkü birazdan kod yazmaktan fazlasının neden bu kadar önemli olduğunu hem konuşacağız hem de birlikte tebessüm edeceğiz.

DevOps’u benimsemek, her bir kişiye, sürece ve ürüne DevOps’un temel felsefelerini aşılamaya yönelik bir taahhüttür. Ekibinizin ürettiği yazılım, birçok açıdan ekibinizin değerlerinin ve ilkelerinin bir yansımasıdır. Eğer yazılımınız bu metodolojiyi yansıtmıyorsa, ne metodoloji ne de teknolojiniz işe yarayacaktır.

Bir ürün ekibinin yaptığı en büyük hatalardan biri, mühendisliği tasarım sürecine çok geç dahil etmektir. Ürününüzden herkesin haberdar olduğundan, temel iş hedeflerinin anlaşıldığından ve planlama sürecine dahil edildiğinizden (ya da dahil olmaya teşvik edildiğinizden) zaten emin oldunuz. Meslektaşlarınız beyin fırtınası sürecine katıldı, öneriler sundu ve hangi özelliklerin ürünün başarısı açısından en kritik olduğuna dair ortak bir anlayışa vardı.

Bu bilgi paylaşımı sistemin tasarımı başladığında durmamalıdır. Evet, kararlar alınmalıdır ve bazen ortalıkta çok fazla “aşçı” varmış gibi hissedebilirsiniz. Her kararda demokratik bir oylama yapmanızı önermiyorum. Hiyerarşi, mühendislik ekiplerinde genellikle kritik bir rol oynar ve liderlik, tüm seçenekler masaya yatırıldığında net kararlar alabilmelidir.

Ancak burada önemli olan şu: Tüm seçenekler masaya yatırıldığında. Tüm seçenekleri ortaya koymak, herkesin sürece dahil olmasını gerektirir. Planlama sürecinde oluşturduğunuz ivme, tasarım sürecinde de devam ettirilmelidir.

## DevOps ile yazılım tasarımı neden sadece “kod yazmak” değildir

Yazılım geliştirme dünyasına yeni adım atanlar için tasarım çoğu zaman arka planda kalan bir gölgedir; esas iş kod yazmaktır, değil mi? Aslında yanlış! İyi bir yazılım tasarımı, hikâyenin tamamıdır ve kod sadece bu hikâyenin cümlelerinden biridir. Nasıl ki bir roman sadece birkaç cümleden ibaret değilse, yazılım geliştirme de sadece kod satırlarından ibaret değildir. Bir özelliği tasarlarken, onu nasıl inşa edeceğimiz kadar neden ve hangi bağlamda inşa ettiğimiz de önemlidir.

DevOps bakış açısıyla düşündüğümüzde, daha kodun ilk satırını yazmadan planlama, mimari, altyapı ve operasyon boyutlarını masaya yatırırız. Kodun çalışacağı ortamı, yaşayacağı kullanıcı senaryolarını, karşılaşacağı yükü öngörmek tasarım sürecinin parçasıdır. Kısacası, yazılım tasarımı bir ekip sporu gibidir: Kodcular, testçiler, operasyoncular herkes aynı oyun planına göre hareket etmelidir. Aksi halde, geliştirdiğiniz uygulama geliştirici makinesinde sorunsuz çalışıp sunucuda tuhaf dramalara yol açabilir (“Bende çalışıyordu, sunucuda neden çalışmıyor?!” diye başlayan cümleler tanıdık geldi mi? 😉). İşte bu yüzden, DevOps ile tasarım yapmak demek, daha en başından itibaren her adımı ortak akılla ve geniş bir vizyonla planlamak demektir.

Yazılımda mimari, bir sistemin yüksek düzeyde yapısını tasarlamayı ifade eder. Bu yalnızca gerçek tasarımı değil, aynı zamanda mimari dokümantasyonu da kapsar bu, yazılım sistemlerinde sıklıkla eksik olan bir kalitedir. Bunu tüm yazılım ürününüz için bir plan gibi düşünün; her bir parçanın nasıl çalışacağını ve birbirleriyle nasıl etkileşimde bulunacağını gösterir.

Yüksek düzey bir tasarım üzerinde çalışırken, sağlam bir çerçeve oluşturmak için dikkate alınması gereken onlarca konu vardır. Tüm bu konularla başa çıkmak, sadece bir ürün yöneticisinin yeteneklerini değil, aynı zamanda mühendislerin güçlü katılımını da gerektirir. Bu katılım, iyi geliştirilmiş ve sürdürülebilir bir yazılım ürünü oluşturmanız için hayati önemdedir.

İnsanların “iyi” kodu tanımlamak için birçok yolu vardır. Ben iyi geliştirilmiş yazılımı “performant” (etkin performans gösteren) olarak tanımlarım; yani yazılımınızın ihtiyaç duyduğunuz düzeyde ve biçimde çalışabilmesidir. Bu tanım kasıtlı olarak belirsizdir çünkü büyük ölçüde ürününüze ve kullanıcıya bağlıdır. Performant, uygulamanızın yanıt verme hızı ve kullanıcıya sunduğu deneyim anlamına gelebilir. Aynı zamanda veri güvenilirliği ve erişilebilirliği anlamına da gelebilir.

Örneğin, müşteri verilerinizin her an doğru ve erişilebilir olup olmadığını düşünün. “Performant” kodun sizin, ekibinizin ve müşterilerinizin gözünde ne anlama geldiğini önceden düşünün. Yazılımınızı belirli performans ihtiyaçlarına göre nasıl tasarlayabilirsiniz?

Geleneksel mühendislik ekiplerinde, geliştiriciler (yani kodu yazanlar), operasyon uzmanlarından ayrı tutulurdu. Operasyon uzmanları, uygulamayı çalıştırmak ve altyapısını korumaktan sorumlu kişilerdi. Bu ayrım, insanların “Karışıklık Duvarı (Wall of Confusion)” dediği, geliştiricilerin kodu yazıp operasyon ekibine fırlattığı metaforik bir duvara neden oldu.

Pek çok organizasyon kendilerini Agile ya da DevOps olarak tanımlasalar bile hala bu şekilde çalışıyor. İş ekipleri, pazardaki ihtiyaçlara karar veriyor; satış ekipleri müşteri isteklerini (ya da verilen vaatleri) aktarıyor; ürün yöneticileri ise tasarımı yapıyor ve yalnızca uygulama kısmı için mühendislik ekibine devrediyor.

Bu tür bir iş akışı, DevOps’un tam tersidir (anti-pattern) ve kesinlikle işe yaramaz. Mühendisler kod makinesi değildir. Görevleri haftalık 40 saatlik kod üretmek değil, uzmanlıkları ile katkı sağlamaktır. Onları sürece dahil etmezseniz, sürdürülebilir bir yazılım ürünü geliştiremezsiniz.

KODLA → DERLE → TEST ET → YAYINLA → BAKIM

Ve sürekli deavam eden tekrarlar.

DevOps ile ekipleriniz sürekli olarak bilgi paylaşmalı ve iş birliği içinde çalışmalıdır. Roller, içinde kalınması gereken keskin sınırlar yerine uzmanlık alanlarını ifade eder. Önceden roller birbirinden tamamen yalıtılmıştı; roller arasında neredeyse hiç geçiş yoktu. DevOps, bilgi paylaşımı ortamı ve her rol ile yazılım teslim süreci aşaması arasında sorumluluğun paylaşıldığı bir yapı oluşturur. Böylece geliştiriciler yalnızca kendi kodları için test yazmakla kalmaz, test mühendisleri de uç durumları belirlemeye veya geliştirme önerileri sunmaya katkı sağlar.

Bu makalede süreçlerin her aşamasını doğrusal bir hat gibi ele alıyorum. Bu doğrusal yaklaşımı her faza DevOps'u nasıl entegre edebileceğimize dair ayrıntılı inceleme yapmak için kullanıyorum.

Tahmin edilebileceği üzere, proje sahipleri bazen kaynaklarla mümkün olmayan fikirlerle gelirler. Ancak mühendislerin eğitimi ve deneyimi sayesinde, müşterinizin problemlerini çözmenin en iyi yolunu hızlıca belirleyebilir, özelliklerin karmaşıklığını değerlendirebilir ve zaman ve kaynak maliyetleri hakkında genel önerilerde bulunabilirler.

İtiraf: Bir Operasyoncu, danışman yada proje yöneticisi olarak geçirdiğim zaman boyunca, geliştirme süresiyle ilgili tek bir tahminin bile doğru çıktığını görmedim. Gerekli zaman miktarı her zaman bir tür “bilinçli tahmin”dir.

Zaman tahminlerinin doğruluğu, mühendislerin belirli bir zaman çizelgesine uyması gerektiğine inanmalarıyla daha da karmaşık hale gelir. Bu beklenti açıkça dile getirilmese bile. Her zaman zaman tahminlerini iki katına çıkararak beklenmedik engeller ve zorluklar için yeterli alan bırakılmasını öneririm. Güvenin bana, müşterileriniz ürünü altı ay erken teslim ettiğiniz için şikayet etmez. Ancak altı gün bile geç teslim ederseniz, neredeyse kesinlikle mutsuz olacaklardır.

Geliştirme sürecinin ileriki aşamalarında ortaya çıkabilecek riskleri azaltmanın en iyi yolu, herkesin en başından itibaren masada olmasını sağlamaktır. Bu planlama ve tasarım aşaması, herkesin fikirlerini, görüşlerini ve endişelerini paylaşma fırsatı sunar. Bu bilgi toplama süreci kaotik görünebilir. Uzmanlardan oluşan bir kakofoni gibi hissedilebilir ancak doğru uygulandığında genellikle daha iyi yazılıma yol açar. Yazılım tasarımı sırasında akılda tutulması gereken üç yaklaşım:

Mühendislerden ilk geri bildirimi alın. Mühendislerin her bir özelliğin ne kadar karmaşık olacağını değerlendirmesine izin verin. Ürün yöneticileri bu sayede mühendislik perspektifinden fayda sağlarken, mühendisler de nelerin geliştirildiğine dair erken bir fikir edinir (ve hangi teknolojilere odaklanmaları gerektiğini anlarlar).

Analiz için zaman tanıyın. Mühendislik ekibinizin ajandasında zaman ayırarak ürün yöneticileriyle konuşmalarını, önerilen fikirleri değerlendirmelerini ve olası çözümleri düşünmelerini sağlayın. Tüm cevapları tek bir 3 saatlik toplantıda alamayabilirsiniz. Çoğu zaman mühendislerinizin toplantıdan sonra biraz düşünmesi ve size geri dönmesi gerekir. Onlara araştırma yapma şansı verin, böylece size en doğru ve bilgili yanıtı verebilirler.

Tasarım için özel bir mühendis ekibi görevlendirmeyi düşünün.Bazı şirketler, mimari ekiplerin oluşturulmasını destekleyecek kadar büyüktür. DevOps bakış açısıyla bu ekip, kendilerine bir grup özellik atanıp bunları sıralayan sıradan bir ekip değildir. Bunun yerine, yüksek düzey sistemleri tasarlama konusunda benzersiz niteliklere sahip uzman mühendislerden oluşurlar. Düşük seviye detaylar yerine ürünü bir bütün olarak belirli yollarla etkileşime giren özelliklerden oluşan bir ağ gibi düşünürler.

## “Performant” kod yazmak nedir ve neden önemlidir?

Gelelim havalı bir tabire: performant kod. Dilimize yerleşen bu deyim, aslında “yüksek performanslı, verimli kod” anlamına geliyor. Peki neden bu kadar gündemde? Çünkü kullanıcılar sabırsızdır, sistemler nazlıdır, bütçeler de kısıtlıdır. Performant kod yazmak, yazdığımız yazılımın hızlı çalışması, kaynakları gereksiz yere sömürmemesi ve ölçeklenebilir olması demektir. Eğer kodunuz bir kaplumbağa hızıyla çalışıyorsa 🐢, kullanıcılar çoktan rakip ürüne geçmiş olabilir; veya kodunuz kaynakları hoyratça kullanıyorsa, bulut faturanız CIO’nuzu ağlatabilir.

Gerçek hayattan bir örnekle önemini vurgulayalım: Amazon’un yaptığı bir araştırmaya göre, sayfa yükleme süresine eklenen her 100 milisaniye gecikme satışları %1 oranında düşürebiliyormuş. Düşünün, sadece bir göz kırpma süresinde müşterilerinizi kaybedebilirsiniz! “Performant” kod, işte bu yüzden altın değerinde. Hem kullanıcı deneyimini iyileştirir hem de sistemlerin ölçeklenmesini kolaylaştırır. Unutmayalım, kodumuz çalışıyor olabilir ama iyi çalışması bambaşka bir meziyet. Yani, kodunuz sadece işi yapmasın, bunu Formula 1 arabası gibi yapsın 🏎️ hızlı, dengeli ve güvenilir.

Değişime uygun yazılım tasarlamak. Geliştiricilerin eski kodlarla çalışmaktan nefret etmesinin nedeni, önceki mühendislerin kötü olması değildir. Gerçek şu ki bu eski kodlar, bağlam ve koşullar çok değiştiği için artık işe yaramamaktadır. Bu kodlar modası geçmiş olabilir, ve yazılım dünyasında bu çok hızlı olur.

Diğer bazı sektörlerin aksine, yazılım geliştirme yüzlerce yıldır var olan bir alan değildir. Temel ilkeleri netleşmiş bir yapıya sahip değildir. Yazılım hâlâ bebeklik dönemindedir; hızla evrilir ve geliştiriciler de bu yolculukta beraberinde sürüklenir.

Yazılımınızı, değişen müşteri ihtiyaçlarına uyum sağlamak üzere kolayca güncellenebilir şekilde inşa edin. Yeni ihtiyaçlara hızlıca uyum sağlayabilmesi için mimarinizin esnek olması gerekir.

Değişime uyum sağlamanın yanı sıra, yazılımınızı yeniden kullanılabilir olacak şekilde inşa etmeniz de gerekir. Bileşen Tabanlı Geliştirme (Component-Based Development), birbirinden bağımsız, tekrar kullanılabilir ve kolayca yönetilebilir bileşenler geliştirmenin yoludur.

Kod zamanla değişecek olsa da, büyük değişikliklerin tüm sistemi etkilemesini engellemek için mimarinizi baştan esnek ve dirençli tasarlamalısınız. Başta daha fazla zaman alsa da, ilerleyen aşamalarda size büyük hız ve esneklik kazandırır.

Değişime uyum sağlamak için sisteminizin bileşenlerini aşağıdaki özelliklere sahip olacak şekilde tasarlayın:

  Bağımsız (Independent)
  Kendi kendine yeterli (Self-contained)
  İyi belgelenmiş (Well-documented)
  Standartlara uygun (Standardized) ≫ Taşınabilir (Portable)

Bu nitelikler sayesinde kod, başka bir yere taşınabilir ya da farklı donanımlar üzerinde çalışabilir hâle gelir. Aynı zamanda kodun bakımını kolaylaştırır, çünkü yeni gelen mühendisler kodu daha kolay anlayabilir.

## Mühendislik ekiplerinin duvarı: “Handoff” kabusu ve nasıl yıkılır?

Geleneksel yazılım süreçlerinde bir ekip bir işi bitirir, topu öbür ekibe atar, sonra arkasına bile bakmazdı. Bu “handoff” dediğimiz devir-teslim anları, mühendislik ekiplerinin önüne örülmüş görünmez duvarlar gibidir. Geliştirme ekibi “Biz kodu yazdık, hadi operasyon ekibi bunu alsın çalıştırsın” der, test ekibi “Biz onayladık, gerisi sizlik” der… Sonuç? Kaçınılmaz olarak bilgi kaybı, karşılıklı suçlamalar ve bolca stres. Bu yaklaşım tam bir kâbus değil de nedir? 😱

DevOps kültürü bu kabusa uyanmanın alarmıdır adeta. “Benim işim kodu yazmak, gerisi ops’un sorunu” devri kapanmıştırtr. Artık ekipler arasında duvarlar değil, köprüler inşa ediyoruz. Geliştirici, tester, operasyon, herkes ürünün başarısından ortak sorumluluk alır. Handoff kabusunu yenmenin ilk adımı, ekibi tek bir ürün takımı olarak düşünmektir. Herkes sürece daha en başından dahil olursa, kimse kimseye bir işi “atmıyor”, birlikte yürütüyor demektir. Daha önceki makalelerimde de söylediğim gibi eğer herkes sadece kendi bölümündeki işi yapıp sonra paslarsa, bu yeni silo’lar yaratır; oysa amaç tam tersidir. Bu duvarları yıkmak için yapabileceğiniz şeyler belli: iletişimi artırmak, süreçleri şeffaflaştırmak, ortak araçlar kullanmak ve mümkün olduğunca otomasyonla işi akışkan hale getirmek. Unutmayalım, hepimiz aynı gemideyiz; kaptan köşkünde ayrı, makine dairesinde ayrı hayat yok. 😉

Yazılımınızı ve sistemlerinizi sürekli olarak geliştirmeniz gerekir. Yeni tasarımlar ve genişleyen kodlar tutarlı mı? Verilen bir karar mimariyle uyumlu mu? Diğer servislerle aynı standartlara mı sahip?

Sistem büyüdükçe ve ekip sayısı arttıkça, kodun farklı kişilerce yazıldığı belli olur. Başta bu doğal gibi gelebilir ama sürdürülebilir değildir.

Kod tabanınız (altyapı kodları dahil) mümkün olduğunca tek bir kişinin yazmış gibi görünmelidir. Mükemmeliyet ulaşılmaz olabilir, ama bu uğruna çabalamamanız gerektiği anlamına gelmez.

Editörlerin yazı yazarken belirli dil kurallarına bağlı kalmaları gibi, yazılım mühendisleri de kodlarını düzenlemek için lint araçları kullanır. Bu araçlar, kod stilinde tutarlılığı sağlar ve ekibin temel stil kararlarını vermesine yardımcı olur. Böylece küçük ayrıntılar örneğin her satırın sonunda noktalı virgül olup olmaması gibi otomatik hale gelir.

Eğer ekibiniz bir araya gelip bu kurallar üzerinde anlaşamıyorsa, bu büyük bir iş birliği sorunudur.

Linter, küçük konular için faydalıdır. Ancak büyük kararlar örneğin API tasarımı daha fazla öngörü ve disiplin gerektirir. Kod incelemelerini (code review) yeterince güçlü şekilde önermeliyim. İncelemeyi yapan kişinin kıdemli olması gerekmez; sadece kodu okuyarak doğru soruları sorabilmelidir.

## Yazılım mimarisi çizerken neden tüm ekip masada olmalı

Mimarlarınızı veya en kıdemli mühendislerinizi tüm kod incelemelerine (code review) dahil edin. Bir özelliğin daha büyük kod tabanına entegre edilmeden önce mimari açıdan incelenmesi, mimari bütünlüğün korunmasını sağlar. Bu süreç hem mimarın hem de geliştiricinin ortak bilgi paylaşımından faydalanmasını sağlar. Mimar, özelliğin nasıl geliştirildiğini ve hangi araçlarla yapıldığını öğrenir. Geliştirici ise, kodunun takım arkadaşlarıyla tutarlı olmasını ve temiz, iyi belgelenmiş bir kod tabanı oluşturmayı öğrenir.

Büyük resmi çizerken küçük ayrıntıları kaçırmamak için herkesi masaya davet etmek şart. Yazılım mimarisi tasarlarken sadece mimar ve birkaç geliştirici kafa kafaya verirse, ortaya kâğıt üstünde harika ama gerçek dünyada problemli bir tasarım çıkabilir. Neden mi? Çünkü belki veritabanı yöneticisinin “Bu yapı ileride ölçeklenmez” uyarısını, güvenlikçinin “Şurada açık olabilir” çekincesini, ya da ops ekibinin “Bunu kurmak için özel sihir lazım mı?” sorusunu duymadan plan yapmış olursunuz. Sonra gerçek dünyada bu eksikler birer birer ortaya dökülür. İşte bu yüzden tüm ekip masada olmalı diyoruz.

Bir yazılım mimarisi çizmek, bir şehir planlamak gibidir. Sadece yolları çizerseniz, su tesisatını unutuverirsiniz. DevOps bakış açısıyla, mimari tartışmalarına geliştiricisinden test uzmanına, güvenlikçisinden operasyoncısına kadar herkesin katılması altın değerindedir. Herkes masada olursa, daha tasarım aşamasında “Bu login servisini yaparız ama deploy ederken şu adımlara dikkat gerek” ya da “Şu modül çok trafik çekecek, altına sağlam bir altyapı düşünelim” gibi hayati noktalar gündeme gelir. Böylece sonradan “Keşke X ekibiyle başta konuşsaydık” demeye gerek kalmaz. Kısacası, mimari tasarım bir kolektif akıl işidir. Herkesin fikrini alıp mayaladığınızda ortaya gerçekten kabarıp leziz bir çörek çıkar. Aksi takdirde, tek kişinin yoğurduğu hamur fazla tuzlu olabilir. Tüm ekip masada olunca, “Bende çalışıyordu, prod’da niye patladı?” dramaları da azalır, çünkü herkes en baştan o prod’un şartlarını bilir.

## Hatalar, tahminler ve kodla gelen kahinlik: Sürekli gelişim kültürü

Yazılım dünyasında geleceği gören bir kahin yoktur, ama hepimiz bazen kahinlik yapmaya çalışırız: “Şimdi bu kodu böyle yazıyorum ama ileride şöyle bir özellik isterler, ben en iyisi şimdiden buna hazırlıklı olayım” deyip kendimizi tahmin oyunlarına kaptırırız. Kimi zaman da hataları asla yapmayacağımızı varsayarız (hah, tabi ya 🙃). İşte DevOps’un benimsediği sürekli gelişim kültürü, bu kahinlik heveslerini ve “ben asla hata yapmam” kibirini bir kenara bırakmamızı söylüyor.

Sürekli gelişim kültüründe hatalar utanılacak şeyler değil, öğrenme fırsatlarıdır. Bir şey production’da patladı mı? Dünyanın sonu değil, hemen kollar sıvanır, post-mortem yapılır, kök neden bulunur ve ders alınır. Sonra da “Peki biz bunu baştan nasıl önlerdik?” diye düşünülür. Bu kültürde ekipler sürekli iyileştirme peşindedir, her döngüye bir önceki döngünün dersleriyle girer. Yani bir nevi, yazdığımız her kod parçası bize geleceğe dair küçük ipuçları verir ama asıl önemli olan, bu ipuçlarını değerlendirip sistemi sürekli evrimleştirmektir. Tahminlerimizi gerçek verilerle güncelleriz, süreçlerimizi her seferinde biraz daha cilalarız. Böylece ekip olarak bir sonraki sprint’te dünün kendimizden daha akıllı hareket ederiz. Unutmayın, “fail fast, fail safe” mottosu boşuna ortaya çıkmadı: Hızlı hata yapın ki hızlı öğrenin, ama hatalarınızı güvenli ortamlarda yapın ki kimseye zarar vermesin. Bu felsefeyi benimseyen ekipler, zamanla adeta kendi kendini eğiten, tecrübe puanını sürekli artıran RPG karakterleri gibi level atlıyor diyebiliriz. 🧙♂️

İyi belgelenmiş yazılımlar oldukça nadirdir ve bunun bir nedeni vardır: Süreleriniz vardır. Hayatımda belgeleri terfi ya da ödül ile ilişkilendirilmiş bir geliştirici görmedim. Belki de bu durum değişmelidir.

Dokümantasyonun birçok amacı vardır ama yalnızca kodun ne dediğini İngilizce’ye çevirmekle sınırlı kalmamalıdır. Bu konuyu GitHub Copilot makalemde detaylı anlatmıştım. Artık AI kullanmak bir ayıp değil aksine kullanmamak bir zaman kaybı olabilir. O yüzden bir asistan gibi angarya gibi gelen süreçlerde bu kod asistanından faydalanmak hem keyif hemde zaman kazandıracaktır.

Tabi gereksiz yorumlar zamanla modası geçmiş ve kafa karıştırıcı hale gelebilir. Kod değiştikçe belgeler de güncellenmelidir. Tabi dokumanlar ve yorumlarda...

Kodunuz, ona bakan geliştiriciye sadece ne yaptığı değil, neden böyle yapıldığı hakkında da bilgi verecek şekilde belgelenmelidir. Belirli bir kısmın sistemin geneli içindeki yeri ne? Alternatifler nelerdi? Bu uygulama neden seçildi? Hangi görevler hâlâ yapılmadı (TODO)? Bu yazılımın teknik borcu ne kadar?

Dokümantasyon, geliştiriciden geliştiriciye (ya da gelecekteki kendinize) bilgi aktarımı sağlar. Bu da DevOps’un temel değerlerinden biridir.

Yazılımınızı değişime dayanıklı ve sürdürülebilir bir hale getirmek için kodu yaşayan bir belge (living document) gibi düşünün. Kodun ve ürünün zamanla nasıl geliştirildiğini açıklayan bu belge, ekip içinde bilgi paylaşımını sağlar. Bu yaklaşım uzun vadede daha az çatışma, daha hızlı döngüler ve daha sürdürülebilir bir yazılım sağlar.

## DevOps’un Yetkinliği İçin Kod Mimarisi

Bir mühendis ve ürün sahibi yeni bir ürünün teknik tasarımında birlikte çalışırken, mühendis hem fonksiyonları hem de bu fonksiyonların nasıl etkileşim kurduğunu dikkate alarak mimari öneriler sunar. Projenin başında belirlenen mimari, ileride alınacak kararları doğrudan etkiler.

Bu yapı sistemi ne kadar esnek yapar? Hangi alanlara yeni şeyler eklenebilir? Mimarlar sistemin nasıl yapılandırılacağına, hangi özelliklerin öncelikli olacağına ve kodun nasıl standartlaştırılacağına karar verirler. Aynı zamanda mühendislik ekibinin işi nasıl ele alacağını da şekillendirirler.

Genel olarak, mimarlar sistem performansını etkileyen altı temel başlık üzerinde dururlar.

## Güvenlikten kullanılabilirliğe, esneklikten ölçeklenebilirliğe: yazılımın altı süper gücü

Bir yazılım ürününün süper güçleri dendiğinde aklınıza belki uçmak, görünmez olmak gelmiyor olabilir; bizim bahsedeceğimiz süper güçler biraz daha mühendislik işi. DevOps perspektifinde, iyi bir yazılım tasarımının altı temel vasfı vardır ki bunlar onu sıradan uygulamalardan süper kahramana dönüştürür. Bir uzman makalede çok net vurgulanmış: kullanılabilirlik, güvenilirlik, ölçeklenebilirlik, erişilebilirlik, test edilebilirlik ve desteklenebilirlik, tek tek yeni özellik eklemekten daha önemlidir. Yani kalite özellikleri nicelikten önde gelir. Gelin bu süper güçlere tek tek bakalım:

  Güvenlik: Yazılımınız Thor’un çekici kadar güçlü olsun, eğer güvenlik zafiyeti varsa bir Loki çıkar, bütün sistemi altüst eder. Güvenlik en baştan düşünülmeli; şifreler açıkta log’lara yazılmasın, veri şifreleme, güvenli kimlik doğrulama... Kısacası, özelliğiniz çalışsa da çalışmasa da güvenli olmalı. DevOps’ta “DevSecOps” akımı da güvenliğin ilk günden ele alınması gerektiğini savunur. DevSecOps, DevOps hareketinden doğmuştur ve güvenliğin herkesin sorumluluğu olduğunu topluluğa hatırlatmak için vardır. Tıpkı geliştiriciler ve operasyon ekiplerinin kendi görevleri olduğu gibi, güvenlik de yalnızca belirli kişilere ait bir sorumluluk değildir. Geçmişte güvenlik genellikle düşmanca bir ilişkiyle ele alınırdı geliştirme tamamlanır, güvenlik en sonda gelip hataları engellerdi. Ancak DevSecOps, "güvenliği sona bırakma" anlayışının yerine "güvenliği en baştan dahil etme" fikrini savunur. Yani güvenlik, yazılım geliştirme yaşam döngüsünün başlarında planlama ve tasarım süreçlerine entegre edilmelidir.
  Kullanılabilirlik: Uygulamanızın arayüzü ve deneyimi, süper güçlerin sevimli devi Hulk gibidir: Karmaşık olabilir ama kullanıcılar için anlaşılır ve rahat olmalıdır. Kullanılabilirlik, son kullanıcıya verdiğiniz değerin ilk hissedildiği yerdir. Tasarım aşamasında kullanıcı hikâyelerini, deneyim akışlarını hesaba katmak şart. Kullanılabilirlik, bir kullanıcının sisteminizi ne kadar kolay kullanabildiğini tanımlar. Kullanılabilirlik; kullanıcı arayüzü (UI) ve kullanıcı deneyimi (UX) tasarımının temelidir. Uygulamanızla olan her etkileşim bu kavram üzerinden düşünülmelidir.
  Esneklik: Değişime hızlı adapte olabilme yeteneği. Yarın yeni bir özellik eklemek istediğinizde tüm sistemi yıkıp baştan kurmak zorunda kalmamak için yazılımınız esnek olmalı. Modüler mimariler, soyutlamalar, arayüzler bu esnekliği sağlar. Esnek bir tasarım, pivot etmeniz gerektiğinde size kanat takar 🦋. Esnek bir sistem, müşterinin değişen ihtiyaçlarına hızlıca uyum sağlayabilen sistemdir. Esnek kod tabanı, büyük kesintilere yol açmadan yeni kodları entegre edebilir.
  Ölçeklenebilirlik: Bugün 100 kullanıcıya hizmet veren uygulama, yarın 100 bin kullanıcıya çıkarsa ne olur? İşte ölçeklenebilirlik bu senaryoda devreye girer. Yazılımın artan yük altında aynı performansı koruyabilmesi, yatay/dikey ölçekleme yapısına uygun tasarlanması gerekir. “Performant kod” yazmak da burada tekrar sahne alıyor; kodunuz ölçeklenmeye hazır olmalı. Bir sistemin ölçeklenebilirliği, yeni kaynaklar eklendiğinde sistemin daha iyi performans gösterip göstermediğiyle ölçülür. Eğer gösteriyorsa, sistem ölçeklenebilirdir. Göstermiyorsa, önünüzde uzun bir yol olabilir. Uygulamanızı ölçeklendirmek, sürecin erken aşamalarında zor olabilir. Henüz 200 kullanıcınız yoksa bile, startuplar ve yeni ürünler için ilk endişe genellikle ölçeklenebilirlik değil, herhangi bir kullanıcı kazanabilmektir. Ancak büyümeyi düşünerek yazılımın daha fazla kullanıcıya ulaşabilmesi için ne gibi yollar izlenebilir bunu değerlendirmek iyi bir fikirdir. Yine de büyüme hedefi, kısa vadede sizin için en kritik olan konuları gölgelememelidir. Bulut için tasarlanan uygulamaların avantajlarından biri, esneklik (flexibility), dayanıklılık (resilience) ve evet, doğru tahmin ettiniz otomatikleştirilebilir ve iyileştirilebilir ölçeklenebilirlik sunmasıdır.
  Sürdürülebilirlik: Yazılımınızın arıza toleransı ve hata karşısında sağlam kalabilmesi. Bir parça çökerse tüm sistem domino taşları gibi yıkılmasın. Yedeklilik, hata ayıklama mekanizmaları, otomatik yeniden başlatma gibi önlemlerle sistemin güvenilirliği sağlanır. Unutmayın, kullanıcılar yazılımınıza güvenirse, tekrar gelir; güvenilmez bulursa kaçar. Kod değişir. Yeni özellikler eklenmeli, eski olanlar kaldırılmalı veya bakım moduna alınmalıdır. Mevcut özellikler evrim geçirir. Yazılım güncellenmelidir. Değişim kaçınılmazdır ve buna hazırlıklı olunmalıdır. Yazılımınızın sürdürülebilirliği, değişim karşısındaki direnci ile doğrudan ilişkilidir. Kodunuz kapsamlı bir otomatik test süiti ile test edilmelidir. Manuel testler bir yere kadar götürür. Modern sistemler çok karmaşıktır; iki kişi ekrana bakarak “her şey yolunda mı?” diyemez. Kodun, kabul kriterlerini karşıladığından emin olmanız gerekir. Yani, bir özelliğin gerçekten çalıştığını nasıl anlarsınız? Uç senaryoları da test etmelisiniz. Hayal edebilirsiniz: Bir dizi parametre olarak girildiğinde ne olur ama kod bir hash bekliyordur? Ya e-posta adresinde @ işareti eksikse? Her hata düzeltildiğinde, o hatanın gerçekten çözüldüğünden emin olmak için yeni bir test eklemelisiniz. Bu testler size, yeni kodun mevcut özellikleri bozup bozmadığını kullanıcılar etkilenmeden önce bildirir. Kodunuzu belgelemeniz gerekir. Belgeleme, neredeyse tüm mühendislik ekiplerinin zorlandığı bir şeydir. Çünkü genellikle belgeyle değerlendirilmezler. Onlardan beklenen, sadece özelliği tamamlamak ya da bir hatayı düzeltmektir. Ancak bu ölçüm, uzun vadede yeterli değildir. Bu durumu iyileştirmek için kod incelemelerine belgeleme kriteri de ekleyin. Karar matrisini ve geliştiricinin yaptığı tercihlerde neleri dikkate aldığını belgeleyin. Hangi alternatifler düşünüldü? Neden bu çözüm seçildi? Bu bağlam, daha sonra (özellikle kodu ilk yazan kişi artık ekipte değilse) büyük değer taşır. Ve unutmayın: kod değişirse, testler ve belgeler de değişmelidir.
  Test Edilebilirlik: Süper güçlerin belki de en gizli kahramanı. Kodunuz ne kadar test edilebilir ise o kadar hızlı geliştirme yapabilirsiniz. Otomasyon testleri, birim testleri, entegrasyon testleri tasarımınızın ayrılmaz bir parçası olmalı. Test edilebilir bir tasarım, sürekli entegrasyon ve sürekli teslimat (CI/CD) hattında size ışık hızı kazandırır. Testleri geçemeyen kod üretime çıkamaz; bu da kaliteyi güvence altına alır.

Bu altı süper güç, özünde yazılımın niteliğini belirler. Özellik tasarlarken bu güçleri göz ardı etmek, süper kahramanı pelerininden mahrum bırakmaya benzer. Sonuçta uçar ama rüzgar alır, üşütür 😊. İşin şakası bir yana, DevOps yaklaşımı bu kalite özelliklerini en baştan gözetmeyi öğütler. Çünkü sonradan eklemeye kalkmak ya çok pahalıya patlar ya da imkânsız hale gelir.

## Geldik bu bölümün finaline...

Buraya kadar okuduysanız muhtemelen kafanızda şöyle bir soru var: “İyi hoş, bütün bunları yapacağız da, bunları uygulamak emek istemiyor mu?” Elbette istiyor. Bu noktada küçük bir sitemimi de iletmeden geçemeyeceğim: Kodlarına tek bir yorum satırı bile eklemeyen geliştiriciler, lütfen bunu bir daha düşünün 🙏. Çünkü yazdığınız kodu bir ay sonra siz bile anlamakta zorlanıyorsanız, ekip arkadaşlarınız ne yapsın? İyi bir dökümantasyon ve yorum alışkanlığı, DevOps’un bilgi paylaşımı ruhuna en yakışan davranışlardan biridir. Unutmayın, kod insana da hitap eder, sadece makineye değil.

Ve gelelim teşekküre: Yazılım mimarları ve ekip liderleri, sizlere kocaman bir alkış 👏. Neden mi? Çünkü bu DevOps prensiplerini hayata geçirmek genelde sizin omuzlarınıza bakıyor. Ekipleri bir araya getirmek, herkesi aynı vizyona ikna etmek, tasarımın her boyutunu düşünmek… Kolay işler değil. İyi bir mimar, bir orkestra şefi gibi tüm enstrümanların uyum içinde çalmasını sağlar. Biz geliştiriciler belki sahnede solo atıyoruz ama arka planda o senfoniyi yazan mimarlara müteşekkiriz.

Son söz: Yazılım tasarımı bir yolculuk ve bu yolculukta DevOps prensipleri hem haritamız hem pusulamız. Kod yazmak elbette işimizin özü, ama etrafına ördüğümüz süreçler, ekip kültürü ve tasarım kararları olmadan o kod ne kadar parlayabilir ki? Hem eğlenceli hem öğretici olmaya çalıştığımız bu yazıda, umarım sizi biraz gülümsetirken düşündürebilmişizdir. Şimdi gidip kodunuza bir yorum satırı ekleyin veya bir takım arkadaşınıza teşekkür edin derim. Happy DevOps ve bol kahkahalı kodlamalar! 🎉
