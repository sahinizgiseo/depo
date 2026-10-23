# Asilserp — tasarım çalışması 04

Asilserp SEO platformu için bağımlılıksız HTML/CSS/JavaScript tasarım prototipi. İki sayfa vardır:

- `index.html`: kaydırmada küçülen header, açılış ekranı, etkileşimli platform paneli ve kayan beş telefon ekranı.
- `trafigim-dusuyor/index.html`: dokuz adımlı trafik kaybı rehberi, kayıtlı kontrol listesi, bölüm bağlantıları ve yedi soru-cevap.

## Çalıştırma

Dosyaları aynı dizin yapısında tutarak `index.html` dosyasını tarayıcıda açın veya:

```sh
cd /workspace/depo
python3 -m http.server 4173 --bind 127.0.0.1
```

Paket kurulumu ve derleme gerekmez. Logo ve Manrope fontları HTML içine gömülüdür; çalışma sırasında harici font veya CDN isteği yapılmaz. İki sayfa da koyu, açık ve lacivert görünümleri destekler. Seçim tarayıcıda hatırlanır.

## Davranışlar

Header 72 piksel kaydırmadan sonra küçülür; üstüne gelince küçülmez. Üste dönünce eski boyutuna gelir. Mobil menü ve Escape ile kapatma çalışır. Dış kapsayıcının yüksekliği sabittir.

Alan adı formu girdiyi doğrular ve açıkça etiketlenmiş örnek raporu açar. Platformun dört sekmesi, klavye okları/Home/End, 30/90 gün kontrolleri ve fırsat pencereleri çalışır. Örnek teknik denetim kapsamı en fazla 100 sayfadır.

Telefon ekranları HTML/CSS ve SVG ile çizilmiştir. Yatay kaydırma, dokunma, fareyle sürükleme, ok düğmeleri, klavye ve durdurma düğmesi desteklenir. Otomatik ilerleme yalnızca bölüm görünürken çalışır; kullanıcı etkileşiminde, odakta, fare üzerinde, gizli sekmede ve hareketi azaltma tercihinde durur. Ekranlar mobil web tasarım önerisidir; yayımlanmış bir mobil uygulama değildir.

Trafik kaybı rehberindeki kontrol listesi `asilserp-traffic-guide-v1` anahtarıyla yalnızca bu tarayıcıda saklanır; hesap senkronizasyonu yoktur. İşaretleri temizleme, ilerleme yüzdesi ve etkin bölüm göstergesi çalışır. Depolama kapalıysa sayfa içindeki işaretleme çalışmaya devam eder.

Kullanıcının sağladığı Uiverse tarzı CSS örnekleri, turuncu/lacivert ışık çerçevesi ve hafif Matrix animasyonu olarak uyarlanmıştır. Ana sayfadaki hareket kontrolü ve işletim sisteminin hareketi azaltma tercihi desteklenir.

## İçerik ve kaynaklar

- Asilserp'in mevcut sitesi bu çalışma sırasında okunmuştur. Rehberdeki araç kapsamı alan adı analizi, organik sıralamalar, en iyi sayfalar ve HTML site denetimine dayanır. Denetim en fazla 100 sayfa; JavaScript çalıştırma, performans testi veya tam site taraması içermez.
- Panel ve fiyat bağlantıları mevcut `https://asilserp.com/customer-login` ve `https://asilserp.com/fiyatlar` adreslerine gider.
- `https://semust.com/trafigim-dusuyor` dokuz adımlı rehber yapısı için referanstır. Asilserp sürümünün metinleri ve görselleri özgün hazırlanmıştır; Semust'a özgü ürün özellikleri aktarılmamıştır.
- Header davranışı kullanıcının `agent-magicui.vercel.app` referansı ve kaydırmada küçülme açıklamasına dayanır.
- Kullanılan logo mevcut `https://asilserp.com/asilserp-logo.png` adresinden alınmıştır: `assets/asilserp-logo-official.png`. Önceki fotoğraf uyarlaması `assets/asilserp-logo.png` olarak korunur, artık gösterilmez.
- Fontlar: Manrope Variable, Latin ve Latin-ext. Font dosyaları ve SIL Open Font License metni `assets/fonts/` altındadır. Türkçe karakterler desteklenir.

## Kapsam ve doğrulama

Bütün panel ve telefon verileri örnektir. Alan adları analiz servisine gönderilmez. Gerçek API bağlantısı, kullanıcı oturumu ve canlı raporlama bu tasarım çalışmasına eklenmemiştir. Rehber otomatik teşhis veya sıralama garantisi sunmaz. Ana sayfanın footer tasarımı sonraki aşamadır.

Chromium/Playwright ile iki sayfada 320–1440 piksel arası görünüm, daralan header, tema seçimi, form, sekmeler, telefon kaydırıcısı, kontrol listesi ve soru-cevap etkileşimleri kontrol edilir. Ekran görüntüleri iki kat piksel yoğunluğunda `/workspace/artifacts` altında üretilir.

Bu bulut arayüzünde canlı localhost önizlemesi desteklenmez. Çalışma dosyalarını ve ekran görüntülerini inceleyebilirsiniz; sunucu yalnızca yerel doğrulama içindir. Değişiklikler üretim sitesine yayımlanmamıştır.
