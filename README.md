# Asilserp — tasarım çalışması 09

Asilserp SEO platformu için bağımlılıksız HTML/CSS/JavaScript tasarım prototipi. Üç sayfa vardır:

- `index.html`: yüzen header, değişen slogan, SEO terimleri akan Matrix, müşteri markaları, kullanım senaryoları, üç adımlı süreç, etkileşimli platform paneli, 21 araç kartı, kesintisiz telefon şeridi, örnek çalışmalar, sekmeli editoryal yorum alanı, paket önizlemesi, ek marka vitrini, sekiz soruluk SSS ve etkileşimli footer.
- `trafigim-dusuyor/index.html`: dokuz adımlı trafik kaybı rehberi, kayıtlı kontrol listesi, bölüm bağlantıları ve yedi soru-cevap.
- `fiyatlar/index.html`: üç paket, kapasite karşılaştırıcısı, özellik/limit tablosu, ortak araç kapsamı, altı soru-cevap ve ana sayfayla ortak etkileşimli footer.

Üç sayfada da ortak marka renkleri, tema seçimi ve Asilserp’e uyarlanmış SVG devre/çip yükleme ekranı bulunur.

## Çalıştırma

Dosyaları aynı dizin yapısında tutarak `index.html` dosyasını tarayıcıda açın veya:

```sh
cd /workspace/depo
python3 -m http.server 4173 --bind 127.0.0.1
```

Paket kurulumu ve derleme gerekmez. Logo ve Manrope fontları HTML içine gömülüdür; çalışma sırasında harici font veya CDN isteği yapılmaz. Üç sayfa da koyu, açık ve lacivert görünümleri destekler. Seçim tarayıcıda hatırlanır.

## Davranışlar

Header 56 piksel kaydırmadan sonra küçülür; üste dönünce eski boyutuna gelir. Masaüstünde yüksekliği 72'den 50 piksele, genişliği %74'e iner. 981–1180 piksel aralığında ve mobilde dar görünüm %84 genişliktedir; 540 piksel ve altında yüksekliği 46 pikseldir. Dar durumdaki logo masaüstünde 118, mobilde 108 piksel genişliğindedir. Kenardaki turuncu/lacivert conic-gradient hareketi korunur. Mobil menü ve Escape ile kapatma çalışır. Dış kapsayıcının yüksekliği sabittir.

Açılış başlığında **SEO’da** sabit kalır. Yanındaki beş ifade yazılıp silinerek değişir: “bir adım öne.”, “veriyle büyü.”, “fırsatı keşfet.”, “rekabette öne.” ve “fark yarat.” Erişilebilir başlık sabit tutulur; ekran okuyucu her karakter değişimini duyurmaz. Slogan hareketi genel durdurma, hareketi azaltma tercihi, gizli sekme ve ekran dışı durumda durur.

Kullanıcının verdiği yeni Matrix CSS’i, raporun arkasında üç akışta 12 okunabilir SEO ifadesi gösterecek şekilde uyarlanmıştır. SEO analizi, anahtar kelime, organik trafik, sıra takibi ve site denetimi gibi ifadeler turuncu/lacivert tonlarda akar. Açık temadaki görünürlüğü artırılmıştır. Katman işaretçi olaylarını engellemez; hareket kontrolünde durur ve hareketi azaltma tercihinde gizlenir.

Açılışın altındaki müşteri alanı kullanıcının birlikte çalıştığını bildirdiği dört markayı gösterir: **ShiftDelete.Net, MediaMarkt, Vestel ve Mis Amasya Tur**. MediaMarkt’ın spiral simgesi ile Vestel’in yazı logosu doğrulanmış Simple Icons dosyalarından gelir. MediaMarkt simgesinin yanında normal marka adı kullanılır. ShiftDelete.Net ve tek bir otobüs firması olan Mis Amasya Tur, güvenilir görsel dosyaları temin edilemediği için düz marka adıyla temsil edilir; bunlar hazırlanmış resmî logo gibi sunulmaz.

Ana sayfanın alt bölümündeki ek marka vitrini, kullanıcının eklenmesini istediği 10 markayı gösterir: **Migros, Aselsan, Anadolu Efes, Türk Tuborg, Opet, LC Waikiki, Mavi, Turkcell, Türkiye İş Bankası ve BİM**. Sekiz markada kaynak kaydı doğrulanmış vektör grafik kullanılır; bunların altısı sağlayıcı şirket simgeleridir, tam yazı logosu olarak sunulmaz. Türkiye İş Bankası ve BİM dosyaları yazı/marka grafikleridir. **LC Waikiki ve Opet**, güvenilir görsel dosyaları edinilemediği için normal marka adıyla temsil edilir. Bu alan müşteri puanı, yıldız, yorum sayısı veya sayısal başarı sonucu içermez; birlikte çalışma bilgisi kullanıcı beyanına dayanır.

Ana sayfadaki panel ve telefon önizlemelerinde alan adı etiketi **Sizin siteniz** olarak gösterilir. Alan adı formu girdiyi doğrular; geçerli bir alan adı girildiğinde açıkça etiketlenmiş örnek raporun başlığında girilen alan adı kullanılır. Platformun dört sekmesi, klavye okları/Home/End, 30/90 gün kontrolleri ve fırsat pencereleri çalışır. Metrik kartlarında küçük trend grafikleri bulunur; büyük grafikte fare ve klavyeyle nokta seçimi tarih/değer açıklamasını gösterir. Örnek teknik denetim kapsamı en fazla 100 sayfadır.

Büyük platform panelinin çevresinde 2 piksel kalınlığında dönen turuncu/lacivert çerçeve ve yumuşak arka ışık bulunur. Açılıştaki örnek rapor kartı da daha ince bir hareketli çerçeve kullanır. Kartlar ve yazılar döndürülmez; renk hareketi kenarlarda kalır. Genel durdurma ve hareketi azaltma tercihleri bu efektlerde de geçerlidir.

Araç kataloğu 18 SEO ve 3 Ads kartından oluşur. Yedi mevcut araç doğrulanmış Asilserp kapsamına dayanır; 14 önerilen araç **Yakında** etiketi taşır. Anahtar Kelime Aracı ve SERP Analizi, güncel fiyatlar kaynağında doğrulanan kapsama göre mevcut araç olarak gösterilir. Her kart klavyeyle erişilebilir bir ayrıntı penceresi açar. Mevcut araçlar panele ve uygun örnek görünüme yönlendirir; planlanan araçlar çalışıyormuş gibi analiz başlatmaz. Kart başına dönen turuncu/lacivert conic-gradient kenar ve hafif arka ışık kullanılır; yazılar sabit kalır. Animasyonlar kart ekran dışındayken, genel hareket kontrolüyle ve hareketi azaltma tercihinde durur.

SVG devre/çip yükleme ekranı, gerçek sayfa yüklenmesi ve font hazırlığını bekler. En az 550 milisaniye görünür; 1600 milisaniyelik yedek kapanış ve 200 milisaniyelik çıkış geçişi vardır. **Sayfaya geç** ve Escape ile atlanabilir. Kapanışta arka içeriğin, footer dahil, önceki `inert` durumu ve kaydırma kilidi geri yüklenir. JavaScript kapalıysa yükleyici görünmez ve sayfa içeriği erişilebilir kalır. Gösterilen yükleme durumu bir SEO analizi yürütüldüğü anlamına gelmez.

Telefon ekranları HTML/CSS ve SVG ile çizilmiştir. Beş farklı ekran, adım adım bekleyip ilerlemek yerine kesintisiz bir şerit olarak kayar. Normal hız saniyede 38 pikseldir; fare üzerindeyken 26 piksele düşer. Döngünün birleşimini gizleyen beş kopya, ekran okuyuculardan ve klavye etkileşiminden çıkarılmıştır; erişilebilir listede yalnızca beş asıl ekran bulunur.

Telefon şeridinde ok düğmeleri, sağ/sol klavye tuşları, fareyle sürükleme, yatay dokunma kaydırması ve yatay tekerlek desteklenir. Durdur/oynat düğmesi fareyle kullanıldığında odağı üzerinde kalsa da hareketi yönetir. Klavyeyle odaklanıldığında, bölüm ekran dışındayken, sekme gizliyken, genel hareket durdurulduğunda veya hareketi azaltma tercihinde otomatik akış durur. JavaScript kapalıysa doğal yatay kaydırma kullanılabilir. Ekranlar mobil web tasarım önerisidir; yayımlanmış bir mobil uygulama değildir.

Trafik kaybı rehberindeki kontrol listesi `asilserp-traffic-guide-v1` anahtarıyla yalnızca bu tarayıcıda saklanır; hesap senkronizasyonu yoktur. İşaretleri temizleme, ilerleme yüzdesi ve etkin bölüm göstergesi çalışır. Depolama kapalıysa sayfa içindeki işaretleme çalışmaya devam eder.

Kullanıcının sağladığı Uiverse tarzı CSS örnekleri, turuncu/lacivert ışık çerçevesi ve okunabilir SEO terimleri içeren Matrix akışı olarak uyarlanmıştır. Ana sayfadaki hareket kontrolü ve işletim sisteminin hareketi azaltma tercihi desteklenir.

Ana sayfa ve fiyatlar sayfasında yeniden tasarlanan footer; büyük bir başlangıç manşeti, **Analiz / Araçlar / Paketler** sekmeli yönlendirme kartı, etkileşimli SEO haritası, araç/platform/rehber bağlantıları ve renkli ışıkla aydınlanan büyük marka yazısını birleştirir. Sekmeler tıklama, ok tuşları ve Home/End ile değişir; açıklama ve hedef bağlantı seçime göre güncellenir. SEO haritasının alan adı, sıralama, denetim ve rapor düğümleri çalışır: ana sayfada ilgili araç penceresini açar; fiyatlar sayfasında ana sayfanın araç bölümüne gider. Analiz bağlantısı ana sayfada alan adı kutusuna odaklanır; fiyatlar sayfasından ana sayfaya yönlendirir. Paket bağlantısı bulunduğu sayfaya uygun yerel hedefi kullanır.

Footer’daki akış çizgileri ve marka ışığı genel durdurma ve hareketi azaltma tercihlerini destekler; yazıların kendisi döndürülmez. 2026 telif satırı ve yukarı dönme bağlantısı korunur. **Tasarım ve geliştirme: İZGİ360** ifadesi üç sayfanın da en alt footer satırında düz metin olarak yer alır; marka adına doğrulanmamış bir URL eklenmez. Destek adresi, sosyal hesap veya hukuki sayfa bağlantısı uydurulmamıştır. Footer üç temada da laciverttir ve sabit görünüm seçicisi için alt boşluk bırakır.

## Ana sayfadaki yeni bölümler

- `#kullanim-senaryolari`: farklı kullanım ihtiyaçlarını üç sekmede açıklar. Eski, tekrarlayan üç platform fayda kartının yerini alır.
- `#nasil-calisir`: alan adıyla başlama, raporları inceleme ve sonraki adımı belirleme sürecini üç adımda gösterir. Önceki kısa ilke şeridinin yerini alır; footer bağlantısından ulaşılır.
- `#calisma-ornekleri`: üç örnek SEO çalışma senaryosu içerir. Gerçek müşterilere ait vaka sonucu veya doğrulanmış sayısal başarı verisi değildir.
- `#yorumlar`: büyük editoryal alıntı, üç konu sekmesi ve önceki/sonraki oklarıyla yeniden tasarlanmıştır. Sorgular/sayfalar, teknik öncelikler ve raporlama bakış açıları arasında elle geçiş yapılır; klavye okları ve Home/End desteklenir. Her içerik **Örnek yorum** olarak etiketlidir; gerçek müşteri markalarına veya kişilere atfedilmez. Geçiş ve işaretçi ışığı, hareket tercihlerine uyar. Gerçek yorum ve çalışma sonucu yayımlanacaksa kullanıcıdan sağlanan, doğrulanmış metinlerle değiştirilmelidir.
- `#paketler`: gerçek başlangıç fiyatlarını ve kapasite farklarını gösteren üç kısa paket kartıdır. Ayrıntılı karşılaştırma için yerel fiyatlar sayfasına gider.
- `#sss`: kategori filtreleriyle sekiz olgusal soru-cevap sunar.
- `#markalar-alt`: üstteki dört müşteri markasından ayrı, 10 markalık alt vitrindir; puan veya yıldız değerlendirmesi göstermez.

Üst menüde önceki “Nasıl çalışır?” düğmesi **Fiyatlar** bağlantısıyla değiştirilmiştir. Süreç bölümü ana sayfada ve footer bağlantısında korunur. Ana sayfa ve rehberdeki fiyat bağlantıları `fiyatlar/index.html` sayfasına yönelir.

## Paketler ve fiyatlar

Yeni fiyatlar sayfasının kaynak içeriği, bu turda yeniden okunan `https://asilserp.com/fiyatlar` adresidir. Fiyatlar aylık TL başlangıç fiyatlarıdır; vergi ve tahsilat koşulları hesap açılışında ayrıca netleştirilir.

| Paket | Aylık başlangıç | Proje | Toplam kayıtlı hedef kelime | SEO araştırması / ay | AI ve içerik işlemi / ay |
|---|---:|---:|---:|---:|---:|
| SEO Başlangıç | ₺2.990 | 3 | 100 | 100 | 20 |
| SEO Büyüme | ₺4.590 | 10 | 500 | 400 | 80 |
| Ajans Pro | ₺9.290 | 30 | 1.500 | 1.200 | 250 |

Kapasite karşılaştırıcısı proje, toplam hedef kelime ve aylık işlem ihtiyaçlarını paket üst sınırlarıyla karşılaştırır. Bir projeye en fazla 100 hedef kelime kaydedilebilir. Bu hesaplama hesap veya ödeme başlatmaz; gerçek ücretli kullanım ayrıca veri bütçesiyle sınırlanır. Araştırma/AI sayıları üst sınırdır: veri bütçesi dolarsa kullanılmamış işlem adedi olsa da yeni ücretli sorgu durur.

Aylık SEO ve AI kotaları UTC takvim ayı başında yenilenir; kullanılmayan haklar devretmez. Proje/kayıt silmek veya paket değiştirmek o ayın tüketimini sıfırlamaz. Otomatik günlük sıralama takibi ve ayrı ekip girişleri henüz sunulmaz. Hesap açılışı ve paket değişiklikleri ekip tarafından yönetilir; fiyatlar sayfası ödeme almaz ve karttan ücret çekmez. Giriş bağlantıları mevcut Asilserp müşteri girişine gider.

Ortak araçlar, kapasite tablosu ve altı SSS bu koşulları açıklamak için tasarlanmıştır. Canlı ChatGPT/Gemini ve AI kelime hacmi kapsamı şu anda ABD / İngilizce’dir; yeni AI ve içerik araçlarının gerçek ücretli verilerle doğrulaması sürmektedir. HTML site denetimi en fazla 100 sayfadır; otomatik günlük takip veya ayrı ekip hesabı vaadi eklenmemiştir.

## İçerik ve kaynaklar

- Asilserp'in mevcut sitesi bu çalışma sırasında okunmuştur. Rehberdeki araç kapsamı alan adı analizi, organik sıralamalar, en iyi sayfalar ve HTML site denetimine dayanır. Denetim en fazla 100 sayfa; JavaScript çalıştırma, performans testi veya tam site taraması içermez.
- Panel bağlantıları mevcut `https://asilserp.com/customer-login` adresine gider. Fiyatlar tasarımı `https://asilserp.com/fiyatlar` kaynak içeriğine dayanır; prototip içindeki fiyatlar gezinmesi yerel `fiyatlar/index.html` sayfasını açar.
- `https://semust.com/trafigim-dusuyor` dokuz adımlı rehber yapısı için referanstır. Asilserp sürümünün metinleri ve görselleri özgün hazırlanmıştır; Semust'a özgü ürün özellikleri aktarılmamıştır.
- Header davranışı kullanıcının `agent-magicui.vercel.app` referansı ve kaydırmada küçülme açıklamasına dayanır.
- Kullanıcının verdiği [Next.js dashboard konu sayfası](https://github.com/topics/nextjs-dashboard) incelenmiştir. [TailAdmin](https://github.com/TailAdmin/free-nextjs-admin-dashboard) metrik kartları, büyüme etiketleri ve boşluk düzeni; [Kiranism/Shadcn Dashboard](https://github.com/Kiranism/next-shadcn-dashboard-starter) sade çerçeveler, koyu/açık görünüm ve grafik/tablo hiyerarşisi; [NextAdmin](https://github.com/NextAdminHQ/nextjs-admin-dashboard) dönem seçimi ve grafik değer açıklamaları için görsel ilhamdır. İlk ikisinin MIT lisansı doğrulanmıştır; NextAdmin'in lisans dosyası API üzerinden bulunamamıştır. Bu projelerden kod alınmamış; mevcut prototipe bağımlılık veya Next.js geçişi eklenmemiştir.
- Kullanılan logo mevcut `https://asilserp.com/asilserp-logo.png` adresinden alınmıştır: `assets/asilserp-logo-official.png`. Önceki fotoğraf uyarlaması `assets/asilserp-logo.png` olarak korunur, artık gösterilmez.
- Üst müşteri markalarının dosyaları ve kaynak kayıtları `assets/clients/` altındadır. `sources.json`, MediaMarkt/Vestel Simple Icons kaynaklarını, dosya özetlerini ve diğer iki markadaki metin kullanımının nedenini kaydeder. Alt vitrinin grafikleri `assets/clients-lower/` altında tutulur; kaynak kayıtları sağlayıcı simgesi/yazı logosu ayrımını, kaynak adreslerini, dosya özetlerini ve LC Waikiki/Opet metin kullanımını belirtir. Altı sağlayıcı simgesi, TradingView BIST şirket eşlemesini kaydeden herkese açık Fundhunter arşivinden; Türkiye İş Bankası Wikimedia kaynak kaydı bulunan bir SVG arşivinden; BİM ise Simple Icons kaynağından edinilmiştir. Birlikte çalışma bilgisi kullanıcının beyanına dayanır.
- Fontlar: Manrope Variable, Latin ve Latin-ext. Font dosyaları ve SIL Open Font License metni `assets/fonts/` altındadır. Türkçe karakterler desteklenir.

## Kapsam ve doğrulama

Bütün panel ve telefon verileri örnektir. Alan adları analiz servisine gönderilmez. Gerçek API bağlantısı, kullanıcı oturumu ve canlı raporlama bu tasarım çalışmasına eklenmemiştir. Rehber otomatik teşhis veya sıralama garantisi sunmaz. Tasarım; footer dahil kullanıcı geri bildirimleriyle geliştirilir.

Chromium/Playwright kontrol kapsamı: üç sayfada 320–1440 piksel arası görünüm, daralan header, değişen slogan ve hareket kontrolleri, üst/alt müşteri markaları ve puansız gösterim, okunabilir Matrix akışı, footer sekmeleri/bağlantıları ve son İZGİ360 satırı, tema seçimi, form, sekmeler, grafik etkileşimi, panel/rapor çerçeveleri, araç kartları ve ayrıntı pencereleri, yükleyicinin kapanması ve atlanması, kesintisiz telefon şeridi ve elle kontrol seçenekleri, kullanım senaryosu sekmeleri, örnek çalışma etiketleri, editoryal yorum sekmeleri/okları ve örnek yorum etiketleri, paket kartları, fiyatlar kapasite karşılaştırıcısı ve limit tablosu, kategori filtreli SSS, rehber kontrol listesi ve soru-cevaplar. Ekran görüntüleri iki kat piksel yoğunluğunda `/workspace/artifacts` altında üretilir. Son kontrol sonuçları ilgili çalıştırmanın çıktısından değerlendirilmelidir.

## Paylaşım ve önizleme

Kaynaklar herkese açık [sahinizgiseo/depo](https://github.com/sahinizgiseo/depo) deposunun `main` dalında paylaşılır. İndirilebilir paket [bu HTTPS adresinden](https://raw.githubusercontent.com/sahinizgiseo/depo/main/indir/asilserp-tasarim.zip) sunulur. Güncel ZIP, kök ajan tarafından kontrol ve yayın adımında yeniden oluşturulur.

Bu bulut arayüzünde canlı localhost önizlemesi desteklenmez. Alternatif `raw.githack.com` önizleme bağlantıları paylaşılmıştır; CDN bu yürütme ortamında 403 ağ engeline takıldığı için burada açılarak doğrulanamamıştır. GitHub Pages etkin değildir: oluşturma API'si entegrasyon yetkisi için 403 döndürmüştür. Depoya kaynak yüklemek ile çalışan bir web önizlemesini doğrulamak ayrı durumlardır.

Üretim `asilserp.com` sitesi bu prototiple değiştirilmemiştir. Tasarım çalışması devam etmektedir.
