# Üç farklı ihtiyaç, üç farklı ilk sürüm

Bu kişiler, hesaplar ve senaryolar tamamen sentetiktir. Bunlar öneri örnekleridir; gerçek kullanıcı hikâyesi, hazır şablon zorunluluğu veya yatırım önerisi değildir. Aynı özellik listesini herkese uygulamamak için hazırlanmıştır.

## Ada — İki fonu ayda bir takip etmek

**İhtiyaç:** Banka ekranları arasında dolaşmak yerine pay adetlerini ve son bilinen toplamı tek yerde görmek. Şu an defter kullanıyor. İki yerli fon, tek hesap, TL raporlama; manuel aylık giriş yeterli. Teknik deneyimi, API anahtarı ve API/barındırma bütçesi yok; ayda yarım saat bakım ayırabilir. Bilgisayarında sade bir tablo istiyor. Yalnızca plan talep ediyor.

**Seçilenler:** Fon kimliği/pay sınıfı, pay adedi, tarihli manuel birim fiyat, isteğe bağlı bilinen maliyet, yerel saklama, JSON dışa aktarma. İlk iki iş: kaydı güncellemek ve ay sonunda toplamı görmek.

**İlk sürüm planı:**

1. İki uydurma fonla tek tablo ve toplam tasarla; fiyat tarihini ve bilinmeyen maliyeti göster.
2. Geliştirme yetkisi geldiğinde kayıt/yenileme ve boş alana geri yükleme ekle.
3. Sentetik olarak 40 pay × 12,50 TL = 500 TL; diğer fonun fiyatı yoksa “bilinen toplam 500 TL, 1 eksik fiyat” göster. Eksik varlığı sıfır diye sunma.

**Ertelenenler:** Canlı fiyat, banka bağlantısı, haber, chatbot, üyelik, yabancı para ve karmaşık getiri grafiği. Önce aylık rutin işe yarasın. API'siz olması AI aracının ücretini kaldırmaz. Yalnızca plan istendiği için bu örnekte kod yazma aşamasına geçilmez.

## Bora — Yabancı hisse, ETF ve kriptoyu birlikte görmek

**İhtiyaç:** Bir CSV dosyası ile iki kurumun kayıtları uyuşmuyor. ABD hissesi/ETF ve belirli iki kripto kimliği; USD ve EUR hesaplar, TL raporlama. Temel teknik deneyim; haftada bir saat bakım ve kendi belirleyeceği küçük ücretli kaynak bütçesi var. Önce bilgisayarında çalışacak. Fiyatların gün sonunda gelmesi yeterli. Haber istemiyor; sonradan “bu ay ne değişti?” diye salt okunur sohbet istiyor. Geliştirme talep ediyor.

**Seçilenler:** Hesaplar, doğru listeleme/kripto kimliği, CSV önizleme, ücretli alış/satış kaydı, işlem kuru ile güncel kur ayrımı, nakit, dışa aktarma. İlk iki iş: aktarımın mükerrer olmaması ve çok para birimli toplamın anlaşılması. Sade dağılım + hesap listesi; grafik ilk zorunluluk değil.

**İlk sürüm planı:**

1. İki hesaba ait sentetik CSV ile kimlik ve para birimi eşlemesini önizlet.
2. Kayıt, tekrar aktarım, düzeltme ve hesapları bitir; [döviz senaryosundaki](skills/kisisel-portfoy-gelistirme/references/KABUL-KONTROLLERI.md) 102 USD maliyet / 120 USD değer ile tarihli TL sonuçlarını doğrula.
3. İlgili listeleme ve token için resmî kapsam/hak/bütçe doğrulanınca gün sonu kaynak ekle; o zamana kadar manuel fiyatla çalıştır.
4. Bu işler geçtikten sonra, açık veri paylaşımı ve bütçeyle salt okunur sohbet eklenebilir. Sohbetin kayıt değiştirme yetkisi yoktur.

**Ertelenenler:** Genel haber akışı, otomatik banka oturumu, gerçek emir, çevrimiçi üyelik ve tahmin modelleri. Tüm kriptolara destek sözü verilmez. Genel geliştirme izni, ücretli aboneliği kendiliğinden açma izni değildir.

## Cemre — Emeklilik ve metal birikimini telefonda izlemek

**İhtiyaç:** İki farklı kurumun emeklilik beyanları ve gram metal kaydı ayrı notlarda. Teknik deneyimi yok; ayda bir güncelleme, kurulum sonrası az bakım istiyor. TL raporlama; emeklilikte kurumun tarihli toplamı, metalde manuel gram/fiyat. Telefonunda çevrimiçi erişim istiyor; barındırma bütçesi kararını seçenekleri görünce verecek. Özet kartları ve aylık karşılaştırma istiyor. İlgili resmî haber bağlantıları ikinci sürüm olabilir; chatbot istemiyor.

**Seçilenler:** Kurumdan bağımsız emeklilik toplam beyanı, devlet katkısı dahil/dahil değil bilgisi, metal birimi, yedek. İlk iki iş: aylık beyanı kaydetmek ve aynı tutarı iki kez saymadan toplamı görmek.

**İlk sürüm planı:**

1. Emeklilik toplamlarını detay fon kaydı gerektirmeden modelle; bilinmeyen hak edişi hesaplama. Sentetik bir beyanın katkı dahil 20.000 TL olduğunu doğrula: sonuç 23.000 TL olmamalı.
2. Önce yerel sentetik prototip, ardından saklama ve yedekten dönüş; telefona uygun büyük kontroller. Yeterli tarih birikince aylık değer grafiği; bunun yatırım getirisi olmadığını açıkla.
3. Çevrimiçi bütçe ve yayın yetkisi netleşince kimlik doğrulama, özel kayıt erişimi ve iki sentetik kullanıcıyla test ortamı kontrolleri; sonra kontrollü kişisel kullanım.
4. İstenirse ikinci sürümde kaynak/tarihi açık resmî bağlantı listesi; zorunlu AI haber özeti yok.

**Ertelenenler:** Banka/kurum parolalarıyla bağlantı, fon bazlı detay muhasebesi, vergi/hak ediş motoru, chatbot ve herkese açık üyelik. Tek bir emeklilik markasına bağlı model kurulmaz.

## Neyi değiştirmiş olduk?

Ada'da veri kaynağı manuel ve arayüz tablo; Bora'da öncelik kimlik/kur/aktarım; Cemre'de toplam beyan, mobil kullanım ve çevrimiçi gizlilik. Modüller, testler, teknik seçimler ve bakım maliyeti bu farklara göre değişir. Hiçbirinde “başka birinin dashboard'unu aynen yap” gereği yoktur.
