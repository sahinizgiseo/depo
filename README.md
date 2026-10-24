# Asilserp — tasarım çalışması 07

Asilserp SEO platformu için bağımlılıksız HTML/CSS/JavaScript tasarım prototipi. İki sayfa vardır:

- `index.html`: daha küçük yüzen header, değişen açılış sloganı, SEO terimleri akan Matrix arka planı, müşteri markaları, hareketli renk çerçeveli platform paneli, 21 araç kartı, kesintisiz kayan beş telefon ekranı ve tam genişlikte footer.
- `trafigim-dusuyor/index.html`: dokuz adımlı trafik kaybı rehberi, kayıtlı kontrol listesi, bölüm bağlantıları ve yedi soru-cevap.

İki sayfada da Asilserp markasına uyarlanmış SVG devre/çip yükleme ekranı bulunur.

## Çalıştırma

Dosyaları aynı dizin yapısında tutarak `index.html` dosyasını tarayıcıda açın veya:

```sh
cd /workspace/depo
python3 -m http.server 4173 --bind 127.0.0.1
```

Paket kurulumu ve derleme gerekmez. Logo ve Manrope fontları HTML içine gömülüdür; çalışma sırasında harici font veya CDN isteği yapılmaz. İki sayfa da koyu, açık ve lacivert görünümleri destekler. Seçim tarayıcıda hatırlanır.

## Davranışlar

Header 56 piksel kaydırmadan sonra küçülür; üste dönünce eski boyutuna gelir. Masaüstünde yüksekliği 72'den 50 piksele, genişliği %74'e iner. 981–1180 piksel aralığında ve mobilde dar görünüm %84 genişliktedir; 540 piksel ve altında yüksekliği 46 pikseldir. Dar durumdaki logo masaüstünde 118, mobilde 108 piksel genişliğindedir. Kenardaki turuncu/lacivert conic-gradient hareketi korunur. Mobil menü ve Escape ile kapatma çalışır. Dış kapsayıcının yüksekliği sabittir.

Açılış başlığında **SEO’da** sabit kalır. Yanındaki beş ifade yazılıp silinerek değişir: “bir adım öne.”, “veriyle büyü.”, “fırsatı keşfet.”, “rekabette öne.” ve “fark yarat.” Erişilebilir başlık sabit tutulur; ekran okuyucu her karakter değişimini duyurmaz. Slogan hareketi genel durdurma, hareketi azaltma tercihi, gizli sekme ve ekran dışı durumda durur.

Kullanıcının verdiği yeni Matrix CSS’i, raporun arkasında üç akışta 12 okunabilir SEO ifadesi gösterecek şekilde uyarlanmıştır. SEO analizi, anahtar kelime, organik trafik, sıra takibi ve site denetimi gibi ifadeler turuncu/lacivert tonlarda akar. Açık temadaki görünürlüğü artırılmıştır. Katman işaretçi olaylarını engellemez; hareket kontrolünde durur ve hareketi azaltma tercihinde gizlenir.

Açılışın altındaki müşteri alanı kullanıcının birlikte çalıştığını bildirdiği dört markayı gösterir: **ShiftDelete.Net, MediaMarkt, Vestel ve Mis Amasya Tur**. MediaMarkt’ın spiral simgesi ile Vestel’in yazı logosu doğrulanmış Simple Icons dosyalarından gelir. MediaMarkt simgesinin yanında normal marka adı kullanılır. ShiftDelete.Net ve tek bir otobüs firması olan Mis Amasya Tur, güvenilir görsel dosyaları temin edilemediği için düz marka adıyla temsil edilir; bunlar hazırlanmış resmî logo gibi sunulmaz.

Ana sayfadaki panel ve telefon önizlemelerinde alan adı etiketi **Sizin siteniz** olarak gösterilir. Alan adı formu girdiyi doğrular; geçerli bir alan adı girildiğinde açıkça etiketlenmiş örnek raporun başlığında girilen alan adı kullanılır. Platformun dört sekmesi, klavye okları/Home/End, 30/90 gün kontrolleri ve fırsat pencereleri çalışır. Metrik kartlarında küçük trend grafikleri bulunur; büyük grafikte fare ve klavyeyle nokta seçimi tarih/değer açıklamasını gösterir. Örnek teknik denetim kapsamı en fazla 100 sayfadır.

Büyük platform panelinin çevresinde 2 piksel kalınlığında dönen turuncu/lacivert çerçeve ve yumuşak arka ışık bulunur. Açılıştaki örnek rapor kartı da daha ince bir hareketli çerçeve kullanır. Kartlar ve yazılar döndürülmez; renk hareketi kenarlarda kalır. Genel durdurma ve hareketi azaltma tercihleri bu efektlerde de geçerlidir.

Araç kataloğu 18 SEO ve 3 Ads kartından oluşur. Beş mevcut araç doğrulanmış Asilserp kapsamına dayanır; 16 önerilen araç **Yakında** etiketi taşır. Her kart klavyeyle erişilebilir bir ayrıntı penceresi açar. Mevcut araçlar panele ve uygun örnek görünüme yönlendirir; planlanan araçlar çalışıyormuş gibi analiz başlatmaz. Kart başına dönen turuncu/lacivert conic-gradient kenar ve hafif arka ışık kullanılır; yazılar sabit kalır. Animasyonlar kart ekran dışındayken, genel hareket kontrolüyle ve hareketi azaltma tercihinde durur.

SVG devre/çip yükleme ekranı, gerçek sayfa yüklenmesi ve font hazırlığını bekler. En az 550 milisaniye görünür; 1600 milisaniyelik yedek kapanış ve 200 milisaniyelik çıkış geçişi vardır. **Sayfaya geç** ve Escape ile atlanabilir. Kapanışta arka içeriğin, footer dahil, önceki `inert` durumu ve kaydırma kilidi geri yüklenir. JavaScript kapalıysa yükleyici görünmez ve sayfa içeriği erişilebilir kalır. Gösterilen yükleme durumu bir SEO analizi yürütüldüğü anlamına gelmez.

Telefon ekranları HTML/CSS ve SVG ile çizilmiştir. Beş farklı ekran, adım adım bekleyip ilerlemek yerine kesintisiz bir şerit olarak kayar. Normal hız saniyede 38 pikseldir; fare üzerindeyken 26 piksele düşer. Döngünün birleşimini gizleyen beş kopya, ekran okuyuculardan ve klavye etkileşiminden çıkarılmıştır; erişilebilir listede yalnızca beş asıl ekran bulunur.

Telefon şeridinde ok düğmeleri, sağ/sol klavye tuşları, fareyle sürükleme, yatay dokunma kaydırması ve yatay tekerlek desteklenir. Durdur/oynat düğmesi fareyle kullanıldığında odağı üzerinde kalsa da hareketi yönetir. Klavyeyle odaklanıldığında, bölüm ekran dışındayken, sekme gizliyken, genel hareket durdurulduğunda veya hareketi azaltma tercihinde otomatik akış durur. JavaScript kapalıysa doğal yatay kaydırma kullanılabilir. Ekranlar mobil web tasarım önerisidir; yayımlanmış bir mobil uygulama değildir.

Trafik kaybı rehberindeki kontrol listesi `asilserp-traffic-guide-v1` anahtarıyla yalnızca bu tarayıcıda saklanır; hesap senkronizasyonu yoktur. İşaretleri temizleme, ilerleme yüzdesi ve etkin bölüm göstergesi çalışır. Depolama kapalıysa sayfa içindeki işaretleme çalışmaya devam eder.

Kullanıcının sağladığı Uiverse tarzı CSS örnekleri, turuncu/lacivert ışık çerçevesi ve okunabilir SEO terimleri içeren Matrix akışı olarak uyarlanmıştır. Ana sayfadaki hareket kontrolü ve işletim sisteminin hareketi azaltma tercihi desteklenir.

Tam genişlikte lacivert footer; başlangıç çağrısı, araç/platform/rehber bağlantıları, fiyat ve panel bağlantıları, örnek rapor, 2026 telif satırı ve yukarı dönme bağlantısı içerir. Araç düğmeleri mevcut katalog ayrıntı pencerelerini açar; analiz düğmesi alan adı kutusuna odaklanır. Doğrulanmamış destek adresi, sosyal hesap veya hukuki sayfa bağlantısı eklenmemiştir. Footer’ın arka planı üç temada da lacivert kalır ve sabit görünüm seçicisi için alt boşluk bırakılır.

## İçerik ve kaynaklar

- Asilserp'in mevcut sitesi bu çalışma sırasında okunmuştur. Rehberdeki araç kapsamı alan adı analizi, organik sıralamalar, en iyi sayfalar ve HTML site denetimine dayanır. Denetim en fazla 100 sayfa; JavaScript çalıştırma, performans testi veya tam site taraması içermez.
- Panel ve fiyat bağlantıları mevcut `https://asilserp.com/customer-login` ve `https://asilserp.com/fiyatlar` adreslerine gider.
- `https://semust.com/trafigim-dusuyor` dokuz adımlı rehber yapısı için referanstır. Asilserp sürümünün metinleri ve görselleri özgün hazırlanmıştır; Semust'a özgü ürün özellikleri aktarılmamıştır.
- Header davranışı kullanıcının `agent-magicui.vercel.app` referansı ve kaydırmada küçülme açıklamasına dayanır.
- Kullanıcının verdiği [Next.js dashboard konu sayfası](https://github.com/topics/nextjs-dashboard) incelenmiştir. [TailAdmin](https://github.com/TailAdmin/free-nextjs-admin-dashboard) metrik kartları, büyüme etiketleri ve boşluk düzeni; [Kiranism/Shadcn Dashboard](https://github.com/Kiranism/next-shadcn-dashboard-starter) sade çerçeveler, koyu/açık görünüm ve grafik/tablo hiyerarşisi; [NextAdmin](https://github.com/NextAdminHQ/nextjs-admin-dashboard) dönem seçimi ve grafik değer açıklamaları için görsel ilhamdır. İlk ikisinin MIT lisansı doğrulanmıştır; NextAdmin'in lisans dosyası API üzerinden bulunamamıştır. Bu projelerden kod alınmamış; mevcut prototipe bağımlılık veya Next.js geçişi eklenmemiştir.
- Kullanılan logo mevcut `https://asilserp.com/asilserp-logo.png` adresinden alınmıştır: `assets/asilserp-logo-official.png`. Önceki fotoğraf uyarlaması `assets/asilserp-logo.png` olarak korunur, artık gösterilmez.
- Müşteri markalarının dosyaları ve kaynak kayıtları `assets/clients/` altındadır. `sources.json`, MediaMarkt/Vestel Simple Icons kaynaklarını, dosya özetlerini ve diğer iki markadaki metin kullanımının nedenini kaydeder. Birlikte çalışma bilgisi kullanıcının beyanına dayanır.
- Fontlar: Manrope Variable, Latin ve Latin-ext. Font dosyaları ve SIL Open Font License metni `assets/fonts/` altındadır. Türkçe karakterler desteklenir.

## Kapsam ve doğrulama

Bütün panel ve telefon verileri örnektir. Alan adları analiz servisine gönderilmez. Gerçek API bağlantısı, kullanıcı oturumu ve canlı raporlama bu tasarım çalışmasına eklenmemiştir. Rehber otomatik teşhis veya sıralama garantisi sunmaz. Tasarım; footer dahil kullanıcı geri bildirimleriyle geliştirilir.

Chromium/Playwright kontrol kapsamı: iki sayfada 320–1440 piksel arası görünüm, daralan header, değişen slogan ve hareket kontrolleri, müşteri markaları, okunabilir Matrix akışı, footer bağlantıları, tema seçimi, form, sekmeler, grafik etkileşimi, panel/rapor çerçeveleri, araç kartları ve ayrıntı pencereleri, yükleyicinin kapanması ve atlanması, kesintisiz telefon şeridi ve elle kontrol seçenekleri, kontrol listesi ve soru-cevaplar. Ekran görüntüleri iki kat piksel yoğunluğunda `/workspace/artifacts` altında üretilir. Son kontrol sonuçları ilgili çalıştırmanın çıktısından değerlendirilmelidir.

## Paylaşım ve önizleme

Kaynaklar herkese açık [sahinizgiseo/depo](https://github.com/sahinizgiseo/depo) deposunun `main` dalında paylaşılır. İndirilebilir paket [bu HTTPS adresinden](https://raw.githubusercontent.com/sahinizgiseo/depo/main/indir/asilserp-tasarim.zip) sunulur. Güncel ZIP, kök ajan tarafından kontrol ve yayın adımında yeniden oluşturulur.

Bu bulut arayüzünde canlı localhost önizlemesi desteklenmez. Alternatif `raw.githack.com` önizleme bağlantıları paylaşılmıştır; CDN bu yürütme ortamında 403 ağ engeline takıldığı için burada açılarak doğrulanamamıştır. GitHub Pages etkin değildir: oluşturma API'si entegrasyon yetkisi için 403 döndürmüştür. Depoya kaynak yüklemek ile çalışan bir web önizlemesini doğrulamak ayrı durumlardır.

Üretim `asilserp.com` sitesi bu prototiple değiştirilmemiştir. Tasarım çalışması devam etmektedir.
