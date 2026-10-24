# Asilserp — tasarım çalışması 10

Asilserp SEO platformu için bağımlılıksız HTML/CSS/JavaScript tasarım prototipi. Üç asıl sayfa ve bir uyumluluk yönlendirmesi bulunur:

- `index.html`: yüzen header, değişen slogan, SEO terimleri akan Matrix, etkileşimli SEO araç haritası, üç adımlı süreç, platform paneli, kullanım senaryoları, 21 araç kartı, kesintisiz telefon şeridi, örnek çalışmalar, editoryal yorum alanı, dört paket önizlemesi, sekiz soruluk SSS, tek marka vitrini ve etkileşimli footer.
- `fiyatlar/index.html`: dört paket, kapasite önericisi, özellik/limit karşılaştırma tablosu, ortak araç kapsamı, yedi soru-cevap ve ana sayfayla ortak footer.
- `seo-yol-haritasi/index.html`: dokuz adımlı **SEO Yol Haritası**, kayıtlı kontrol listesi, bölüm bağlantıları ve yedi soru-cevap. Başlık ve anlatım, organik görünürlük verilerini bir SEO çalışma planına dönüştürmeye odaklanır.
- `trafigim-dusuyor/index.html`: eski bağlantılar için yeni rehbere yönlendirme yapar. Sorgu parametreleri ve URL parçası (`?…` ve `#…`) yeni rotaya taşınır.

Üç asıl sayfada ortak marka renkleri, tema seçimi, SVG devre/çip yükleme ekranı ve en altta **Tasarım ve geliştirme: İZGİ360** kredisi bulunur.

## Çalıştırma

Dosyaları aynı dizin yapısında tutarak `index.html` dosyasını tarayıcıda açın veya:

```sh
cd /workspace/depo
python3 -m http.server 4173 --bind 127.0.0.1
```

Paket kurulumu ve derleme gerekmez. Logo ve Manrope fontları HTML içine gömülüdür; çalışma sırasında harici font veya CDN isteği yapılmaz. Üç asıl sayfa da koyu, açık ve lacivert görünümleri destekler. Seçim tarayıcıda hatırlanır.

## Görsel davranışlar ve etkileşimler

Header 56 piksel kaydırmadan sonra küçülür; üste dönünce eski boyutuna gelir. Masaüstünde yüksekliği 72'den 50 piksele, genişliği %74'e iner. 981–1180 piksel aralığında ve mobilde dar görünüm %84 genişliktedir; 540 piksel ve altında yüksekliği 46 pikseldir. Dar durumdaki logo masaüstünde 118, mobilde 108 piksel genişliğindedir. Kenardaki turuncu/lacivert conic-gradient hareketi, mobil menü ve Escape ile kapatma çalışır. Dış kapsayıcının yüksekliği sabittir.

Açılış başlığında **SEO’da** sabit kalır. Beş ifade yazılıp silinerek değişir: “bir adım öne.”, “veriyle büyü.”, “fırsatı keşfet.”, “rekabette öne.” ve “fark yarat.” Erişilebilir başlık sabittir; ekran okuyucu her karakter değişimini duyurmaz. Slogan hareketi genel durdurma, hareketi azaltma tercihi, gizli sekme ve ekran dışı durumda durur.

Kullanıcının verdiği Matrix CSS’i, raporun arkasında üç akışta 12 okunabilir SEO ifadesi gösterir. SEO analizi, anahtar kelime, organik trafik, sıra takibi ve site denetimi gibi ifadeler turuncu/lacivert tonlarda akar. Açık temadaki görünürlüğü güçlendirilmiştir. Katman işaretçi olaylarını engellemez; genel hareket kontrolünde durur, hareketi azaltma tercihinde gizlenir.

Panel ve telefon önizlemelerindeki alan adı etiketi **Sizin siteniz** olarak gösterilir. Alan adı formu girdiyi doğrular; geçerli bir alan adı girildiğinde örnek rapor başlığında girilen alan adı kullanılır. Dört platform sekmesi, klavye okları/Home/End, 30/90 gün kontrolleri ve fırsat pencereleri çalışır. Küçük trend grafikleri ve büyük grafikte fare/klavyeyle tarih-değer gösterimi bulunur. Örnek teknik denetim en fazla 100 sayfayı kapsar.

Büyük platform panelinin çevresinde 2 piksel kalınlığında dönen turuncu/lacivert çerçeve ve yumuşak arka ışık vardır. Çerçeve uygulama kutusunu sarar; alt açıklama alanını kaplamaz. Açılış rapor kartının daha ince hareketli kenarı bulunur. Kartlar ve yazılar sabit kalır; genel durdurma ve hareketi azaltma tercihi bu efektleri de kontrol eder.

Araç kataloğu 18 SEO ve 3 Ads kartından oluşur. Yedi mevcut araç, doğrulanan Asilserp kapsamına dayanır; 14 önerilen araç **Yakında** etiketi taşır. Anahtar Kelime Aracı ve SERP Analizi, fiyatlar kaynağında doğrulanan kapsama göre mevcut araçtır. Her kart klavyeyle erişilebilir bir ayrıntı penceresi açar. Mevcut araçlar panele veya uygun örnek görünüme yönlendirir; planlanan araçlar canlı analiz başlatmaz. Kartların dönen renkli kenarları ekran dışındayken, genel durdurmada ve hareketi azaltma tercihinde durur.

SVG devre/çip yükleme ekranı, sayfa yüklenmesi ve font hazırlığını bekler. En az 550 milisaniye görünür; 1600 milisaniyelik yedek kapanış ve 200 milisaniyelik çıkış geçişi vardır. **Sayfaya geç** ve Escape ile atlanabilir. Kapanışta footer dahil arka içeriğin önceki `inert` durumu ve kaydırma kilidi geri yüklenir. JavaScript kapalıysa yükleyici görünmez; sayfa içeriği erişilebilir kalır. Bu yükleme durumu bir SEO analizi yürütüldüğü anlamına gelmez.

Telefon ekranları HTML/CSS ve SVG ile çizilmiştir. Beş özgün ekran kesintisiz bir şerit olarak kayar; döngü kopyaları ekran okuyuculardan ve klavye etkileşiminden çıkarılmıştır. Normal hız saniyede 38 piksel, fare üzerindeyken 26 pikseldir. Ok düğmeleri, sağ/sol tuşları, fareyle sürükleme, yatay dokunma ve yatay tekerlek desteklenir. Açık oynatma isteği klavye veya fare odağı düğme üzerinde kalsa da akışı başlatabilir. Bölüm ekran dışındayken, sekme gizliyken, genel hareket durdurulduğunda veya hareketi azaltma tercihinde otomatik akış durur. JavaScript kapalıysa doğal yatay kaydırma kullanılabilir. Ekranlar mobil web tasarımıdır; yayımlanmış bir mobil uygulama değildir.

SEO Yol Haritası kontrol listesi, eski rehberden kalan işaretleri de okuyabilmek için `asilserp-traffic-guide-v1` anahtarını korur. İlerleme yalnızca bu tarayıcıda saklanır; hesap senkronizasyonu yoktur. İşaretleri temizleme, ilerleme yüzdesi, etkin bölüm göstergesi ve soru-cevaplar çalışır. Depolama kapalıysa işaretleme sayfa açıkken kullanılabilir.

## Ana sayfa bölümleri

- `#seo-arac-haritasi`: etkileşimli SEO haritası yalnızca ana sayfadadır ve `#nasil-calisir` bölümünün hemen önünde yer alır. Alan adı, sıralama, denetim ve rapor düğümleri ilgili araç ayrıntısını açar.
- `#nasil-calisir`: alan adıyla başlama, raporları inceleme ve önceliği belirleme akışını üç adımda gösterir.
- `#kullanim-senaryolari`: e-ticaret, ajans ve içerik sitesi ihtiyaçlarını üç sekmede açıklar.
- `#calisma-ornekleri`: üç örnek SEO çalışma senaryosu içerir. Gerçek müşterilere ait vaka sonucu veya doğrulanmış sayısal başarı verisi değildir.
- `#yorumlar`: büyük editoryal alıntı, üç konu sekmesi ve önceki/sonraki okları içerir. Sorgular/sayfalar, teknik öncelikler ve raporlama arasında elle geçiş yapılır; ok tuşları ve Home/End desteklenir. İçerikler **Örnek yorum** olarak etiketlidir ve gerçek marka veya kişilere atfedilmez. Gerçek görüşler yayımlanacaksa kullanıcıdan sağlanan, doğrulanmış metinlerle değiştirilmelidir.
- `#paketler`: SEO Mini dahil dört paketin kısa kapasite ve fiyat önizlemesidir. Ayrıntılar yerel fiyatlar sayfasına gider.
- `#sss`: kategori filtreli sekiz soru-cevap sunar. 07. soru SEO Mini’nin ilk 7 gün ücretsiz denemesini, ardından aylık 400 TL fiyatını ve paket geçişini açıklar.
- `#markalar-alt`: 15 markanın tek vitrinidir; ana sayfanın alt bölümündedir. Kullanıcının birlikte çalıştığını bildirdiği markalar **ShiftDelete.Net, MediaMarkt, Vestel, Mis Amasya Tur, Migros, Aselsan, Anadolu Efes, Türk Tuborg, Opet, LC Waikiki, Mavi, Turkcell, Türkiye İş Bankası, BİM ve işbul.net** olarak bir araya getirilir. Alan puan, yıldız, yorum sayısı veya sayısal başarı sonucu göstermez.

Marka varlıklarında doğrulanan görsel dosya, sağlayıcı şirket simgesi ve normal marka adı gösterimi birbirinden ayrılır; her grafik tam resmî yazı logosu gibi sunulmaz. ShiftDelete.Net için doğrulanan PNG dosyası kullanılır. Kullanılan dosyaların doğrulama durumu, kaynakları ve grafik türü `assets/clients/` ile `assets/clients-lower/` altındaki `sources.json` kayıtlarında tutulur. Görsel doğrulanamayan markalarda uydurma grafik yerine normal marka adı kullanılabilir. Birlikte çalışma bilgisi kullanıcı beyanına dayanır.

## Footer ve gezinme

Ana sayfa ve fiyatlar footer’ı; büyük başlangıç manşeti, **Analiz / Araçlar / Paketler** sekmeli yönlendirme kartı, araç/platform/SEO Yol Haritası bağlantıları ve ışıkla aydınlanan büyük marka yazısını içerir. Launcher sekmeleri tıklama, ok tuşları ve Home/End ile değişir; açıklama ve hedef bağlantı seçime göre güncellenir. SEO araç haritası footer’ın içinde değildir; ana sayfada süreç bölümünün önündedir.

Analiz hedefi ana sayfada alan adı kutusuna odaklanır; fiyatlar sayfasından ana sayfaya gider. Araç ve paket hedefleri bulunduğu sayfaya uygun yerel rotayı kullanır. Footer ışıkları genel durdurma ve hareketi azaltma tercihlerini destekler. 2026 telif satırı, yukarı dönme bağlantısı ve son satırdaki **Tasarım ve geliştirme: İZGİ360** korunur. Marka adına doğrulanmamış URL, destek adresi, sosyal hesap veya hukuki sayfa bağlantısı eklenmemiştir. Footer üç temada da laciverttir ve görünüm seçicisi için alt boşluk bırakır.

Menü ve içerik bağlantıları yeni rehber için `seo-yol-haritasi/index.html`, paketler için `fiyatlar/index.html` rotalarını kullanır. Eski rehber rotası sorgu ve parça bilgisini koruyarak yeni rehbere geçer.

## Paketler ve fiyatlar

SEO Başlangıç, SEO Büyüme ve Ajans Pro’nun fiyat/kapasiteleri `https://asilserp.com/fiyatlar` kaynak sayfasından okunmuştur. **SEO Mini ile ilk 7 gün ücretsiz deneme ve ardından aylık 400 TL koşulu, kullanıcının bu oturumda tanımladığı yeni paket politikasıdır; önceki üç paketli kaynak sayfadan türetilmemiştir.**

Fiyatlar aylık TL başlangıç fiyatlarıdır. Vergi ve tahsilat koşulları hesap açılışında ayrıca netleştirilir.

| Paket | Ücretsiz deneme | Aylık başlangıç | Proje | Toplam kayıtlı hedef kelime | SEO araştırması / ay | AI ve içerik işlemi / ay |
|---|---|---:|---:|---:|---:|---:|
| SEO Mini | İlk 7 gün | ₺400 | 1 | 20 | 20 | 5 |
| SEO Başlangıç | — | ₺2.990 | 3 | 100 | 100 | 20 |
| SEO Büyüme | — | ₺4.590 | 10 | 500 | 400 | 80 |
| Ajans Pro | — | ₺9.290 | 30 | 1.500 | 1.200 | 250 |

Kapasite önericisi dört paketi sırayla değerlendirir; proje, toplam hedef kelime, aylık SEO araştırması ve AI işlem ihtiyacını karşılayan en düşük kapasiteyi gösterir. Bir projede en fazla 100 hedef kelime bulunabilir. SEO Mini önerildiğinde 7 günlük deneme bilgisi de görünür. Paket sınırlarını aşan veya geçersiz girdiler için açıklama gösterilir.

Bu karşılaştırıcı gerçek hesap, deneme veya ödeme başlatmaz. Deneme ve paket geçişlerinde Asilserp ekibi yardımcı olur; arayüz karttan otomatik ücret çekmez. Gerçek ücretli kullanım ayrıca veri bütçesiyle sınırlanır. Araştırma/AI adetleri üst sınırdır: veri bütçesi dolarsa kullanılmamış işlem adedi olsa da yeni ücretli sorgu durur.

Aylık SEO ve AI kotaları UTC takvim ayı başında yenilenir; kullanılmayan haklar devretmez. Proje/kayıt silmek veya paket değiştirmek o ayın tüketimini sıfırlamaz. Otomatik günlük sıralama takibi ve ayrı ekip girişleri henüz sunulmaz. Giriş bağlantıları mevcut Asilserp müşteri girişine gider.

Fiyatlar sayfasındaki ortak araç grupları, dört paketli kapasite tablosu ve yedi SSS kapsamı ve kullanım koşullarını açıklar. Canlı ChatGPT/Gemini ile AI kelime hacmi kapsamı şu anda ABD / İngilizce’dir; yeni AI/içerik araçlarının gerçek ücretli verilerle doğrulaması sürmektedir. HTML site denetimi en fazla 100 sayfadır; JavaScript çalıştırma, performans testi veya tam site taraması içermez. “Her pakette aynı araçlar” ifadesi, fiyatlar kaynağında belirtilen mevcut kapsamı anlatır; ana sayfada **Yakında** olarak gösterilen bütün tasarım önerilerinin kullanıma açıldığı anlamına gelmez.

## İçerik, varlıklar ve lisanslar

- Kullanıcı logo, renk, Uiverse tarzı ışık/Matrix CSS örnekleri ve tasarım referansları sağlamıştır. Bu efektler turuncu/lacivert kimliğe uyarlanmıştır.
- Asilserp’in mevcut sitesi ve fiyatlar içeriği bu çalışma sırasında okunmuştur. Panel bağlantıları doğrulanan `https://asilserp.com/customer-login` adresine gider. Fiyatlar gezinmesi prototipte yerel sayfayı açar.
- SEO Yol Haritası’nın dokuz adımlı özgün metinleri ve görselleri Asilserp’e göre hazırlanmıştır. Önceki rehber yapısında `https://semust.com/trafigim-dusuyor` referansı incelenmiş; yeni rota ve görünen başlıklar SEO Yol Haritası olarak düzenlenmiştir.
- Header davranışı kullanıcının `agent-magicui.vercel.app` referansı ve kaydırmada küçülme açıklamasına dayanır.
- [Next.js dashboard konu sayfası](https://github.com/topics/nextjs-dashboard) incelenmiştir. [TailAdmin](https://github.com/TailAdmin/free-nextjs-admin-dashboard) metrik kartları ve boşluk düzeni; [Kiranism/Shadcn Dashboard](https://github.com/Kiranism/next-shadcn-dashboard-starter) sade çerçeveler ile grafik/tablo hiyerarşisi; [NextAdmin](https://github.com/NextAdminHQ/nextjs-admin-dashboard) dönem seçimi ve değer açıklamaları için görsel ilhamdır. İlk ikisinin MIT lisansı doğrulanmıştır; NextAdmin’in lisans dosyası API üzerinden bulunamamıştır. Bu projelerden kod alınmamış, bağımlılık veya Next.js geçişi eklenmemiştir.
- Asilserp logosu `https://asilserp.com/asilserp-logo.png` kaynağından alınmıştır: `assets/asilserp-logo-official.png`. Önceki fotoğraf uyarlaması `assets/asilserp-logo.png` olarak korunur ve gösterilmez.
- Müşteri marka varlıklarının kaynak adresleri, dosya özetleri ve simge/yazı logosu ayrımları ilgili `sources.json` dosyalarındadır. Bu kayıtlar yeni görseller doğrulandıkça güncellenir; README sabit bir doğrulanmış-logo sayısı iddia etmez.
- Fontlar Manrope Variable Latin ve Latin-ext’tir. Dosyalar ve SIL Open Font License metni `assets/fonts/` altındadır; Türkçe karakterler desteklenir.

## Kapsam ve doğrulama

Bütün panel ve telefon verileri örnektir. Alan adları analiz servisine gönderilmez. Gerçek API bağlantısı, kullanıcı oturumu, deneme/abonelik başlatma, ödeme tahsilatı ve canlı raporlama bu tasarım prototipine bağlanmamıştır. Rehber otomatik teşhis veya sıralama garantisi sunmaz. Örnek yorumlar doğrulanmış müşteri görüşleri olarak kullanılmamalıdır. Tasarım, kullanıcı geri bildirimleriyle geliştirilir.

Chromium/Playwright kontrol kapsamı: üç asıl sayfada dar/mobil ve masaüstü görünüm, küçülen header, slogan/Matrix ve hareket tercihleri, tek marka vitrini, SEO araç haritasının ana sayfadaki konumu ve düğümleri, footer launcher sekmeleri/bağlantıları ve son İZGİ360 satırı, tema seçimi, form, grafik/sekme etkileşimleri, çerçeveler, araç kartları, yükleyici temizliği, telefon şeridi ve elle kontrol seçenekleri, kullanım senaryoları, örnek çalışma/yorum etiketleri, dört paket önizlemesi, dört basamaklı kapasite önerisi, deneme açıklaması, karşılaştırma tablosu, SSS, yeni rehberde eski kontrol kayıtları ve eski rotanın sorgu/parça yönlendirmesi. Son test durumu ilgili çalıştırmanın raporundan değerlendirilmelidir; bu liste tek başına bütün kontrollerin geçtiği anlamına gelmez.

Ekran görüntüleri iki kat piksel yoğunluğunda `/workspace/artifacts` altında üretilir.

## Paylaşım ve önizleme

Kaynaklar herkese açık [sahinizgiseo/depo](https://github.com/sahinizgiseo/depo) deposunun `main` dalında paylaşılır. İndirilebilir paket [bu HTTPS adresinden](https://raw.githubusercontent.com/sahinizgiseo/depo/main/indir/asilserp-tasarim.zip) sunulur. ZIP, kök ajan tarafından kontrol ve yayın adımında yeniden oluşturulur; tek başına yerel dosyayı değiştirmek uzak paketi güncellemez.

Bu bulut arayüzünde canlı localhost önizlemesi desteklenmez. Alternatif `raw.githack.com` bağlantıları paylaşılmıştır; CDN bu yürütme ortamında ağ engeline takıldığı için burada açılarak doğrulanamamıştır. GitHub Pages oluşturma API’si entegrasyon yetkisi için 403 döndürmüştür. Kaynakları depoya yüklemek ile çalışan web önizlemesini doğrulamak ayrı durumlardır.

Üretim `asilserp.com` sitesi bu prototiple değiştirilmemiştir. Tasarım çalışması devam etmektedir.
