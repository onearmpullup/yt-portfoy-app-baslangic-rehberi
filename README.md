# AI ile Portföy Geliştirme Kiti

Kendi ihtiyaçlarına uygun bir kişisel portföy takip uygulamasını AI ile **planlamak, küçük adımlarla geliştirmek ve test etmek** için Türkçe başlangıç rehberi ve skill paketi.

Bu depo hazır bir uygulama veya belirli bir ürünün kopyası değildir. Önce hangi sorunu çözmek istediğini belirler; sonra varlıklarını, veri girişini, ekranlarını ve teknik seçeneklerini buna göre seçersin. Haber, chatbot, otomatik fiyat ve çevrimiçi üyelik zorunlu değildir. Bütçen veya API anahtarın yoksa manuel ve sentetik verilerle başlayabilirsin.

## En kolay başlangıç: skill kurmadan

Codex, Claude Code veya dosya okuyabilen başka bir AI yardımcısında kendi proje klasörünü aç. [AI-ILE-PORTFOY-TASARLA.md](AI-ILE-PORTFOY-TASARLA.md) dosyasını ekle veya içeriğini yapıştır. Şu mesajı gönder:

> Bu talimata göre benimle Türkçe ilerle. Önce ihtiyaçlarımı öğren; her turda en fazla 3–4 ilgili soru sor. Bana özel bir portföy takip uygulaması planlayalım. Şimdilik sadece plan istiyorum, kod yazma. Bütçe veya API anahtarı gerektirmeyen başlangıç seçeneğini de açıkla.

Yardımcın internete erişebiliyorsa bu deponun bağlantısını verip aynı dosyayı okumasını isteyebilirsin. Erişemiyorsa okumuş gibi devam etmesini isteme; dosyayı ekle veya metni yapıştır. GitHub'a bir depo bağlamak tek başına skill kurulumu değildir.

İlk beklenen sonuç: ihtiyaçlarını özetleyen, ilk sürümün bir veya iki önemli işini seçen, test ölçütleri belli kısa bir plan. Geliştirmek istediğinde:

> Uzlaştığımız planın ilk çalışan dilimini oluştur. Tamamen sentetik veriler kullan. Kabul kontrollerini çalıştır; çalıştıramadıklarını açıkça yaz. Mevcut dosyalarımı koru. Henüz yayınlama veya ücretli hizmet açma.

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
