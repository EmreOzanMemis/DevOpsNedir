Bu bölümü kendim gibi operasyon ekiplerini düşünerek yazdım. Amacım, yazılım ve operasyon geçmişi olmayan yöneticilerin yazılım geliştirme sürecini ve bunun gerektirdiği yüzlerce kararı anlamalarına yardımcı olmak. Bu, operasyon ekiplerinin kod hakkında daha özgüvenli konuşmalarını sağlayacak ve geliştiricilerin aldığı kararlar (ve bu kararlara eşlik eden hatalar) konusunda daha fazla empati kurmalarına katkıda bulunacağını düşünüyorum. Belkide sadece ben böyle düşünüyorum :) 

Bir geliştiriciyseniz, bu bölümdeki içerik size tanıdık gelebilir (gerçi iyi geliştirme uygulamaları konusunda bir tazeleme fena olmaz diyebilirsiniz). Bu bölümde, kod hakkında nasıl işbirlikçi bir şekilde konuşacağınızı, değişime karşı çevik kod nasıl yazılır ve yazılım kararlarının DevOps bakış açısından nasıl alınacağını tartışıyor olacağız. 

Yazılım geliştirme dünyası, dışarıdan bakıldığında ciddiyet dolu bir alan gibi görünebilir. Monitörlere kilitlenmiş yüzler, karmaşık kod satırları, kahve kokan ofisler... Ancak işin mutfağında neler oluyor bir bilseniz :) Aslında yazılım geliştirmenin gerçekleri hem eğlenceli hem de eğitici, adeta bir komedi sahnesi gibidir.

Hazır mısınız? O zaman başlayalım – nihayetinde "Deploy ettik, dua edin." anlarını birlikte yaşayacağız.
İletişim Kurmak

Bodrum katında yaşayan geliştirici klişesi artık modası geçmiş durumda. Teknolojide çeşitlilik ve kapsayıcılık hala bir zorluk olsa da, durum iyileşiyor. Geleneksel olmayan geçmişlerden gelen daha fazla insan sektöre katıldı ve bu sayede sektöre farklı eğitim ve deneyimler kazandırdılar. Bu çeşitliliğin faydalarından biri de, DevOps değerleriyle tamamen uyumlu olan kod hakkında iletişimin vurgulanması oldu.

Kod incelemeleri, kodun master branch de birleştirilmeden önce bir meslektaşınız tarafından gözden geçirilmesi süreci, bu bölümü makalenin ilerleyen kısımlarında, "Kodunuzu meslektaşlarınıza inceletmek” başlığı altında ele alınacağım. Ancak, kod hakkında iletişim kurmak kod incelemesinden çok daha önce başlar. Eskiden geliştiricilere gereksinimler verilirdi ve uygun özellikleri geliştirmeleri beklenirdi, ardından kod sadece QA ve güvenliğe gözden geçirme ve operasyonlara dağıtım için teslim edilirdi. DevOps bunu değiştirdi.

Bugün, geliştirici iletişimi işinizi rakiplerden ayırmak için gereken hızlanmanın kritik bir bileşenidir. Geliştirme tarafındaki mühendisler, gereksinimler belirlenmeden ve kullanıcı hikâyeleri oluşturulmadan önce, bir özelliğin veya ürünün bağlamını anlamak için işin farklı alanlarıyla yakın iş birliği içinde çalışır.

💡İpucu: Kullanıcı hikâyesi, bir özelliği kullanıcı bakış açısından tanımlamak için kullanılan Agile tabanlı bir yaklaşımdır. Geleneksel olarak, “Kullanıcı kayıt sürecini oluştur. E-posta ve şifreyi talep et.” gibi belirsiz gereksinimlerle yetinmek zorunda kalırdınız. Ancak kullanıcı hikâyeleri, geliştiriciye son kullanıcı bakış açısından daha net detaylar vererek büyük özellikleri küçük parçalara ayırmasını sağlar. İşte bir kullanıcı hikâyesine örnek:

  “Bir site ziyaretçisi olarak, ana sayfadaki bağlantıya tıklayıp kayıt formuna yönlendirilmek istiyorum.” 

Bu hikâye şu şekilde devam edebilir:

  “Bir site ziyaretçisi olarak, e-posta ve şifremle bir kayıt formunu doldurmak, Gönder’e tıklamak ve hesabımın oluşturulduğuna dair bir doğrulama mesajı almak istiyorum.” 

Eğer ekibiniz iletişim kurmuyorsa, iyi iletişimi teşvik eden uygulamaları hayata geçirmek için zaman ayırmanız gerekir. Kod incelemeleri ve olay sonrası değerlendirme oturumları, bir ekip olarak iletişim pratiği yapmak için fırsatlar sunar. Daha önceki yazılarımda söylediğim gibi, iletişim de diğer beceriler gibi geliştirilebilir. Öğrenilebilir ancak ustalaşmak zaman alır.

Ekibinize iyi bir geliştirici olmak için gerekli “yumuşak becerileri” geliştirme yollarını sunun. Hitabet eğitmenleri ve doğaçlama dersleri, iletişimde zorlanan geliştiricilerin becerilerini büyük ölçüde geliştirebilir. Aslında çoğu kişi, başkalarıyla nasıl ilişki kuracağı konusunda koçluk alarak daha empatik olabilir.

DevOps, tüm paydaşları ortak bir hedef doğrultusunda bir araya getirir ve iletişim bunun kritik bir parçasıdır. Eğer geliştirme ekibiniz homojense ve yeni bakış açılarına yeriniz varsa, takıma farklı bakış açıları getirecek geliştiricileri dahil ederek yeni bir soluk kazandırabilirsiniz.
Kodla İletişim: Satır Arasındaki Sohbetler

Bazen iki yazılımcı konuşmadan anlaşır; çünkü asıl sohbet kodun satır aralarındadır. Kod yorumları, değişken isimleri, commit mesajları... Hepsi küçük birer iletişim aracı. Örneğin, bir arkadaşım proje çıkmaza girdiğinde kodunun en üstüne esprili bir not düşmüştü: 

// TODO: Bu kod çalışıyorsa ben süper kahramanım. 

Bu küçük yorum satırı aslında çok şey anlatıyordu: Hem durumun vahimliğini mizahla ortaya koyuyor hem de kodu okuyacak olana göz kırpıyordu. Kod üzerinden şakalaşmak, yazılımcılar arasında yaygın bir terapi yöntemi!

Gerçek iletişim ise bazen pull request yorumlarında gizlidir. Bir kod incelemesinde 

  "Eline sağlık, küçük bir önerim var" 

cümlesini duyarsanız anlayın ki kodunuzda revizyon gerekiyor ama kibarca söyleniyor. 🙂 İtiraf edelim, hataları doğrudan yüzümüze vurmak yerine ufak bir emoji ya da nazik bir dille ifade etmek ekip içi barışı koruyor. Hatta bazen tek bir Stack Overflow linki paylaşmak, sayfalarca açıklama yazmaktan daha etkili olabiliyor. Ne de olsa eski yazılımcıların kutsal kitabı Stack Overflow'dur diye boşa demiyoruz. Artık GitHub Copilot bu tip durumlarda Batman'in Robini gibi duruma yetişiyor. 

Yazılımcıların kendi aralarında kullandığı dillere pelesenk olmuş bazı ifadeler vardır. Bu ifadeler dışarıdan tuhaf gelse de, biz ne demek istediğimizi çok iyi anlarız:

  "Kod çalışıyorsa, elleme!" 

  – Eğer sistem tıkır tıkır işliyorsa dokunma; bozulmayan sistemi kurcalamamak altın kuralımızdır.

  "Bug değil, özellik!" 

  – Hataları halının altına süpürmenin eğlenceli bir yolu. Bir şey düzgün çalışmıyorsa belki de özellikle öyle tasarlanmıştır diyerek kendimizi avuturuz

  "Abi bende çalışıyor, sende neden patlıyor bilmiyorum." 

  – Klasik “bende sorun yok” savunması. Ortam farkı mı dersiniz, evrende bir glitch mi bilinmez; ama biz sorunu önce başka yerde ararız

  "Copilot'a dua etmeden iş yapamam." 

  – E malum, Stack Overflow veya GitHub Copilot olmasa çoğumuzun kodu çalışmazdı. Modern ve eski toprak yazılımcının gerçekten de kutsal bilgi kaynağı, adeta bacasız akıl hocası buraları :D 

Gördüğünüz gibi, yazılımcılar kendi diline ve esprilerine sahip. Kodla iletişim kurar, esprilerle stresi azaltır, gerektiğinde de birbirimize durumu esprili bir dille anlatır. Bu sayede hem iletişim kurar hem de kahkahayla çalışırlar, çalışırız . 😉
Imposter Sendromu

Günlük işlerine DevOps metodolojilerini entegre etmeye çalışan ekiplerle çalışırken, genellikle ekipteki geliştiricilerin operasyonel bilgi eksikliklerinden dolayı kendilerini biraz yetersiz hissettiklerini görüyorum. Aynı şekilde, birçok operasyon çalışanı da yazılımı sıfırdan geliştirme konusunda yeterli bilgiye sahip olmadıkları için kendilerini eksik hissediyor. Öğrenme sürecindeyken bile, her iki taraf da belirli bir düzeyde imposter sendromundan (sahtekârlık sendromu) muzdarip olabilir yani, yüksek başarıya sahip bireyler başarılarını içselleştirmekte zorlanır ve kendilerini bir sahtekâr gibi hissederler. Bu korkuyla, yani “yeterince iyi değilim” duygusuyla, birçok teknoloji çalışanı başa çıkmak zorunda kalıyor; yeterince hızlı üretmemek ya da yeterince çalışmamak endişesiyle.

İmposter sendromu, DevOps öğrenme ortamı oluşturma yetinizi şu şekillerde etkileyebilir:

  Sizi yetersiz hissettirir. Eğer kendinizi meslektaşlarınıza kıyasla daha az bilgili veya yetenekli hissederseniz, “aptalca” görünmekten korktuğunuz için soru sormaktan çekinebilirsiniz. Oysa soru sormamak, yapabileceğiniz en kötü şeydir. Çünkü bu durum, öğrenme şansınızı ve başkalarına öğretme fırsatınızı elinizden alır. Ayrıca, ekip içinde soru sormama kültürünü körükler.
  Öğretme güveninizi baltalar. Bilginiz olduğundan daha az katkı sağlayabileceğinizi düşünürsünüz. Aslında takıma şu anda güvendiğinizden çok daha fazlasını katma potansiyeliniz vardır. İmposter sendromu o küçük sesle size “Sen uzman değilsin” der. (Eee, ne olmuş yani?) Size kolay gelen bir şey, başkaları için zor olabilir. Bu yüzden anlatmaktan çekinmeyin.

Mükemmel bir DevOps kültüründe, mühendisler korkusuzca bildiklerini öğretir ve öğrenmeleri gerekenleri açıkça kabul eder. Bu noktaya gelene kadar, geliştiriciler ve operasyon ekipleri arasında yazılım teslimat sürecinin belirli aşamalarında geleneksel sürtüşmeler olabilir. Bu, geliştirmenin geliştiriciye ait bir alan olması sebebiyledir. Bu aşamada geliştiriciler kendilerini en özgüvenli, operasyoncular ise en savunmasız hisseder. Her iki tarafın imposter sendromu ve gururu, iş birliğini engelleyebilir. Oysa gerçek şudur: Her iki taraf da birbirine mutlak ihtiyaç duyar. Biri olmadan diğeri eksik kalır.
Hatalar İçin

Hata yönetimi, sürdürülebilir kod yazımının önemli bir parçasıdır. Sessiz hatalar, kod tabanınızda saklanan en tehlikeli unsurlardan biridir.

Zarif çıkışlar programları biraz daha ayrıntılı hale getirse de, bir hatanın nedenini açıklayan mesajlar göstererek programın durmasını engellemek veya yavaşlatmak yerine devam etmesini sağlar. Doğru şekilde ele alınmamış hatalara sahip programlar, garip ve beklenmedik şekillerde davranabilir — bu da hata ayıklamayı zorlaştırır.

Hataları ele alırken, müşterilere gösterilen mesajların anlamlı olduğundan emin olun. “418 durum kodu” ve “null pointer” hatası hakkında belirsiz bir mesaj, ortalama bir kullanıcıya hiçbir şey ifade etmez ve teknik olmayan kullanıcılar gözlerini devirecektir. Kullanıcı arayüzünüzü, kullanıcının neyin yanlış gittiğini, ne yapılması gerektiğini ve kime başvurması gerektiğini anlayabileceği mesajlar gösterecek şekilde tasarlayın.

Ayrıca, yalnızca açık ve anlamlı mesajlar değil; aynı zamanda geliştiricinin kodun tam olarak nerede başarısız olduğunu, hangi verilerin etkilendiğini ve bu verilerin kurtarılabilir olup olmadığını anlamasına yardımcı olacak bilgiler de sağlamanız gerekir. Her şey yolunda giderken çalışan programlar yazmak yeterli değildir. Harika geliştiriciler, potansiyel hataları ve olasılığı düşük durumları (edge case) düşünerek bu koşulları ele alacak kodlar yazar.
Sürdürülebilir Kod Yazma

Kodunuzu bir günlüğüne çalışsın diye yazmazsınız. (Gerçi bazen düşünüyorum da, bir şekilde bir kıyamet senaryosu interneti sağ bıraksa bile, çoğu sistem birkaç gün içinde çökerdi.) Ekibinizin yazdığı yazılım büyük olasılıkla yıllarca çalışacak bu, birkaç ay önce yazdığı koddan utanmış olan herkes için özellikle korkutucu bir düşünce.

Sürdürülebilir kod asla nihai durumunda değildir. “Canlıdır!” (Umarız Frankenstein’ın canavarından daha iyi durumdadır.) ABD Anayasası gibi, metaforik olarak yaşayan, nefes alan bir belgedir özen ve öngörü gerektirir.
Kodu Test Etmek

Bir yazılımın test edilebilir olması için modüler hale getirilip küçük bileşenler ve fonksiyonlara ayrılması gerekir. Eğer x’in y yapması bekleniyorsa, x’in gerçekten y yaptığına emin olmak için bir test yazabilirsiniz.

Eski kod tabanları (bazen “brownfield” olarak adlandırılır) genellikle test içermez ya da testler yetersizdir. Bu eski sistemleri sürdürmenin zorluklarından biri, test yazmak isteseniz bile kodun kolayca buna izin verecek şekilde tasarlanmamış olmasıdır. Eğer durum buysa, sistemi baştan yazmanız gerekmez. Onu eski bir araba gibi düşünün: Çalışan parçaları kaldırmayın. Bir şey bozulduğunda, o kısmı düzeltin ve çözümün sağlam olduğunu garanti altına almak için bir test ekleyin.
Kodu Hata Ayıklama

Debugger’lar, kodda neler olduğunu (neredeyse) gerçek zamanlı olarak görmenin anahtarıdır. Bildiğiniz gibi, hata ayıklama araçları seçtiğiniz belirli bir noktada programınızı durdurur, bu da varsayımlarınızı kontrol etmenize ve programın ne yaptığını anlamanıza olanak tanır. Beklenmeyen sonuçları ortaya çıkarmak ve beklediğinizden farklı olanı görmek için harika bir yöntemdir. Örneğin, bir değişkenin değeri beklenmedik şekilde değişmiş olabilir veya yanlış türde bir parametre kazara girilmiş olabilir.

Çoğu IDE (entegre geliştirme ortamı) ve tarayıcı, kutudan çıktığı haliyle hata ayıklama araçlarına sahiptir. Hata ayıklayıcılar, hata olmadığında bile özellikle daha az deneyimli mühendisler için son derece faydalıdır. Programı “adım adım” ilerletmenize izin verir, böylece kodu bir makine gibi düşünmeye başlarsınız ve kod okuma beceriniz gelişir.
Kodu Günlükleme

Günlükleme, bir geliştiricinin en değerli aracı ya da en büyük kabusu olabilir. Hata ayıklama araçları işe yaramaz hale geldiğinde, günlükleme cevaplar sağlar. Kodunuzu her zaman çalışma anında satır satır inceleyemezsiniz. Bunun yerine kodunuz bulutta dağıtılmış veya yayında olabilir.

Günlükleme, hata ayıklama gibidir ancak koda kesme noktası (breakpoint) eklemek yerine, program çalışırken gözden geçirebileceğiniz ifadeler eklenir. Bu ifadeler, programın hangi eylemleri ve durumları gerçekleştirdiğini gösterir.

Logging framework’ler, günlük mesajlarını sınıflandıran ve günlüklerin arasından daha hızlı bilgi almanıza yardımcı olan araçlardır. Günlükleme ücretsiz değildir; günlükleri bir yerde saklamanız gerekir, bu nedenle yalnızca ihtiyacınız olan verileri günlüğe kaydedin. Her şeyi kaydetmek kaynak israfı ve bilgi yüklemesine yol açar.

Ne kaydedeceğiniz, ne sıklıkla kaydedeceğiniz ve nasıl organize edeceğiniz tamamen size ve uygulamanıza bağlıdır. İşte uygulamanızı önerdiğim üç kılavuz:

  Günlük mesajlarınızı biçimlendirin. Oturum kimliği veya kullanıcı hesabı bilgileri gibi ilgili bilgileri ve zaman damgasını ekleyin.
  Bağlam sağlayın. Bazen yalnızca anlık veriden fazlasına ihtiyacınız olur. Bir şeyin yanlış gittiğini bilmek yeterli değildir. Bir hata meydana gelmeden önce ne oldu? Hangi veri etkilendi?
  Kodu Günlükleme

Günlükleme, bir geliştiricinin en değerli aracı ya da en büyük kabusu olabilir. Hata ayıklama araçları işe yaramaz hale geldiğinde, günlükleme cevaplar sağlar. Kodunuzu her zaman çalışma anında satır satır inceleyemezsiniz. Bunun yerine kodunuz bulutta dağıtılmış veya yayında olabilir.

Günlükleme, hata ayıklama gibidir ancak koda kesme noktası (breakpoint) eklemek yerine, program çalışırken gözden geçirebileceğiniz ifadeler eklenir. Bu ifadeler, programın hangi eylemleri ve durumları gerçekleştirdiğini gösterir.

Logging framework’ler, günlük mesajlarını sınıflandıran ve günlüklerin arasından daha hızlı bilgi almanıza yardımcı olan araçlardır. Günlükleme ücretsiz değildir; günlükleri bir yerde saklamanız gerekir, bu nedenle yalnızca ihtiyacınız olan verileri günlüğe kaydedin. Her şeyi kaydetmek kaynak israfı ve bilgi yüklemesine yol açar.

Ne kaydedeceğiniz, ne sıklıkla kaydedeceğiniz ve nasıl organize edeceğiniz tamamen size ve uygulamanıza bağlıdır. İşte uygulamanızı önerdiğim üç kılavuz:

  Günlük mesajlarınızı biçimlendirin. Oturum kimliği veya kullanıcı hesabı bilgileri gibi ilgili bilgileri ve zaman damgasını ekleyin.
  Bağlam sağlayın. Bazen yalnızca anlık veriden fazlasına ihtiyacınız olur. Bir şeyin yanlış gittiğini bilmek yeterli değildir. Bir hata meydana gelmeden önce ne oldu? Hangi veri etkilendi?
  Yan etkilerden kaçının. Günlük kayıtlarınız (loglarınız) uygulamanızın performansını etkilememelidir. Her şeyi günlüklemek cazip gelebilir, ancak bunun bir maliyeti vardır. Bunun yerine yavaş başlayın. Bir kez kurulduktan sonra günlüklemeyi kaldırmaktansa başta dikkatli olmak çok daha iyidir.

Değiştirilemez Kod Yazmak

Temel olarak, tüm değişkenler bir kez atanır ve daha sonra değişmez. Eğer iş parçacığı (threading) bir endişeyse, değiştirilemezlik daha dayanıklı bir kod üretir. Ayrıca yazılım daha kolay hata ayıklanabilir hale gelir çünkü değişkenler programın ortasında değişmez. Bunun yerine, yeni bir değer yeni bir değişkene atanır. Kodunuza ne kadar az hareketli parça yerleştirirseniz, hata ayıklamak ve sürdürmek o kadar kolay olur.
Okunabilir Kod Yazmak

Uygulamanızın kodu, üzerinde çalıştığı makineler tarafından okunabilir olmalıdır. Ama bu makineler kodu sürdürmez. Bunun yerine insanlar kodu okumalı, anlamalı, değişiklik yapmalı ve bir kara deliğe neden olmamalıdır.

Kod yazarken, sadece iş arkadaşlarınızı değil, gelecekteki “kendinizi” de düşünmelisiniz. Altı ay sonra bir dizide neyin saklandığını anlamaya çalışırken elinizde o bağlam olmayacak.

Ayrıca, kodunuz ne kadar okunaklı olursa, insanların değişiklik yapması ve hataları düzeltmesi de o kadar kolay olur. Bazen kodu birkaç satırla "şık" hale getirmek eğlenceli olabilir. Ama biri kodunuzun ne yaptığını anlamak için saatler harcamak zorunda kalıyorsa, bakım maliyeti çok yüksektir.
Programlama Kalıpları

Bu bölümde yalnızca iki tanesini ele aldığım halde, pek çok programlama paradigması mevcuttur. Bu iki paradigma nesne yönelimli programlama (OOP) ve fonksiyonel programlamadır. Her ikisi de aynı hedefe giden farklı yollar sunar: yazılım mantığını son kullanıcıya fayda sağlayacak şekilde organize etmek. Ben OOP ve fonksiyonel programlamayı tercih ediyorum çünkü ikisi de popüler ve karşılaştırmalı özellikleri sayesinde size daha geniş bir yaklaşım yelpazesi sunuyor.
Nesne Yönelimli Programlama

Nesne yönelimli programlama (OOP) tamamen nesneler üzerine kuruludur tahmin ettiniz. Nesneler her şey olabilir, ama genellikle veri barındırırlar. Nesneler özellikler veya nitelikler içerebilir. OOP'de insanlar genellikle prosedürlere fonksiyon ya da metot der.

Çoğu nesne yönelimli programlama dili Java, C++, Python, JavaScript, Ruby ve Scala sınıf tabanlıdır. Nesneler sınıfların örnekleridir.

Nesne yönelimli geliştirmenin hedefleri yeniden kullanılabilirlik ve modülerliktir. Bir OOP uygulamasında geliştirilmiş mantık ve ilişkili metodları küçük tutmak idealdir. Bu, verimliliği artırır ve zaten yapılmış çalışmaları yeniden kullanmanızı sağlar. Bu özellik güçlüdür ancak, geliştirici metodun içsel olarak sezgisel ve esnek biçimde yeniden kullanılabilir olmasını sağlamazsa, sorunlara yol açabilir.

OOP programları mantığı kapsülleyerek nesnenin kullanılabilmesi için iç detaylarını bilmenize gerek kalmaz. Nesneler, geliştiricilerden belirli nitelikleri gizleyebilir; böylece kimse onları değiştirmez. Bu yaklaşım, büyük programların sürdürülme yükünü azaltan tasarım faydaları sağlar çünkü nispeten kolayca değiştirilebilir.
Fonksiyonel Programlama

Fonksiyonel programlama, durumu (state) değiştirmekten kaçınır ve verilerin değiştirilemezliğini vurgular. Bir fonksiyonun çıktısı sadece ona verilen argümanlara bağlıdır. Bu yaklaşımın yan etkisi yoktur. Aynı parametrelerle bir fonksiyonu bin kez çalıştırırsanız, her zaman aynı sonucu üretir. Yerel ya da global durum bu fonksiyonları etkilemez, bu yüzden yan etkilerden kaçınılır.

Fonksiyonel programlama son derece modülerdir ve test etmesi kolaydır. Uygulamada bu yaklaşım, mühendislerin OOP ile mümkün olandan daha temiz kod yazmasına olanak tanır. Yan etkilerden kaçınma ve değiştirilemez veri kullanımı ilkeleri kodun sade ve okunabilir şekilde yazılmasına yol açar. Ayrıca kod daha az hareketli parçaya sahip olduğundan hata ayıklamak daha kolay hale gelir.

Fonksiyonel programlama lambda calculus’tan doğmuştur, ama fonksiyonel programlama yazmak için matematik dehası olmanıza gerek yok. Bu uygulamalardan faydalanmak için Lisp, Haskell, Scala, Erlang, Rust ve Elm gibi dillerde yazabilirsiniz.
Bir Dil Seçmek

Herhangi bir proje için doğru dili seçmek zor bir karardır. Sayısız seçeneğiniz vardır ve her birinin artıları ve eksileri bulunur. Zor olan bir diğer şey de: Gerçek değeri olan şeylerle pazarlama abartılarını ayırt edebilmektir.

Hiçbir tek programlama dili diğerlerinden üstün değildir; belirli bir topluluğun savunucuları ne derse desin, her birinin avantajları ve dezavantajları vardır. Her dil, yapılacak işe göre farklı ödünleşmeler (trade-off) sunar.

Her dilin potansiyel avantajlarını (ve maliyetlerini) sıralamam mümkün değil, ama işte takımınız için göz önünde bulundurmanız gereken bazı yönler:

Performans: Dil, ihtiyaç duyduğunuz şekilde performans gösterecek mi? Bir dilin performansı hakkında fikir veren karşılaştırmalar (benchmark) mevcuttur; ancak kodun kalitesi de performansı doğrudan etkiler. İyi yazılmış bir Ruby uygulaması, zayıf yazılmış bir Java uygulamasından her zaman daha iyi performans gösterir, dilin benchmark sonuçları ne olursa olsun.

Konfor: Ekip dili zaten biliyor mu, yoksa hızlıca öğrenebilecek mi?

Topluluk: Çevrimiçi yanıtlar ve topluluk kaynakları bulmak kolay mı?

Platform: Dil özel bir makine ya da araç gerektiriyor mu? Örneğin, Java ile geliştirilen programlar yalnızca Java Sanal Makinesi (JVM) bulunan sistemlerde çalıştırılabilir.

Çerçeve (Framework): Bazı diller belirli framework’lerle sıkı şekilde bağlantılıdır. Ruby başlı başına güçlü bir dilken, hafif framework’ler (örneğin Sinatra) mevcut olsa da Rails, Ruby ile oldukça iç içe geçmiştir. Bunun geliştirme sürecinize etkilerini önceden düşünün.

Eğer mikroservis mimarisi tercih ediyorsanız ve yeterince büyük bir ekibiniz varsa, uygulamanızı birden çok dil kullanarak geliştirebilirsiniz. Her servis, başka bir dilde yazılmış servislerle standart bir protokol veya API üzerinden etkileşimde bulunabilir.
Anti-Kalıplardan Kaçınmak

Anti-kalıplar, yazılım geliştirmede kötü uygulamaları tanımlar. Genellikle başlangıçta mantıklı görünen bu davranışlar, sektörde sık karşılaşılan ama verimsiz yöntemlerdir. Sonuçları ciddi olabilir. Daha etkili çözümler çoğu zaman mevcuttur. Aşağıdaki liste, DevOps pratiğinizde kaçınmanız gereken bazı yazılım mühendisliği anti-kalıplarıdır:

Komite ile tasarım: DevOps’un iş birliği ve iletişime yaptığı vurgu nedeniyle, bazı kişiler bunu tasarımı komiteye bırakmak gibi yorumlayabilir. Yazılım geliştirme böyle bir şey değildir. Bu tür karar alma süreçleri genellikle felaketle sonuçlanır. Bunun yerine, bireylerin süreçten geçerek fikirlerini oluşturmuş şekilde masaya gelmesi gerekir. Aksi hâlde, hiç düşünülmeden bir araya gelinip karar alınmaya çalışılır ve sonuçlar kaotik olur.

Tanrı nesneleri: Bu anti-kalıp, çok fazla mantığın tek bir nesneye yüklenmesiyle ortaya çıkar. Bu “her şeye gücü yeten” nesne, diğer nesnelerin ona bağımlı olmasına neden olur. Kod fazla sıkı bağlı hale gelir ve bu nesne o kadar büyür ki bakım yapmak zorlaşır.

Kargo kültü: Bu terim, belirli bir desenin ya da aracın neden kullanıldığını tam anlamadan, sadece bir başkası kullanıyor diye aynısını uygulamak anlamına gelir. Genellikle deneyimsiz geliştiricilerde görülse de, belirsiz araçlardan veya sıkı teslim tarihlerinden dolayı kıdemli mühendislerde bile görülebilir.

Çekiç kanunu: Eğer mühendisler bir dil, framework veya araca aşırı derecede bağlıysa, bu anti-kalıptan muzdarip olabilirler. Araçlarını kullanmakta rahat olmaları iyi olsa da, bu rahatlık tembelliğe dönüşüyorsa, doğru araçları kullanıp kullanmadığınızı tekrar gözden geçirme zamanı gelmiştir.

Kanayan uç (Bleeding edge): Bu terim, mühendislerin henüz tam olgunlaşmamış ama yeni çıkan teknolojilere hemen yönelip bunları projelerine entegre etmeleri anlamına gelir. Bu teknolojiler heyecan verici olabilir, ancak çoğunlukla kararsız, belgelenmemiş ve hatalıdır. Ayrıca, henüz tam piyasaya çıkmadan önce yön değiştirme potansiyeli yüksek olan araçları kullanmak risklidir.

Aşırı mühendislik (Overengineering): Bir ürün tasarlarken yalnızca gerekli sorunu çözmeye ve bunu verimli şekilde yapmaya odaklanmalısınız. Gereksiz karmaşıklık eklemek aşırı mühendisliktir. Bu durum, hayatların riske girdiği güvenlik sistemleri dışında çoğu projede kaçınılması gereken bir durumdur. Sade tutun.

Spagetti kod: Bu terim, yapısız ve zar zor okunabilir kodları tanımlar. Kod çalışabilir ama sanki tabakta dolaşan spagetti gibidir; çözülmesi zordur.

Kopyala-yapıştır (Copypasta): Bu anti-kalıp, var olan bir kodun ya da internetten bulunan kod parçalarının olduğu gibi uygulamaya yapıştırılmasıdır. Bunun yerine, parametre alabilen ve yeniden kullanılabilir çözümler oluşturun.

Erken optimizasyon: Mühendisler, her şeyi baştan itibaren mümkün olduğunca verimli hale getirme eğiliminde olabilir. Ancak erken optimizasyon genellikle kaynakların en verimli kullanımı değildir ve kodun sürdürülebilirliğini zorlaştırabilir özellikle de sorunu gerçekten çözdüğünüzden emin değilseniz. MVP’ler (Minimum Viable Product) asla erken optimize edilmemelidir, optimizasyonlar yalnızca gerekli olduğu net bir şekilde belirlendikten sonra yapılmalıdır.

Tedarikçiye kilitlenme (vendor lock-in): Bu konuya kitap boyunca birkaç kez değiniyorum. Bir sağlayıcıya bağımlı kalmak, yeni ve belki de daha iyi bir araca geçişte engel oluşturan yüksek maliyetler doğurabilir.
Bakımı Kolay Kod Yazmak: Spagetti Canavarı ve Temiz Kod Kahramanı

Farz edin ki altı ay önce yazdığınız koda yeniden bakıyorsunuz. Sanki o satırları uzaylılar yazmış! Yorum deseniz yok, değişken isimleri a, b, c diye gidiyor, fonksiyon 500 satır... Tanıdık geldi mi? Yalnız değilsiniz. Zaman zaman hepimiz "Kodumu ben bile anlamıyorum" noktasına geliyoruz Geçmişteki benliğimize kızıp "Yazarken mantıklıydı ama şimdi hiçbir şey anlamıyorum" diye yakınan iç sesimizle karşılaştığımız anlar oluyor doğrusu.

Kod kalitesini korumak, gelecekteki siz (veya ekip arkadaşlarınız) için bir iyiliktir. Ama kabul edelim, bazen hızlı çözüm üretme telaşıyla kodu biraz dağıtabiliyoruz. Proje öyle bir hale gelir ki kod tabanı adeta bir spagetti yumağına döner. Başını tutsanız sonu gelmez, bir yeri düzeltirsiniz başka yerden hata fırlar. Yine de içimizden bir ses "Kodum spagetti ama en azından pişmiş!" diye bizi teselli eder. Yani kod karmakarışık olabilir ama çalışıyorsa sorun yok (muş) gibi davranırız. 🙈

Tabii bu tavır teknik borcu büyütür, ileride ödeyeceğimiz faturanın faizini artırır. Ertelenen refaktöringler, “nasılsa sonra toparlarız” diye yazılan geçici çözümler kalıcı hale gelir. Bir gün gelir, o “geçici” çözüm yüzünden sistemi kimse güncelleyemez olur. Temiz ve bakımı kolay kod yazmak işte bu yüzden kritiktir. Anlamlı değişken isimleri, kısa ve öz fonksiyonlar, bolca yorum ve dokümantasyon... Bunlar geleceğe bırakılan hazinelerdir. Unutmayalım, bir satır kod bile dünyayı değiştirebilir ya da çökertebilir. Büyük güç büyük sorumluluk getirir; o nedenle kodumuza özen göstermek, sonraki kahramanlık hikâyelerimizi belirler.
Temiz Kod Yazmak

Temiz kod insanlar tarafından okunabilir ve test edilmesi kolay olandır. Her bir fonksiyon (ya da bazı dillerde metot), yalnızca tek bir şey yapmalıdır. Bu “tek sorumluluk” ilkesi, kodu daha modüler hale getirir, böylece ne yaptığı hızlıca anlaşılır ve hata ayıklamak kolaylaşır.

Odak noktası eksik olan fonksiyonlar, kodun okunmasını zorlaştırır ve bir bölümün amacını anlamayı karmaşık hale getirir. Aynı zamanda bu odak eksikliği, soyutlanmış veya tekrar kullanılan genel metotların anlaşılmasını da güçleştirir. Fonksiyonların ne yaptığını anlatacak şekilde adlandırıldığından emin olun. Eğer bir fonksiyon adını yazarken “ve” (“and”) kelimesini eklemek istiyorsanız, bu büyük ihtimalle tek sorumluluk ilkesini ihlal ettiğinizin göstergesidir.
İşi Anlamak

Bu bölümde daha önce bahsetmediğim bir anti-pattern, “mantar yönetimi”dir. Bu, geliştiricilere çok az bilgi verilerek geliştirme yapmaları beklendiği bir durumu tanımlar. Yönetim kararlarına göre ürün geliştirilen bu modelin ismi, mantarların karanlıkta tutulup arada sırada gübrelenmesinden gelir. Bu ortamda neden-sonuç ilişkisi kurmak mümkün değildir, çünkü geliştiricilerle yöneticiler arasında iletişim eksiktir.

Eğer geliştiriciler işi tam olarak anlamazsa, kodu doğru amaca hizmet edecek şekilde yazamazlar. Öte yandan işi anlayan geliştiriciler, alternatifler önerebilir, fikirleri sorgulayabilir ve çalışmalarından gurur duyarlar.
Başkilerini Dinlemek

İş ve mühendislik dünyasında dinleme sanatı belki de en az değer verilen beceridir özellikle de geliştiriciler için. Verimli ekipleri izlerseniz, kıdemli mühendislerin genelde en az konuşan kişiler olduğunu görürsünüz. En iyi mühendislik liderleri, herkesin fikirlerini paylaşmasına izin verir, her şeyi dikkatlice düşünür ve ardından ekibin planı nasıl uygulaması gerektiğine dair net yönlendirmeler sağlar.

İşe alırken aradığım önemli bir özellik, birinin neyi bilmediğini kabul etme rahatlığıdır. Kendini odadaki en zeki kişi sanan mühendisler iş birliğini yok eder. Bu kişiler ekip arkadaşlarını susturur ve farklı fikirlere karşı duvar örer. Böyle bir kişinin ekibe maliyeti çok yüksektir. Hatalı olduklarında bunu kabul edemeyen kişiler yerine, başkalarının fikirlerini dinleyen mühendisler tercih edilmelidir.
Doğru Şeylere Odaklanmak

Ben neredeyse hiç “coder” (kodcu) kelimesini kullanmam çünkü bu kelime, düşünmeden sadece kod yazan biri anlamını çağrıştırır. Disiplinli olup, işin farklı alanlarından gelen geri bildirimleri dikkate alabilen geliştiriciler, iş için en değerli becerileri taşır. Bu beceriler, teknik dili başkalarının da anlayabileceği şekilde ifade etme yetisi gerektirir.

Doğru şeylere odaklanan geliştiriciler, teslim tarihleri uğruna kaliteden taviz vermezler. Aksine, sorunları erken bildirir ve herkesin teslim tarihleri konusundaki beklentisini hizalarlar (özellikle de ne zaman teslim edilmesi gerektiği konusunda).

Bu tür mühendisler, teknik borçları hafife almaz ama hızlı bir şekilde çözmeyi de bilir. İşe yarayan, değişime açık ve sürdürülebilir mimari ve özellikler üzerinde çalışırlar. Kodu sade tutar, aşırı karmaşıklıktan kaçınır ve yeniden tasarım gerektirecek tuzaklardan uzak dururlar.
Rahatsızlıkla Rahat Olmak

Merak, tüm harika geliştiricilerin ortak özelliğidir. Yeni şeylerden korkmazlar ve yeni fikirleri çocukça bir neşeyle karşılarlar. Harika geliştiriciler, yeni endüstri araçlarının veya trendlerin her zaman her şirket için en iyi fikir olmayabileceğini bilirler, ancak teknolojik gelişmeleri takip eder, yeni araçların temellerini öğrenir ve böylece doğru kararlar verebilirler.

Sürekli eğitim, harika yazılımlar üreten ekiplerin bir diğer temel unsurudur. Okumanın, diğer geliştiricilerle konuşmanın, konferanslara katılmanın ve kurslara gitmenin önemini vurgularlar. Bir yöneticiyseniz, geliştiricilerinizi desteklemeli ve sürekli eğitim için bütçe ayırmalısınız. Geliştiricileriniz yalnızca kod yazan kişilerden ibaret değildir. Uygun şekilde yetiştirildiklerinde, şirketinize yıllarca değerli tavsiye ve rehberlik sağlayabilecek bilgi kaynaklarıdırlar.

Mühendislerinize eğitim fırsatları sağlamanın yanı sıra, onlara gelişim için odaklanabilecekleri sessiz zamanlar da tanıyın. Tanıdığım bir mühendislik yöneticisi, toplantıların yalnızca Pazartesi ve Cuma günleri yapılmasına izin veriyor. Toplantıları haftaya yaymak yerine, geliştiricilerin odaklı çalışma sürelerini kesintiye uğratmadan koruyor. Yazılım geliştirmek yoğun dikkat gerektirir. Odaklanmada yaşanan tek bir kesinti, bir geliştiricinin saatlerce verimini düşürebilir.
Sağlam Uygulamalar Yerleştirmek

Artık ne yapmamanız gerektiğini bildiğinize göre, organizasyonunuzda iyi uygulamaları nasıl hayata geçireceğinize odaklanabilirsiniz. Ve hayır, “en iyi uygulamalar” demedim. Bir iyi uygulama, endüstride diğer tekniklerden daha iyi sonuçlar verdiği kanıtlandığı için üstün görülen bir yaklaşımdır. Diğer bir deyişle, yaygın olarak kabul edilen uygulama şeklidir.

💡 İpucu: “En iyi uygulamalar” yaklaşımını sevmiyorum çünkü bu yaklaşım yeniliği boğar. Bir şeyi “en iyisi” olarak kabul ederseniz, onu sorgular ya da geliştirir misiniz? Öte yandan, iyi uygulamalar, belirli zorluklara yaklaşımda sektörde yaygın olarak kabul görmüş ve test edilmiş standart yöntemlerdir. Katı kurallar dayatmadan size rehberlik sunarlar.
Kaynak Kodunuzu Düzenlemek

Ekibinizdeki her mühendisin, en azından yalnızca-okuma erişimiyle, organizasyondaki tüm kod satırlarına erişimi olmalıdır. Bu erişim, uygulamanızın hem özellik kodlarını hem de altyapı kodlarını kapsamalıdır. Bu paylaşılan depo (ya da muhtemelen birden fazla depo), herkesin aşina olmadığı uygulama bölümlerini incelemesini sağlar. Bu sayede her mühendis yalnızca günlük işlerde değil, özellikle kesintiler ve acil durumlarda da faydalı olabilir.

Çoğu organizasyon için, Git ve bir GitHub veya GitLab gibi barındırma hizmeti idealdir. Bu araçlar, eski kaynak kontrol araçlarına göre çok daha hafif yapılıdır ve toplantı gündemleri ve fikir alışverişi için harika iş birliği araçlarıdır.

Kodunuzu tekrar edilebilir ve sade tutun. Derlemeler (builds) basit ve tekrar edilebilir olmalı. Ayrıca ilerledikçe sürekli entegrasyona doğru geçiş için otomasyonlarınızı başlatın.
Test Yazmak

Henüz bir test altyapınız yoksa, şimdi kurmanın zamanı. Geliştiricilere yazarken otomatik test yazma alışkanlığı kazandırmak çok önemlidir. Bazı kişiler test odaklı geliştirme (TDD) yaklaşımını benimser: önce gerekli fonksiyon için test yazılır, ardından bu testi geçecek şekilde kod yazılır. Bu yaklaşım etkilidir ama ağır gelebileceği için birçok kişi tarafından tercih edilmez. En azından, geliştiriciler yazdıkları mantığın beklendiği gibi çalıştığını doğrulayan birim testleri yazmalıdır.

“Happy path” testleri, her şeyin beklendiği gibi gittiği senaryolardır. “Sad path” testleri ise hataların ortaya çıktığı senaryoları kapsar.

Kullanacağınız test framework’ü, dilinize bağlı olacaktır. Organizasyonunuzun ihtiyaçlarını karşılayacak kadar güçlü ama öğrenilmesi ve uygulanması kolay bir framework seçin. Test yazmak zorsa, geliştiriciler yazmaz. Belkide Copilot ile tanışma zamanı gelmiştir ;) 
Özellikleri Belgelemek

Bir kod parçası üzerine notlar almak, gelecekteki geliştiricilere o fonksiyonun ne yaptığı (eğer karmaşıksa), kodun bağlamının ne olduğu, hangi parametreleri beklediği ya da ürettiği ve zamanla nasıl iyileştirilebileceği hakkında fikir verir. (Hey, bazen işleri aceleyle yapmak zorunda kalıyoruz.)

Kodun kendisi temiz ve okunabilir olmalı; böylece yazılı olmasa da bir tür dokümantasyon işlevi görebilir. Kod bir makine dilinde yazılmış olsa bile, yine de bir belge niteliğinde olabilir. Tıpkı DevOps’un diğer her şeyinde olduğu gibi, belgeleri de bir yere kadar otomatikleştirebilirsiniz. Ancak önce sorunlarınızı manuel olarak çözmeyi unutmayın; aksi hâlde bozuk sistemleri otomatikleştirmiş olursunuz. Eğer belgeleri otomatikleştirecekseniz, bir çerçeve (framework) oluşturun ve geliştiricilere belgeleri özelleştirebilmeleri için özel değerler atamalarına izin verin.

API yazarken, genellikle GET, POST, PATCH, DELETE gibi işlemler için temel API şablonlarını içeren bir betik (script) hazırlarım. Böylece her seferinde aynı belgeleri yazmak zorunda kalmam. Hem zaman kazanırım hem de hata yapma ihtimalimi azaltırım. Şablonu yazdıktan sonra belirli koda göre düzenlerim. Bu tür küçük tekrar eden işleri otomatikleştirmek tam bir DevOps zihniyetidir!

Bir diğer belge türü ise dış müşterilere yönelik olanlardır. Bu belgeler genellikle geliştiriciler tarafından değil, daha teknik ve açıklayıcı yazım gerektiren uzmanlar tarafından yazılır. Geliştirici ilişkileri alanında çalışan biri olarak, ürün mühendislik takımlarının oluşturduğu API’leri tanıtmak, anlaşılır ve herkesin kullanabileceği belgelerle sunmak da işimin bir parçası.
Kodunuzu Gözden Geçirmesi

Kod incelemelerine güçlü bir şekilde inanıyorum. Geliştiricilerin kendi kodlarını master (ana) branch'e kendilerinin birleştirmemesi gerektiğine de inanıyorum. Kod incelemesi, kodun bulunduğu havuzda yorumlarla yapılabilir ya da yüz yüze, iki (veya daha fazla) mühendis bir araya gelerek ekranda birlikte yapılabilir.

Kod incelemesi birçok açıdan önemlidir çünkü:

Genç mühendislerin daha hızlı gelişmesine yardımcı olur 

Hataları azaltır çünkü birden fazla göz tarafından kontrol edilir 

Kod tabanını formatlama açısından standartlaştırır 

İnceleyen mühendisin varsayımları sorgulamasını sağlar 

İnsanların yazmadıkları kodları tanımasına yardımcı olur 

Kıdemli mühendislerin, daha az deneyimli mühendislerin nasıl düşündüğünü anlamasını sağlar

Kod inceleme süreci basittir. Git kullandığınızı varsayarsak, kodunuz bir feature (özellik) branch’inde gelişir. Kod tamamlandığında bir pull request (PR) gönderirsiniz. Bu PR, kodu master, trunk ya da ana dal olarak tanımlanan branch’e birleştirmek içindir. (Kullandığınız dağıtım modeline göre master branch, prod'da çalışan versiyon olmayabilir, ama genellikle en güncel koddur.)

GitHub gibi platformlarda birini PR’a dahil etmek için yorum kısmına @username yazmanız yeterlidir. Bu şekilde ilgili kişiye bildirim gönderilir. Bazı şirketler kimin neyi gözden geçireceğini önceden atar, bazıları ise daha gevşek bir süreç izler.

Eğer sizin veya ekibinizin zamanı kısıtlıysa, hafif bir kod incelemesinden bile fayda görürsünüz. İki mühendis kısa süreliğine bir araya gelip kodu tartışır ve göz gezdirir. Yine de hatalar bulunacaktır.

Eğer inceleme uzaktan veya eş zamansız yapılacaksa, gözden geçiren kişi kodu inceleyip PR’a yorumlarını bırakır. İncelemeyi yüz yüze (veya video görüşmesiyle) yapıyorsanız, kodu gözden geçirmek için sessiz bir ortam bulun. Geniş ekranlı bir monitör kullanmak, okuma ve yorumlamayı kolaylaştırır.
DevOps Kararları: Kaos Yönetimi

Yazılım sadece kod yazmaktan ibaret değil; işin bir de DevOps tarafı var ki orası tam bir macera! Sunucular, dağıtık sistemler, pipeline'lar... Doğru kararlar alınmazsa, geliştirme ortamı tam bir kaosa dönebilir. Bu bölümde, DevOps dünyasındaki karar anlarının komediyle karışık gerçeklerine bakalım.

Öncelikle, 

  asla Cuma akşamı deploy yapma 

kuralını duymuşsunuzdur. Duymayanlar için özet: Hafta sonu tatilini telefonda geçirilen acil durumlarla bölmek istemiyorsanız, üretim ortamına kod göndermek için Pazartesi sabahını bekleyin. 🙂 Ama gelin görün ki bazen müşteri ısrar eder, yönetici göz ucuyla bakar, ekip "hadi bir cesaret" der... Ve tabii ki Cuma akşamı deploy yapılır. Sonra? Sonrası malum: herkes Slack'te kırmızı alarm emojileriyle "Production patladı, kim bastı?" sorgusu. İşte o an yaşanan panik hem trajik hem komiktir.

Bir de iç sesimiz var tabii. Bazen daha kodu sunucuya yollarken içinize doğar, "sanki bir terslik olacak" dersiniz. Hani şu "İçimde kötü bir his var, push etmeyeyim bugün" diyenler yok mu, genelde haklı çıkarlar. Keşke her zaman o sese kulak verebilsek! Yine de gerçek hayatta bazen o sese rağmen düğmeye basarız. Kimileri ise işi iyice gizemli hale getirir, örneğin gece yarısı kimseye çaktırmadan iş yapanlar da yok değil: "Production’a deploy ettim ama kimseye söyleme" diye mesaj atan cesur (!) ekip arkadaşından bahsediyor. Böyle bir mesaj aldığınızda kalp atışlarınız hızlanır, adrenalin tavan yapar; sabaha kadar sistemi izlemek farz olur.

DevOps kararları sadece zamanlamayla bitmiyor, teknoloji seçimleri de ayrı bir muamma. Mesela bir ara herkes “Docker her şeyin cevabıdır” diye atladı. Ardından "Kubernetes olmadan ölçeklenemez" furyası başladı. Tabii bunları duyup da hemen proje altyapısını değiştiren ekipler çokça ter döktü. Mikroservis mimarisi kulağa havalı gelir, ama hazırlıksız girerseniz elinizde 50 tane minik servis ve kocaman bir baş ağrısı kalır. Monolitik uygulamanızı parçalayıp sonra parçaları birleştirmek için uğraşırsınız, adına da esprili bir şekilde "dağıtık monolit" denir. Yani her trendi uygulamadan önce iki kez düşünmek lazım; yoksa DevOps kararınız bir fıkraya dönüşebilir.

Peki ya CI/CD pipeline? Otomasyonu hayatımıza sokarak bizi manüel işkenceden kurtaran o harika araçlar... Taa ki bir şeyler bozulana dek. Pipeline aniden kırmızıya döner ve herkes birbirine bakar: "Kim yaptı?" Cevap genelde malum: "CI/CD pipeline çökmüş ama ben değilim." Diyen çok, sorumluluk alan yok. Yine de birileri o sorunu sabaha kadar düzeltir, biz de ertesi gün hiçbir şey olmamış gibi devam ederiz. İşte DevOps dünyasının kahramanları da böyle doğar: kimliği belirsiz bir şekilde sistemi kurtaran gizli ninja gibi. 🥷

Özetle, DevOps kararlarında risk ve ödül hep bir aradadır. Doğru planlama, test ortamları, geri dönüş planları iyi pratikler olarak dursa da, itiraf edelim bazen şansa da güveniyoruz. (Siz siz olun, şansa fazla güvenmeyin, yedeğiniz olsun. Yoksa haftasonu uykunuz kaçar, bizden söylemesi.)

Yazılım geliştirmenin gerçekleri bazen acı, bazen tatlı; çoğu zaman da kahkahası bol. İyi bir ekip, bu zorlukları birlikte göğüslerken eğlenmeyi de bilen ekiptir. Pull request'te yaşanan komik bir diyalog, sabaha kadar süren debug seansında paylaşılan pizzalar, 

  "kim yaptı bunu" 

diye başlayıp kahkahalarla biten toplantılar... Bunlar yazılım dünyasının hem stres azaltma yöntemi hem de ekip ruhunu pekiştiren anılarıdır.

Sevgili junior geliştiriciler ve bu işe yeni adım atan taze mezunlar, tüm bu hikayeler gözünüzü korkutmasın. Her birimiz bu yollardan geçtik, hatalar yaptık, güldük, öğrenmeye devam ettik. Sürdürülebilir kod yazmak bir gecede kazanılan bir yetenek değil; pratikle, deneme-yanılmayla ve bazen de tatlı hatalarla gelişiyor. Önemli olan, hatalardan ders alırken mizah duygumuzu kaybetmemek.

Sonuç olarak, yazılım dünyasında iletişim sadece toplantı odasında değil kod satırlarında da gerçekleşir; bakımı kolay kod geleceğe atılan bir imzadır; doğru DevOps kararları kaosu önler (ya da yönetilebilir düzeye indirir); ve iyi pratikler, arada tökezlesek de, yolumuzu aydınlatan işaret fişekleridir. Tüm bunları yaparken eğlenmeyi de ihmal etmeyelim. Çünkü günün sonunda, bir deploy sonrası monitöre bakıp her şeyin çalıştığını görmek kadar güzel bir duygu varsa, o da bunu ekipçe kahkahalar eşliğinde kutlamaktır. 
