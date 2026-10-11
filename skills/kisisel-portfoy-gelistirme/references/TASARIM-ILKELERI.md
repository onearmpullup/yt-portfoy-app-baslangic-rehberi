# Portföy takibi için tasarım ilkeleri

Buradaki maddeler genel geliştirme önerileridir; belirli bir kişinin verilerini, bir ürünün özelliklerini veya doğrulanmış başarı hikâyesini anlatmaz. Çözümü kullanıcının ihtiyacına göre daralt. Kayıt tutabilmek, doğru hesaplayabilmek ve otomatik fiyat alabilmek ayrı yeteneklerdir.

## 1. Varlığı doğru tanımla

**Risk:** Aynı sembol farklı borsada, pay sınıfında veya kripto ağında başka bir varlık olabilir.

**Yaklaşım:** Gerekli olduğunda sembol + piyasa + para birimi, fon pay sınıfı, sağlayıcı kimliği veya metal birimini sakla. Fiyatı doğrulanmış kimliğe bağla; belirsiz eşlemeyi kullanıcıya sor.

**Sınır:** İki manuel fon için küresel bir varlık kataloğu kurmak gerekmeyebilir. Bunun yerine seçilen iki fonun kimliğini ve birim pay anlamını açık tut. Her ülke veya varlık için otomatik kapsam varsayma.

## 2. Fiyatın zamanını ve anlamını göster

**Risk:** Yeni çekilmiş eski bir fiyat “canlı” sanılabilir. Gram ile ons veya bankanın satış fiyatı ile spot gösterge karışabilir.

**Yaklaşım:** Kaynak fiyat zamanı, çekilme zamanı, para birimi, birim ve gecikmeyi ayrı taşı. Manuel fiyatın tarihini de koru. Kurun yönünü belirt; tarihli işlem kuru ile güncel gösterim kurunu ayır.

**Sınır:** Tek para birimli kullanımda döviz servisi gerekmeyebilir. Gerçek alış/satış kuru yoksa referans kurdan kesin gerçekleşmiş kâr üretme.

## 3. Maliyet, piyasa değeri ve nakdi ayır

**Risk:** İşlem tutarı ile güncel değer eşit sanılabilir; ücret iki kez düşülebilir; para yatırmak kazanç görünebilir.

**Yaklaşım:** Maliyet yöntemini, ücretlerin işlenmesini, nakit akışlarını ve getiri tanımını yazılı seç. Ekranları ortak hesap katmanından besle. Bilinmeyen maliyeti sıfır sayma. Dış katkıyı yatırım sonucundan ayır.

**Sınır:** Sadece toplam beyanı bulunan hesapta ayrıntılı gerçekleşmiş kâr veya TWR/XIRR iddia etme. Portföy takibi otomatik olarak vergi muhasebesi değildir.

## 4. Eksikliği dürüstçe göster

**Risk:** Eksik fiyat sıfırmış gibi toplanırsa grafik sahte zarar gösterebilir. Geçmişi doldurmak için uydurulmuş eğri gerçek performans sanılabilir.

**Yaklaşım:** Bilinen toplamı ve fiyat kapsamını birlikte göster. Eksik/eski fiyatı işaretle. Tarihsel hesapta yalnızca o tarihte geçerli kayıtları kullan. Sentetik geçmişi gerçek veriden ayır; boşluğu gizleyen kesintisiz çizgi üretme.

**Sınır:** Eksik noktaları filtrelemek tek başına doğru performans hesabı oluşturmaz; tarihli fiyat/kur ve nakit akışı gerekebilir. Kullanıcı aylık kontrol istiyorsa gün içi grafik zorunlu değildir.

## 5. Hesap ve portföy grubunun kapsamını açıkla

**Risk:** Ortak hesap nakdi birkaç portföye dağıtılıp mükerrer sayılabilir.

**Yaklaşım:** Hesabın nerede saklanan para/varlık olduğunu, portföy grubunun hangi yatırımları kapsadığını belirle. Nakit tahsisi tutulmuyorsa ortak nakdi genel görünümde gösterip seçili grupta neden hariç olduğunu açıkla.

**Sınır:** Gerçek alt hesap veya cüzdan bazlı tahsis varsa nakit portföye atanabilir. Tek bir gruplama modeli herkese uygun değildir.

## 6. Emeklilik toplamını iki kez sayma

**Risk:** Kurum toplamıyla fon detayları veya zaten dahil devlet katkısı birlikte eklenebilir.

**Yaklaşım:** Toplam beyan ve detaylı fon takibi arasında açık bir değerleme modu seç. Devlet katkısının toplamda olup olmadığını ve beyan tarihini kaydet. Bir modu diğerine geçirirken farkı göster.

**Sınır:** Hak ediş, kesinti veya vergi bilgisi yoksa bunları hesaplıyor gibi görünme. Kurumdan bağımsız tasarla; ilk sürümde ayrıntılı fon motoru zorunlu değildir.

## 7. Haber kaynağı ile yorumu ayır

**Risk:** Modelin yorumu kaynaktaki kesin bilgi veya kişiye özel gerçek gibi sunulabilir.

**Yaklaşım:** Kaynak bağlantısı, yayın tarihi, yayıncı ve portföyle ilişki nedeni görünür olsun. Olgu, kaynaklı yorum ve model çıkarımını etiketle. Kaynak yoksa içerik uydurma; ortak haber işlemek için özel portföyü gereksiz yere dışarı gönderme.

**Sınır:** Haber istemeyen kullanıcıya modül ekleme. Kamuya açık erişim veya robots izni tek başına yeniden yayın hakkı değildir.

## 8. Chatbot açıklasın, kayıt sistemi doğrulasın

**Risk:** Akıcı yanıt yanlış miktar, hesap veya tarih gizleyebilir. “Sattım” ifadesinde gelir veya ücret eksik olabilir.

**Yaklaşım:** Güncel gerekli bağlamı kullan; sayıları hesap motorundan al. Eksikleri sor; önce/sonra etkisini göster; kullanıcı onayıyla kaydet. Yazarken yetkiyi ve bakiyeyi yeniden doğrula. Aynı onayı tek kayda bağlayan kimlik ve izlenebilir düzeltme yolu kullan. Ağ sonucu belirsizken kesin başarısızlık ilan etme.

**Sınır:** Salt okunur sohbet için yazma yetkisi gerekmez. Miktarı sıfırlayan mutabakat veya arşivleme satış değildir; fiyat bilinmiyorsa nakit/kâr uydurulmaz. Gerçek banka emri kapsam dışıdır.

## 9. Gizliliği kullanım ortamına göre kur

**Risk:** Tek kullanıcı varsayımı çevrimiçi kullanımda veri veya anahtar karışmasına yol açabilir.

**Yaklaşım:** Sırları sohbet, tarayıcı paketi, Git ve loglardan uzak tut. Sunuculu yapıda kayıt sahipliği/yetkiyi sunucuda kontrol et; sohbet, özel cache ve anahtarları kullanıcıya göre ayır. Şifreli saklamanın kimlerin erişimini engellediğini açıkla. Yerel cihazda da yedek ve cihaz güvenliği gerekir.

**Sınır:** API'siz yerel uygulamaya çok kullanıcılı kasa eklemek gereksiz olabilir. İnternette “sadece arkadaşım kullanacak” demek yetki kontrollerini kaldırmaz. Yerel test canlı iki kullanıcı kontrolü yerine geçmez.

## 10. Kota, maliyet ve kurtarmayı tasarımın parçası yap

**Risk:** Kullanıcı/varlık sayısı, güncelleme sıklığı ve tekrarlar arttıkça tüketim artabilir. JSON indirmek tam sistem yedeği sanılabilir.

**Yaklaşım:** İstekleri önbellekle ve tekrarları sınırla; ücretli kullanım bütçesini açık seç. Güncel fiyat, kota ve veri hakkını resmî kaynaktan kontrol et. Dışa aktarma kapsamını/şemasını yaz; ayrı boş test alanında geri yüklemeyi dene ve sonuçları karşılaştır.

**Sınır:** Uygulama içi tahmini sayaç kesin sağlayıcı fatura tavanı değildir. Yapısal JSON kontrolü bütün sistemin kurtarılabildiğini kanıtlamaz. Manuel başlayıp entegrasyonları ertelemek geçerli bir tercihtir.
