# Asilserp — tasarım çalışması 05

Asilserp SEO platformu için bağımlılıksız HTML/CSS/JavaScript tasarım prototipi. İki sayfa vardır:

- `index.html`: belirgin biçimde küçülen ve renkli kenarı hareket eden header, açılış ekranı, etkileşimli platform paneli, 21 araç kartı ve kayan beş telefon ekranı.
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

Header 56 piksel kaydırmadan sonra küçülür; üste dönünce eski boyutuna gelir. Masaüstünde yüksekliği 72'den 54 piksele, genişliği %80'e iner. 981–1180 piksel aralığında dar görünüm %88 genişliktedir. Mobilde de genişlik %88 olur; 540 piksel ve altında yüksekliği 50 pikseldir. Kenardaki turuncu/lacivert conic-gradient hareketi belirginleştirilmiştir. Mobil menü ve Escape ile kapatma çalışır. Dış kapsayıcının yüksekliği sabittir.

Alan adı formu girdiyi doğrular ve açıkça etiketlenmiş örnek raporu açar. Platformun dört sekmesi, klavye okları/Home/End, 30/90 gün kontrolleri ve fırsat pencereleri çalışır. Metrik kartlarında küçük trend grafikleri bulunur; büyük grafikte fare ve klavyeyle nokta seçimi tarih/değer açıklamasını gösterir. Örnek teknik denetim kapsamı en fazla 100 sayfadır.

Araç kataloğu 18 SEO ve 3 Ads kartından oluşur. Beş mevcut araç doğrulanmış Asilserp kapsamına dayanır; 16 önerilen araç **Yakında** etiketi taşır. Her kart klavyeyle erişilebilir bir ayrıntı penceresi açar. Mevcut araçlar panele ve uygun örnek görünüme yönlendirir; planlanan araçlar çalışıyormuş gibi analiz başlatmaz. Kart başına dönen turuncu/lacivert conic-gradient kenar ve hafif arka ışık kullanılır; yazılar sabit kalır. Animasyonlar kart ekran dışındayken, genel hareket kontrolüyle ve hareketi azaltma tercihinde durur.

SVG devre/çip yükleme ekranı, gerçek sayfa yüklenmesi ve font hazırlığını bekler. En az 550 milisaniye görünür; 1600 milisaniyelik yedek kapanış ve 200 milisaniyelik çıkış geçişi vardır. **Sayfaya geç** ve Escape ile atlanabilir. Kapanışta arka içeriğin `inert` durumu ve kaydırma kilidi temizlenir. JavaScript kapalıysa yükleyici görünmez ve sayfa içeriği erişilebilir kalır. Gösterilen yükleme durumu bir SEO analizi yürütüldüğü anlamına gelmez.

Telefon ekranları HTML/CSS ve SVG ile çizilmiştir. Yatay kaydırma, dokunma, fareyle sürükleme, ok düğmeleri, klavye ve durdurma düğmesi desteklenir. Otomatik ilerleme yalnızca bölüm görünürken çalışır; kullanıcı etkileşiminde, odakta, fare üzerinde, gizli sekmede ve hareketi azaltma tercihinde durur. Ekranlar mobil web tasarım önerisidir; yayımlanmış bir mobil uygulama değildir.

Trafik kaybı rehberindeki kontrol listesi `asilserp-traffic-guide-v1` anahtarıyla yalnızca bu tarayıcıda saklanır; hesap senkronizasyonu yoktur. İşaretleri temizleme, ilerleme yüzdesi ve etkin bölüm göstergesi çalışır. Depolama kapalıysa sayfa içindeki işaretleme çalışmaya devam eder.

Kullanıcının sağladığı Uiverse tarzı CSS örnekleri, turuncu/lacivert ışık çerçevesi ve hafif Matrix animasyonu olarak uyarlanmıştır. Ana sayfadaki hareket kontrolü ve işletim sisteminin hareketi azaltma tercihi desteklenir.

## İçerik ve kaynaklar

- Asilserp'in mevcut sitesi bu çalışma sırasında okunmuştur. Rehberdeki araç kapsamı alan adı analizi, organik sıralamalar, en iyi sayfalar ve HTML site denetimine dayanır. Denetim en fazla 100 sayfa; JavaScript çalıştırma, performans testi veya tam site taraması içermez.
- Panel ve fiyat bağlantıları mevcut `https://asilserp.com/customer-login` ve `https://asilserp.com/fiyatlar` adreslerine gider.
- `https://semust.com/trafigim-dusuyor` dokuz adımlı rehber yapısı için referanstır. Asilserp sürümünün metinleri ve görselleri özgün hazırlanmıştır; Semust'a özgü ürün özellikleri aktarılmamıştır.
- Header davranışı kullanıcının `agent-magicui.vercel.app` referansı ve kaydırmada küçülme açıklamasına dayanır.
- Kullanıcının verdiği [Next.js dashboard konu sayfası](https://github.com/topics/nextjs-dashboard) incelenmiştir. [TailAdmin](https://github.com/TailAdmin/free-nextjs-admin-dashboard) metrik kartları, büyüme etiketleri ve boşluk düzeni; [Kiranism/Shadcn Dashboard](https://github.com/Kiranism/next-shadcn-dashboard-starter) sade çerçeveler, koyu/açık görünüm ve grafik/tablo hiyerarşisi; [NextAdmin](https://github.com/NextAdminHQ/nextjs-admin-dashboard) dönem seçimi ve grafik değer açıklamaları için görsel ilhamdır. İlk ikisinin MIT lisansı doğrulanmıştır; NextAdmin'in lisans dosyası API üzerinden bulunamamıştır. Bu projelerden kod alınmamış; mevcut prototipe bağımlılık veya Next.js geçişi eklenmemiştir.
- Kullanılan logo mevcut `https://asilserp.com/asilserp-logo.png` adresinden alınmıştır: `assets/asilserp-logo-official.png`. Önceki fotoğraf uyarlaması `assets/asilserp-logo.png` olarak korunur, artık gösterilmez.
- Fontlar: Manrope Variable, Latin ve Latin-ext. Font dosyaları ve SIL Open Font License metni `assets/fonts/` altındadır. Türkçe karakterler desteklenir.

## Kapsam ve doğrulama

Bütün panel ve telefon verileri örnektir. Alan adları analiz servisine gönderilmez. Gerçek API bağlantısı, kullanıcı oturumu ve canlı raporlama bu tasarım çalışmasına eklenmemiştir. Rehber otomatik teşhis veya sıralama garantisi sunmaz. Ana sayfanın footer tasarımı sonraki aşamadır.

Chromium/Playwright kontrol kapsamı: iki sayfada 320–1440 piksel arası görünüm, daralan header, tema seçimi, form, sekmeler, grafik etkileşimi, araç kartları ve ayrıntı pencereleri, yükleyicinin kapanması ve atlanması, telefon kaydırıcısı, kontrol listesi ve soru-cevaplar. Ekran görüntüleri iki kat piksel yoğunluğunda `/workspace/artifacts` altında üretilir. Son kontrol sonuçları ilgili çalıştırmanın çıktısından değerlendirilmelidir.

## Paylaşım ve önizleme

Kaynaklar herkese açık [sahinizgiseo/depo](https://github.com/sahinizgiseo/depo) deposunun `main` dalında paylaşılır. İndirilebilir paket [bu HTTPS adresinden](https://raw.githubusercontent.com/sahinizgiseo/depo/main/indir/asilserp-tasarim.zip) sunulur. Güncel ZIP, kök ajan tarafından kontrol ve yayın adımında yeniden oluşturulur.

Bu bulut arayüzünde canlı localhost önizlemesi desteklenmez. Alternatif `raw.githack.com` önizleme bağlantıları paylaşılmıştır; CDN bu yürütme ortamında 403 ağ engeline takıldığı için burada açılarak doğrulanamamıştır. GitHub Pages etkin değildir: oluşturma API'si entegrasyon yetkisi için 403 döndürmüştür. Depoya kaynak yüklemek ile çalışan bir web önizlemesini doğrulamak ayrı durumlardır.

Üretim `asilserp.com` sitesi bu prototiple değiştirilmemiştir. Tasarım çalışması devam etmektedir.
