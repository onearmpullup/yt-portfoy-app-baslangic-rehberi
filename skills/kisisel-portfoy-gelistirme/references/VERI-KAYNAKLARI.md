# Veri kaynağını ihtiyaca göre seç

Bu bir “en iyi API” listesi değil, karar kontrolüdür. Otomatik kaynak zorunlu değildir. Manuel tarihli fiyatla başlamak geçerli bir ilk sürümdür. Aşağıdaki ölçütler genel öneridir; belirli sağlayıcının sözleşmesi veya kapsam garantisi değildir.

## Önce varlık ve kullanım

| İhtiyaç | Seçimden önce doğrulanacak ayrıntı |
| --- | --- |
| Hisse / ETF | Tam listeleme, borsa, sembol, para birimi; ETF pay sınıfı; bölünme/temettü düzeltmeli mi, ham fiyat mı? |
| Yatırım fonu | ISIN veya kurum kodu, doğru pay sınıfı, birim pay değeri ve değerleme günü; işlem günüyle yayın günü farklı mı? |
| Döviz / nakit | Kur yönü, alış/satış/orta kur; referans mı gerçekleşmiş işlem kuru mu; tatilde son fiyat davranışı |
| Metal | Gram/ons, saflık, para birimi; spot gösterge mi bankanın gerçekleşmiş fiyatı mı? |
| Kripto | Sağlayıcı kimliği, gerekiyorsa ağ/kontrat ve fiyatlanan çift; aynı sembol farklı token olabilir |
| Emeklilik | Kurum toplam beyanı mı fon detayı mı; devlet katkısı dahil mi; tarih; hak ediş bilgisi gerçekten mevcut mu? |
| Tahvil / diğer | Kupon, vade, nominal, temiz/kirli fiyat gibi ayrıntılar gerekli mi? Yetersiz modelde tam hesap desteği vaat etme; açıkça sınırlı manuel takip veya kapsam dışı seç. |

## Kaynak karar kartı

Her aday için şu kısa kaydı doldur; bilinmeyen alanı boş bırakmak yerine “doğrulanmadı” yaz:

- İstenen **tam varlık kimliği** ve alanlar; örnek yanıtla eşleşme kanıtı.
- Resmî belge URL'si, kontrol tarihi ve kullanılan plan/hesap türü.
- Kaynak fiyat zamanı, çekilme zamanı, saat dilimi, gecikme ve tatil davranışı.
- Tarihçe kapsamı ve düzeltmeler; güncel fiyat ile tarihçe aynı anlamda mı?
- Kota birimi: çağrı, sembol, kredi veya veri noktası mı? Toplu istek ve başarısız tekrarlar nasıl sayılıyor?
- Maliyet: AI aracı, fiyat API'si, haber/AI çağrıları, barındırma ve saklamayı ayrı değerlendir. Hesaba özgü koşulları kontrol et.
- Kişisel gösterim, önbellekleme, tarihçe saklama, başkalarına sunma ve yeniden dağıtım hakları; atıf şartı. Genel doküman aboneliğin yetkisini kanıtlamaz.
- Anahtar nerede tutulacak? Hangi veri dışarı gönderilecek? Kim erişebilecek?
- Kesintide davranış: tarihli son fiyat, açık eksiklik veya manuel giriş. Yeni kaynağa geçerken birim/anlam aynı mı?

Kullanıcıdan API anahtarını sohbete yapıştırmasını isteme; izin verilen araçların güvenli sır giriş yolunu kullan. Kaynak okuyamıyorsan kota/fiyat/hak tahmin etme. Açık yetki olmadan deneme için ücretli plan açma veya erişim engelini aşma.

## Güncelleme politikasını yaz

“Canlı” kelimesinden önce kabul edilebilir gecikmeyi sor. Aylık fon takibine saniyelik istek gerekmez. Önbellek, toplu istek, sınırlı yeniden deneme ve başarısızlığı gösteren durum seç. Uygunluk kontrolü: pozitif/sayısal değer, doğru birim, geçerli tarih, tekrarlı gözlem, aşırı büyük yanıt ve zaman aşımı.

Haber seçilmişse ayrı karar ver: kaynak URL'si, yayın tarihi, portföyle ilgi nedeni, alıntı/özet hakkı ve model yorumunun etiketi. Resmî duyuru ile gazetecilik yorumu aynı kategori değildir. Yalnızca erişilebilen/izin verilen alanları kullan; kaynağın yokluğunu uydurma başlıkla kapatma.

## Resmî başlangıç bağlantıları

11 Ekim 2026'da aşağıdaki dokümantasyon sayfalarına erişim kontrol edildi:

- [CoinGecko API belgeleri](https://docs.coingecko.com/): kripto aday kaynağını araştırmak için.
- [Metals.Dev API belgeleri](https://metals.dev/docs): metal birimi ve kotasyon alanlarını araştırmak için.

Bu iki bağlantı önerilen zorunlu tedarikçi veya her varlığa destek kanıtı değildir. Güncel fiyat/ücretsiz kota rakamı aktarılmadı; kullanıcının seçtiği planda maliyet, haklar ve tam kimlik kapsamı **henüz doğrulanmış değildir**. Fon için ilgili fon/kurumun resmî belgelerini, hisse için seçilen piyasa/veri lisansı belgelerini, döviz için seçilen resmî kaynak ve kullanım şartlarını karar kartına ekle. Bir fiyat uç noktasının çalışması, yayına veri dağıtma izni vermez.
