# AI ile Portföy Geliştirme Kiti

Kendi ihtiyaçlarına uygun bir kişisel portföy takip uygulamasını AI ile **planlamak, küçük adımlarla geliştirmek ve test etmek** için Türkçe başlangıç rehberi ve skill paketi.

Bu depo hazır bir uygulama veya belirli bir ürünün kopyası değildir. Önce hangi sorunu çözmek istediğini belirler; sonra varlıklarını, veri girişini, ekranlarını ve teknik seçeneklerini buna göre seçersin. Haber, chatbot, otomatik fiyat ve çevrimiçi üyelik zorunlu değildir. Bütçen veya API anahtarın yoksa manuel ve sentetik verilerle başlayabilirsin.

## İlk kez kullanıyorsan buradan başla

GitHub burada yalnızca rehberin bulunduğu yer. Başlamak için kod yazmayı, terminal kullanmayı veya Git komutlarını bilmene gerek yok. Skill, AI'a tekrar kullanabileceği talimatlar veren bir klasördür; şimdilik onu kurmana gerek yok.

1. [AI'a verilecek rehberi aç](AI-ILE-PORTFOY-TASARLA.md). GitHub'da dosyanın üstündeki **Raw** düğmesine bas; düz metin açılır. Windows'ta `Ctrl+A`, ardından `Ctrl+C`; Mac'te `⌘A`, ardından `⌘C` ile tamamını kopyala.
2. Codex veya Claude Code'da yeni bir sohbet aç. Metni mesaj kutusuna yapıştır; **göndermeden önce sonuna aşağıdaki mesajı ekle**. Henüz kodlama aracın yoksa ilk planı kullandığın AI sohbetinde hazırlayabilirsin; dosya oluşturmak ve test etmek için daha sonra bir kodlama aracı gerekir.
3. Mesajı gönder ve AI'ın sorularını günlük dille yanıtla. Gerçek bakiye, parola veya API anahtarı paylaşma. İlk sonuç, sana uygun küçük bir uygulama planı olacak; henüz bitmiş uygulama değil.

> Bu talimata göre benimle Türkçe ilerle. Önce ihtiyaçlarımı öğren; her turda en fazla 3–4 ilgili soru sor. Bana özel bir portföy takip uygulaması planlayalım. Şimdilik sadece plan istiyorum, kod yazma. Bütçe veya API anahtarı gerektirmeyen başlangıç seçeneğini de açıkla.

Bir cevap örneği: “İki fon takip ediyorum, ayda bir güncellemek istiyorum. Bilgisayarımda çalışsın; şimdilik haber ve chatbot istemiyorum.”

Planı beğendikten sonra **[adım adım başlangıç sayfasındaki](BASLA.md) “Plan hazırsa geliştirmeye geç” bölümünü izle**. Orada boş klasör oluşturma, Codex/Claude Code'a açma ve ilk geliştirme mesajı anlatılıyor. Bu kiti indirmek veya GitHub hesabını AI'a bağlamak zorunlu değil; metni kopyalamak yeterli. Kullandığın AI aracının erişimi ücretli olabilir.

Bağlantı vererek başlamayı tercih edersen AI'dan bu depodaki `AI-ILE-PORTFOY-TASARLA.md` dosyasını okumasını iste. Erişemiyorsa yukarıdaki kopyala-yapıştır yolunu kullan. Repo bağlantısı vermek tek başına skill kurmaz.

## İsteğe bağlı: skill'i kendi projenize ekleme

Bu bölüm yerel proje klasörüyle çalışan **Codex CLI / IDE eklentisi** ve **Claude Code** içindir. Skill hesabına otomatik kurulmaz; dosyalar seçtiğin projeye eklenir. Web, masaüstü ve kurumsal politikalar farklı olabilir. İlk yol bunlara bağlı değildir.

Önce [skill talimatını](skills/kisisel-portfoy-gelistirme/SKILL.md) gözden geçir. Depodaki `skills/kisisel-portfoy-gelistirme` klasörünü, `references` alt klasörüyle birlikte kopyala:

| Araç | Kendi projenizde hedef dosya | Çağırma |
| --- | --- | --- |
| Codex CLI / IDE | `.agents/skills/kisisel-portfoy-gelistirme/SKILL.md` | `$kisisel-portfoy-gelistirme` veya `/skills` |
| Claude Code | `.claude/skills/kisisel-portfoy-gelistirme/SKILL.md` | `/kisisel-portfoy-gelistirme` |

Klasörü kendi projenin kökünden itibaren yerleştir; yalnızca `SKILL.md` dosyasını taşımak bağlı kaynakları eksik bırakır. Aynı adlı skill varsa üzerine yazmadan karşılaştır/yedekle. Codex'te görünmüyorsa yeniden başlat; Claude Code'da hedef projede yeni oturum aç. Bu adımlar skill'i taşır, uygulama kurmaz.

Yollar ve çağırma biçimleri 11 Ekim 2026'da [OpenAI skill belgesi](https://learn.chatgpt.com/docs/build-skills) ve [Claude Code skill belgesi](https://code.claude.com/docs/en/skills) üzerinden kontrol edildi. Kurulum senin ortamında ayrıca doğrulanmalıdır. Bu repo bir plugin/marketplace veya tek tıklamalı otomatik kurucu içermez. Yerel kopya güncellemeleri kendiliğinden almaz; yeni sürümde değişiklikleri inceleyip bilinçli olarak güncelle.

## Kit neler içeriyor?

- [BASLA.md](BASLA.md): kısa başlangıç.
- [AI-ILE-PORTFOY-TASARLA.md](AI-ILE-PORTFOY-TASARLA.md): tek başına kullanılabilen çalışma talimatı.
- [ORNEK-IHTIYACLAR.md](ORNEK-IHTIYACLAR.md): üç farklı, tamamen sentetik ihtiyaç ve ilk sürüm planı.
- [SKILL.md](skills/kisisel-portfoy-gelistirme/SKILL.md): aynı iş akışının yeniden kullanılabilir sürümü.
- [Tasarım ilkeleri](skills/kisisel-portfoy-gelistirme/references/TASARIM-ILKELERI.md): veri, hesap, kapsam ve güvenlik kararları.
- [Veri kaynakları](skills/kisisel-portfoy-gelistirme/references/VERI-KAYNAKLARI.md): sağlayıcı seçimi ve doğrulama ölçütleri.
- [Kabul kontrolleri](skills/kisisel-portfoy-gelistirme/references/KABUL-KONTROLLERI.md): elle de kontrol edilebilen sentetik testler.
- [Sürüm notları](SURUM-NOTLARI.md): doğrulama kapsamı ve sınırlamalar.

## Sınırlar ve gizlilik

Bu kit gerçek kişilerin kayıtlarını, hesaplarını, anahtarlarını veya bir uygulamanın kaynak kodunu içermez. Örnekler sentetiktir. Sen de gerçek hesap parolalarını, API anahtarlarını ve özel finansal dökümlerini sohbetlere veya public depolara koyma. Röportaj için kesin bakiye gerekmez.

Bir günde bitmiş ürün, sıfır maliyet veya hatasız finansal veri garantisi yoktur. Seçtiğin AI aracının, veri kaynağının ve barındırmanın ücretleri ayrı olabilir. Ücret, kota, veri hakkı ve tam varlık kapsamını seçtiğin plan için resmî kaynaklardan doğrula.

Kullanıcının yaptığı bir işlemi kaydetmek ile bankaya/aracı kuruma gerçek emir göndermek farklıdır; gerçek emir bu kitin kapsamı dışındadır. Yatırım veya vergi danışmanlığı sağlamaz. Kodun çalışması, finansal hesabın veya çok kullanıcılı erişimin güvenli olduğunun tek başına kanıtı değildir.

## Lisans

Kit [MIT lisansı](LICENSE) ile paylaşılır. Lisans ve telif bildirimlerini koruyarak içeriği kullanabilir, değiştirebilir ve paylaşabilirsin; ticari kullanım da mümkündür. Lisans hiçbir garanti vermez. Bu izin kitin içeriği içindir; kullandığın AI araçlarının, veri kaynaklarının veya diğer bileşenlerin koşullarını değiştirmez. Tam metin `LICENSE` dosyasında; [resmî MIT metni](https://opensource.org/license/mit) üzerinden kontrol edilebilir.
