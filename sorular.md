# Araştırma Soruları

Artık yeni iş yerindeki ilk görevini gerçekleştirmek için hazırsın! Kullandığımız araçları biraz daha iyi anlama zamanı. Yapman istenilen şey, bu dokümanı güncelleyerek, aşağıdaki soruları soruları cevaplaman. Böylece Git yapısına biraz daha aşina olmaya başlayacaksın.

Soruları cevaplarken takıldığın yerlerde [GitHub docs](https://docs.github.com/en)'u kullanabilirsin. Docs, (ingilizce documentation'ın kısaltılmış halidir) bir programı veya dilin nasıl kullanılacağını anlatan dokümandır. Yazılım dünyasında sıkça kullanılır. Bir yazılımcı olarak _zamanınızın büyük çoğunluğu da bu tarz dokümanları okumakla ve üzerinde çalışmakla geçecek_.

![READ THE DOCS](https://github.com/Workintech/FSWeb-S1G1-Projesi-Web-Development-Projesi-icin-Git/blob/main/read-the-docs-wit.gif?raw=true)

Eğer aradığın soruların cevapları GitHub docs'ta yoksa, Google'lama becerileriniz size yardımcı olacak. Google'ı iyi kullanabilmek de aslında büyük bir dikkat ve çalışma gerektiriyor. Zamanla bu konuda da daha iyileştiğini göreceksin :)

## Sorular

1. Git nedir?
Git, Açık Kaynak Dağıtılmış Sürüm Kontrol Sistemi(Open Source Distributed Version Control System)'dir.
Geliştiriciler bir proje yarattıklarında (örneğin bir uygulama veya web sitesi) ilk resmi (beta olmayan) sürüme kadar ve hatta sonrasında yeni sürümler yayınlayarak kod üzerinde sürekli değişiklik yaparlar. Sürüm kontrol sistemleri, değişiklikleri merkezi bir depoda saklayarak bu revizyonları düzenli tutar. Bu, geliştiricilerin kodun yerel sürümleri üzerinde çalışabilmelerini, değişiklik yapabilmelerini ve en yeni revizyonu yükleyebilmelerini sağlayarak kolayca işbirliği yapmalarına olanak tanır. Her geliştirici bu yeni değişiklikleri görebilir, indirebilir ve katkıda bulunabilir.

2. Git ile GitHub arasında ne fark var?
Git, bir versiyon takip yazılımıdır. Lokal olarak bilgisayarda çalışır ve Github olmadan da Git'i kullanabilmek mümkündür. Git ile projelreinizin versiyonlamasını yapabilir ve bunu internete bile bağlanmadan kullanabilirsiniz. Herhangi bir kayıt işlemine ihtiyaç duymaz.
Github ise Git repository'lerinin cloud üzerinde saklandığı online bir servistir. Github'a kayıt olmanız gereklidir ve ek fayda olarak da başka kişilerin repository'lerine erişebilir ya da kendi repository'lerinize erişmelerini ve katkı sağlamalarını isteyebilirsiniz. Online bir servistir ve offline olarak kullanabilneniz mümkün değildir.
Özetle, Git, bir yazılımın sürüm kontrolü için kullanılan araçtırken, GitHub, kodu bir arada tutmak, işbirliği yapmak ve projeleri yönetmek için kullanılan bir platformdur. Yani, Git’in temel amacı bir projenin kodunu yönetmek iken, GitHub’un amacı ise bu kodu depolamak, paylaşmak, işbirliği yapmak ve yönetmek için bir platform sağlamaktır.

3. Neden bir branch oluşturuyoruz?
Branch oluşturmak kullanıcıya çalıştığı projenin farklı versiyonlarına erişmesini sağlar. Kullanıcı, projesine bir yenilik eklemek istediğinde, yaptığı değişiklik projenin çalışmasını olumsuz etkileyebilir. Bu gibi durumlarda projemizin o anki halini bozmamak için branch kullanabiliriz.Üzerinde çalışılan kaynak kodun bir kopyasını oluşturarak geliştirmelerin orijinal koddan bağımsız olarak ilerlemesini sağlayabildiği için oluşturuyoruz. Örneğin bir git deposu varsayılan olarak master branch'i ile oluşur. Dilerseniz geliştirme amaçlı olarak "development" isminde farklı bir branch oluşturarak kod üzerindeki geliştirmelerinizi burada yapabilir ve test süreci sonrasında hatasız olduğuna emin olduğunuzda değişiklikleri master branch'ine taşıyabilirsiniz.

4. Pull Request'in amacı nedir?
Pull request, açık kaynaklı bir projede katkıda bulunmak isteyen bir kullanıcının, projenin sahibine değişikliklerini inceletmek üzere yaptığı bir taleptir. Bu şekilde projeye katkı sağlamak isteyen kullanıcılar, projenin sahibine değişiklikleri önerir ve projenin sahibi bu değişiklikleri projeye dahil etmek veya reddetmek için karar verir.

5. Bir Branchten diğerine geçmek için kullandığın KOMUT nedir? Mesela `isim-soyisim` branch'inde çalıştığını hayal et ve main branch'ine geçmek istiyorsun, ne yaparsın?
git checkout main (Kodunu yazarım.)

6. `git fetch`, `git merge` ve `git pull` arasındaki farkları açıklayınız. Bu konutlar ne yapar açıklayınız.
git fetch, uzaktaki bir deponun dosyalarını, anlık görüntülerini ve referanslarını yerel deponuza indiren bir komuttur. 
git merge, başka bir branch'deki değişiklikleri üzerinde çalıştığınız kendi branch'inize entegre etme işlemidir. 
git pull, proje ana dosyasındaki yaptığınız değişikliklerin bilgisayarınızdaki versiyonuna çekilmesini sağlar. 

Git fetch, uzaktaki bir deponun dosyalarını, anlık görüntülerini ve referanslarını yerel deponuza indiren bir komuttur. Bu komut, yerel deponuzun mevcut çalışma durumunu güncellemeden uzaktaki verileri indirir, çalışmanızı olduğu gibi bırakır ve getirilen içerik gitcheckout komutu kullanılarak açıkça kontrol edilir.

Öte yandan, git pulls komutu uzaktaki bir depodan verileri getirip indirirken yerel depoyu getirilen verilerle eşleşecek şekilde günceller. Git pulls komutu, git fetch ve git merge komutlarının bir kombinasyonudur, bu nedenle başlangıçta git fetch komutunun işlevini yerine getirir ve daha sonra commit’i birleştirir ve yeni bir merge commit oluşturur.

7. Merge conflict nedir?
Çoğu zaman, insanlar aynı dosyanın aynı satırında farklı değişiklikler yaptığında veya bir kişi bir dosyayı düzenlerken başka bir kişi aynı dosyayı sildiğinde meydana gelir.
8. Merge conflict'i nasıl çözeriz?
Dosyamızı açıp çakışan satırları düzeltmemiz gerekiyor. Dosyamızın içeriğinin ne olacağına karar verip kaydettikten sonra normal bir commit işlemi ile çakışmayı çözme işlemini tamamlıyoruz.