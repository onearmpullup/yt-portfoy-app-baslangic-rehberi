# Buradan başla

Kod bilmen gerekmiyor. Bu kit hazır bir uygulama değil; AI ile kendi ihtiyacını belirleyip uygulamanı küçük adımlarla geliştirmen için bir rehber. İlk hedef sadece **sana uygun bir plan** çıkarmak.

**Gerekenler:** Bir bilgisayar, internet ve kullanabildiğin bir AI yardımcısı. İkisini birden kullanmana gerek yok; Codex veya Claude Code yeterli. Henüz bunlara erişimin yoksa planı normal bir AI sohbetinde hazırlayabilirsin. AI aracının kendi ücretleri olabilir; bu kit için ayrıca API anahtarı alman gerekmiyor.

## 1. AI'a vereceğin metni kopyala

1. [AI-ILE-PORTFOY-TASARLA.md dosyasına tıkla](AI-ILE-PORTFOY-TASARLA.md). `.md`, burada yalnızca bir metin dosyası demek.
2. GitHub'da dosyanın üstündeki **Raw** düğmesine bas. Rehber düz yazı olarak açılacak.
3. Windows'ta `Ctrl+A` ile tamamını seç, `Ctrl+C` ile kopyala. Mac'te aynı işlem `⌘A` ve `⌘C`. Dosya zaten bilgisayarındaysa bir metin düzenleyicide açıp içeriğini kopyalayabilirsin.

## 2. Yeni bir sohbet aç ve gönder

Codex veya Claude Code'da yeni bir sohbet aç. Kopyaladığın metni `Ctrl+V` / `⌘V` ile mesaj kutusuna yapıştır. **Göndermeden önce sonuna şunu ekle:**

> Önce benim ihtiyaçlarımı öğren; her turda en fazla 3–4 ilgili soru sor. Kendi portföy takip uygulamamı planlayalım. Şimdilik kod yazma. API anahtarım ve bütçem yoksa manuel ve sentetik veriyle başlayalım.

Sonra mesajı gönder. Araç sohbet açmadan önce bir proje klasörü istiyorsa aşağıdaki 4. bölümün ilk iki adımını yap; yine yalnızca plan isteyen mesajla başla.

## 3. Soruları günlük dille yanıtla

Örneğin: “İki fon takip ediyorum. Şu an deftere yazıyorum. Ayda bir güncelleyeyim, bilgisayarımda bir tablo göreyim. Haber veya chatbot istemiyorum.”

Kesin tutar, hesap numarası, parola veya API anahtarı paylaşma. AI'ın senden ihtiyacını öğrenmesini, ilk sürümde yapılacak bir veya iki işi seçmesini ve nasıl kontrol edeceğini anlatmasını bekle. Anlamadığın terim olursa “Bunu teknik olmayan birine anlatır gibi açıkla” de. [Üç örnek ihtiyaç](ORNEK-IHTIYACLAR.md) fikir verebilir; birini aynen seçmek zorunda değilsin.

## 4. Plan hazırsa geliştirmeye geç

1. Bilgisayarında **Portfoyum** adında yeni, boş bir klasör oluştur. Klasör, uygulamanın dosyalarının duracağı yer. Windows'ta Dosya Gezgini'ni, Mac'te Finder'ı kullanabilirsin. Belgelerinin tamamını veya gerçek finansal dosyalarının olduğu klasörü seçme.
2. Bu klasörü kodlama aracında aç: **Codex masaüstünde** yerel projene klasör olarak ekle; **Claude Desktop'ta** `Code` bölümünde `Local` ortamını ve bu proje klasörünü seç. Menülerin adı sürüme göre değişebilir; alttaki resmî yardım bağlantılarını kullan. Terminal komutu yazmak bu yolun şartı değil.
3. Yeni bir sohbete geçtiysen rehber metnini ve üzerinde anlaştığınız planı yeniden ekle. AI'ın önceki sohbetini kendiliğinden bildiğini varsayma. Ardından şunu gönder:

> Üzerinde anlaştığımız planın ilk çalışan bölümünü sadece seçtiğim Portfoyum klasöründe oluştur. Tamamen uydurma örnek kayıtlar kullan; gerçek hesaplarıma bağlanma. Gerekli kontrolleri sen çalıştır; çalıştıramadıklarını açıkça yaz. Bana sonucu nasıl açacağımı adım adım anlat. Ek program gerekirse ne olduğunu ve neden gerektiğini önce açıkla. Henüz internette yayınlama veya ücretli hizmet açma.

İlk bölüm çalışınca örnek bir kayıt ekle, değiştir ve sayfayı yenile. Sonraki bölüme bunları gördükten sonra geç. Bir hata olursa özel bilgi içermeyen hata mesajını AI'a gönder; “Ne yapacağımı tek adım halinde söyle” diyebilirsin. AI dosya oluşturamıyor veya test çalıştıramıyorsa bunu açıkça belirtmeli; yalnızca sohbet yanıtı, çalışan uygulama sayılmaz.

## Takılırsan

- **AI bağlantıyı okuyamıyor:** Bağlantı yerine 1. adımdaki metnin tamamını yapıştır.
- **Nereden klasör seçeceğini bulamıyorsun:** Kullandığın aracı ve Windows/Mac bilgisayarını söyleyip menü için yardım iste. Parola veya anahtar gönderme.
- **Skill kurulumunu anlamadın:** Atlayabilirsin. Yukarıdaki yol skill kurmadan çalışır; skill, rehberi tekrar kullanmayı kolaylaştıran isteğe bağlı bir özelliktir.

Resmî yardım (11 Ekim 2026'da kontrol edildi): [GitHub'da metni açma/kopyalama](https://docs.github.com/en/repositories/working-with-files/using-files/viewing-and-understanding-files), [Codex'te yerel proje klasörleri](https://learn.chatgpt.com/docs/projects), [Claude Code masaüstü kullanımı](https://code.claude.com/docs/en/desktop).

[Ana rehberde](README.md) isteğe bağlı skill kurulumu var. Bir günde bitmiş uygulama, ücretsiz kullanım veya hatasız finansal veri garantisi yoktur. İlk denemelerini uydurma kayıtlarla yap; gerçek veriye geçmeden hesaplama ve yedekten dönüş kontrollerini tamamla.

Kitin kullanım ve paylaşım koşulları [MIT lisansında](LICENSE) yer alır.
