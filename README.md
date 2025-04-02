# RaceForge Eklentisi (Irk Sistemi)

![RaceForge]([http://url/to/img.png](https://hizliresim.com/56iszaj))

## İçindekiler
- [Genel Bakış](#genel-bakış)
- [Özellikler](#özellikler)
- [Kurulum](#kurulum)
- [Komutlar](#komutlar)
- [İzin Sistemi](#izin-sistemi)
- [Irk Sistemi](#irk-sistemi)
  - [İnsan Irkı](#i̇nsan-irkı)
  - [Cüce Irkı](#cüce-irkı)
  - [Elf Irkı](#elf-irkı)
  - [Ork Irkı](#ork-irkı)
- [Yetenek Sistemi](#yetenek-sistemi)
- [Holokron Sistemi](#holokron-sistemi)
- [Market Sistemi](#market-sistemi)
- [Placeholder'lar](#placeholderlar)
- [Yapılandırma](#yapılandırma)
- [LuckPerms Entegrasyonu](#luckperms-entegrasyonu)
- [Sık Sorulan Sorular](#sık-sorulan-sorular)
- [İletişim](#i̇letişim)

## Genel Bakış

IrkSistemi, Minecraft sunucunuza kapsamlı bir rol yapma deneyimi kazandıran, tamamen özelleştirilebilir bir ırk ve yetenek ağacı eklentisidir. Oyuncular dört farklı ırk arasından seçim yapabilir (İnsan, Cüce, Elf ve Ork), her biri benzersiz özellikler ve yeteneklerle donatılmıştır.

Bu eklenti, oyuncuların karakterlerini seviyeler kazanarak geliştirmelerini ve zamanla daha güçlü yeteneklerin kilidini açmalarını sağlar. Ayrıca, holokron ekonomisi ve özel eşya sistemiyle oyun deneyimini zenginleştirir.

## Özellikler

- **4 Benzersiz Irk**: Her biri kendine özgü avantajlar ve yeteneklerle gelir
- **Kapsamlı Yetenek Ağaçları**: Her ırk için 20+ özel yetenek
- **Holokron Para Birimi**: Yetenekleri açmak ve marketten eşya satın almak için özel para birimi
- **Irk Marketi**: Her ırkın kendi özel eşyalarını satın alabileceği market
- **Seviye Sistemi**: Aktivitelerden XP kazanarak seviye atlama
- **Özel Eşyalar**: Her ırk için özel yeteneklere sahip eşyalar
- **LuckPerms Entegrasyonu**: Irk bazlı izinler için destek
- **Tam Yapılandırılabilir**: Tüm özellikler config dosyasından özelleştirilebilir

## Kurulum
- Parties / Vault / EssentialsX kurulumu **zorunlu** eklentilerdir.
1. Sunucunuzda LuckPerms eklentisini kurun (isteğe bağlı, ancak ırk bazlı izin sistemi için önerilir)
2. IrkSistemi eklentisini `plugins` klasörüne yerleştirin
3. Sunucuyu yeniden başlatın veya `/reload` komutunu çalıştırın
4. İstenirse, `config.yml` dosyasını düzenleyerek eklentiyi özelleştirin
5. `/irk` komutuyla ırk menüsünü açın!

## Komutlar

### Genel Komutlar

| Komut | Açıklama | İzin |
|-------|----------|------|
| `/irk` | Ana ırk bilgisi ve komut listesini gösterir | `irksistemi.irk` |
| `/irk menü` | Irk seçim menüsünü açar | `irksistemi.irk` |
| `/irk bilgi` | Mevcut ırkınız hakkında bilgi verir | `irksistemi.irk` |
| `/irkmenu` | Ana IrkSistemi menüsünü açar | `irksistemi.irk` |
| `/yetenek` | Yetenek komutlarını gösterir | `irksistemi.yetenek` |
| `/yetenek listele` | Açılabilir yetenekleri listeler | `irksistemi.yetenek` |
| `/yetenek aç <yetenek>` | Belirtilen yeteneği açar | `irksistemi.yetenek` |
| `/yetenek info <yetenek>` | Yetenek hakkında bilgi verir | `irksistemi.yetenek` |
| `/seviye` | Seviyenizi ve XP bilginizi gösterir | `irksistemi.seviye` |
| `/istatistik` | Oyuncu istatistiklerini gösterir | `irksistemi.istatistik` |

### Holokron Komutları

| Komut | Açıklama | İzin |
|-------|----------|------|
| `/holokron` | Holokron bakiyenizi gösterir | `irksistemi.holokron` |
| `/holokron topla` | Envanterinizdeki holokronları toplar | `irksistemi.holokron` |
| `/holokron ekle <oyuncu> <miktar>` | Belirtilen oyuncuya holokron ekler | `irksistemi.holokron.admin` |
| `/holokron çek <miktar>` | Belirtilen miktarda holokron çeki oluşturur | `irksistemi.holokron.admin` |

### Cüce Yetenek Komutları

| Komut | Açıklama | İzin |
|-------|----------|------|
| `/yeraltiyolu` | Yer Altı Yolu yeteneğini kullanır | Cüce yeteneği açık oyuncular |
| `/titanyumkalkan` | Titanyum Kalkan yeteneğini kullanır | Cüce yeteneği açık oyuncular |

### Admin Komutları

| Komut | Açıklama | İzin |
|-------|----------|------|
| `/irk admin reload` | Eklenti konfigürasyonunu yeniden yükler | `irksistemi.admin.reload` |
| `/seviye ekle <oyuncu> <miktar>` | Belirtilen oyuncuya XP ekler | `irksistemi.seviye.add` |
| `/seviye ayarla <oyuncu> <seviye>` | Belirtilen oyuncunun seviyesini ayarlar | `irksistemi.seviye.set` |

## İzin Sistemi

### Genel İzinler

| İzin | Açıklama | Varsayılan |
|------|----------|------------|
| `irksistemi.admin` | Tüm yönetici komutlarına erişim | op |
| `irksistemi.irk` | Irk komutlarını kullanma izni | true |
| `irksistemi.yetenek` | Yetenek komutlarını kullanma izni | true |
| `irksistemi.seviye` | Seviye görüntüleme izni | true |
| `irksistemi.istatistik` | İstatistik görüntüleme izni | true |
| `irksistemi.holokron` | Holokron komutlarını kullanma izni | true |
| `irksistemi.irkmarket` | Irk marketi komutlarını kullanma izni | true |

### Yönetici İzinleri

| İzin | Açıklama | Varsayılan |
|------|----------|------------|
| `irksistemi.admin.reload` | Config dosyasını yeniden yükleme izni | op |
| `irksistemi.seviye.add` | Oyunculara XP ekleme izni | op |
| `irksistemi.seviye.set` | Oyuncuların seviyesini değiştirme izni | op |
| `irksistemi.irk.change` | Başka oyuncuların ırkını değiştirme izni | op |
| `irksistemi.istatistik.others` | Başka oyuncuların istatistiklerini görme izni | op |
| `irksistemi.holokron.admin` | Holokron admin komutlarını kullanma izni | op |

### Irk İzinleri (LuckPerms ile)

| İzin | Açıklama | Varsayılan |
|------|----------|------------|
| `irk.insan` | İnsan ırkına sahip oyuncular için | false (otomatik verilir) |
| `irk.cuce` | Cüce ırkına sahip oyuncular için | false (otomatik verilir) |
| `irk.elf` | Elf ırkına sahip oyuncular için | false (otomatik verilir) |
| `irk.ork` | Ork ırkına sahip oyuncular için | false (otomatik verilir) |

## Irk Sistemi

IrkSistemi eklentisi, dört benzersiz ırk sunar. Her ırkın kendi özellikleri, yetenekleri ve avantajları bulunur.

### İnsan Irkı

İnsanlar çok yönlü ve uyumlu bir ırktır. Her tür zorlukla başa çıkabilirler.

**Temel Özellikler:**
- Başlangıç Sağlık: 20 (10 ❤)
- Hasar Çarpanı: 1.0
- Başlangıç Yetenek Puanı: 3

**Pasif Yetenekler:**
- Bilgelik: %25 daha fazla XP kazanma
- Dayanıklılık: Alınan hasarı azaltma (3 seviye)
- Taş Kalp: Maksimum canı artırma (3 seviye)
- Alet Ustası: Alet dayanıklılığını artırma
- Acele: Gece görüşü yeteneği

**Aktif Yetenekler:**
- Liderlik: Yakındaki takım arkadaşlarını güçlendirir
- Savaş Çığlığı: Düşmanları şaşırtır ve müttefikleri güçlendirir
- Kutsal Kalkan: Hasar azaltan koruyucu alan yaratır
- İlkyardım: Yakındaki oyuncuları iyileştirir
- Yansıtıcı Zırh: Alınan hasarın bir kısmını geri yansıtır

### Cüce Irkı

Cüceler dayanıklı ve güçlü madencilerdir. Yeraltında avantajlıdırlar ve maden konusunda uzmandırlar.

**Temel Özellikler:**
- Başlangıç Sağlık: 22 (11 ❤)
- Hasar Çarpanı: 0.9
- Başlangıç Yetenek Puanı: 3

**Pasif Yetenekler:**
- Taş Yumruk: Kazma ve balyoz ile daha fazla hasar
- Maden Dehası: Nadir maden bulma şansını artırır
- Derin Nefes: Su altında daha uzun süre nefes alma
- Metal Ustası: Alet üretiminde malzeme tasarrufu
- Doğa Direnci: Sıcak/soğuk hasarına karşı direnç

**Aktif Yetenekler:**
- Yer Altı Yolu: Kısa mesafeli ışınlanma
- Titanyum Kalkan: Geçici hasar azaltıcı kalkan
- Deprem: Etraftaki düşmanlara hasar verir ve fırlatır
- Cüce Gazabı: Etraftaki bloklara ve düşmanlara hasar verir
- Örs Yağmuru: Düşmanların üzerine örsler düşürür

### Elf Irkı

Elfler çevik ve doğa ile uyumlu bir ırktır. Okçulukta ustadırlar ve doğadan güç alırlar.

**Temel Özellikler:**
- Başlangıç Sağlık: 18 (9 ❤)
- Hasar Çarpanı: 1.2
- Başlangıç Yetenek Puanı: 3

**Pasif Yetenekler:**
- Keskin Göz: Kritik vuruş şansını ve hasarını artırır
- Doğanın Fısıltısı: Yakındaki düşmanları hissetme
- Sarmaşık Adımlar: Ot üzerinde koşarken hız kazanma
- Zehirli Oklar: Ok atışlarının zehirleme şansı
- Ay Şifası: Gece vakti daha hızlı iyileşme

**Aktif Yetenekler:**
- Doğa Kontrolü: Bitkileri hızla büyütür
- Rüzgarın Çocuğu: Etraftaki düşmanları itip yavaşlatır
- Gölge Bağı: Hedefi belirli bir süre sabitler
- Ay Işığı Salvosu: Hızlı ok atışları yapar
- Ormanın Kalbi: Çevredeki dost birimleri iyileştirir

### Ork Irkı

Orklar vahşi ve güçlü savaşçılardır. Yakın dövüşte avantajlıdırlar ve saldırgan bir doğaya sahiptirler.

**Temel Özellikler:**
- Başlangıç Sağlık: 24 (12 ❤)
- Hasar Çarpanı: 1.1
- Başlangıç Yetenek Puanı: 3

**Pasif Yetenekler:**
- Kaba Kuvvet: Yakın dövüş hasarını artırır
- Kalın Deri: Zırh dayanıklılığını artırır
- Savaş İçgüdüsü: Düşük canda hasar artışı
- Zırh Kırıcı: Düşmanların zırh korumasını azaltır
- Acimasız Öldürüş: Kritik vuruşlarda iyileşme

**Aktif Yetenekler:**
- Ork Savaş Çığlığı: Güç verir ve yakındaki düşmanları korkutur
- Öfke Patlaması: Düşmanları fırlatır ve hasar yansıtır
- Çarşaf Zincirleri: Düşmanları etkisiz hale getirir
- Kızgın Zırhlı: Yakın dövüş hasarı verir ve kendini güçlendirir
- Yırtıcı Canavarın Hücumu: Geçici olarak hız ve güç kazanır

## Yetenek Sistemi

Oyuncular seviye atlayarak yetenek puanları kazanırlar. Bu puanlar, ırklarına özel yetenek ağacındaki yetenekleri açmak için kullanılır.

### Yetenek Türleri

1. **Pasif Yetenekler**: Her zaman etkin olan yeteneklerdir.
2. **Aktif Yetenekler**: Komutla veya menüden etkinleştirilen, bekleme süresi olan yeteneklerdir.

### Yetenek Açma

1. `/yetenek` komutuyla yetenek menüsünü açın
2. Açmak istediğiniz yeteneği seçin
3. Yeterli yetenek puanına sahipseniz, yetenek açılacaktır
4. Aktif yetenekler için uygun komutu veya hızlı yetenek menüsünü kullanabilirsiniz

### Hızlı Yetenek Kullanımı

1. `/irkmenu` komutuyla ana menüyü açın
2. "Hızlı Yetenek" seçeneğine tıklayın
3. Kullanmak istediğiniz aktif yeteneği seçin

## Holokron Sistemi

Holokronlar, IrkSistemi eklentisinin özel para birimidir. Market eşyaları satın almak için kullanılır.

### Holokron Kazanma Yolları

1. **Canavar Öldürme**: Canavarlar belirli bir şansla holokron düşürür
2. **Admin Komutu**: Yöneticiler `/holokron ekle <oyuncu> <miktar>` komutuyla holokron verebilir
3. **Holokron Çeki**: `/holokron çek <miktar>` komutuyla oluşturulan çekler, sağ tıklanarak kullanılabilir

### Holokron Toplama

Envanterinizdeki holokronları toplamak için:
1. `/holokron topla` komutunu kullanın
2. Holokronlarınız bakiyenize eklenecektir

## Market Sistemi

Irk Marketi, her ırk için özel eşyalar sunar. Bu eşyalar holokron ile satın alınabilir.

### Market Kategorileri

1. **İnsan Eşyaları**:
   - Arturhur'un Kılıcı
   - Tyrll Zırh Seti
   - Karanlık Asa
   - Adem'in Elması

2. **Cüce Eşyaları**:
   - Mitril Kazma
   - Örn Çekici
   - Mitril Zırh Seti
   - Cüce Derisi
   - Örs Yağmuru

3. **Elf Eşyaları**:
   - Rüzgar Yayı
   - Legolas'ın Yayı
   - Aphetios Botları
   - Elrond Tacı
   - Legolas Zırh Seti

4. **Ork Eşyaları**:
   - Ork Balyozu
   - Savaş Baltası
   - Kemik Kıran Kılıcı
   - Öfke Zırhı

### Market Kullanımı

1. `/irkmarket` komutuyla market menüsünü açın
2. Satın almak istediğiniz eşyaya tıklayın
3. Yeterli holokrona sahipseniz, eşya envanterinize eklenecektir

## Placeholder'lar

IrkSistemi, PlaceholderAPI ile entegre çalışarak diğer eklentiler tarafından kullanılabilecek çeşitli placeholder'lar sunar. Bu placeholder'ları skor tablolarında, chat mesajlarında veya hologram eklentilerinde kullanabilirsiniz.

### Kurulum

1. PlaceholderAPI eklentisini sunucunuza yükleyin
2. IrkSistemi otomatik olarak PlaceholderAPI ile entegre olacaktır

### Kullanılabilir Placeholder'lar

| Placeholder | Açıklama | Örnek Çıktı |
|-------------|----------|-------------|
| `%irksistemi_race%` | Oyuncunun ırkını gösterir | İnsan, Cüce, Elf, Ork |
| `%irksistemi_race_color%` | Oyuncunun ırkını renkli gösterir | &aİnsan, &8Cüce, &bElf, &cOrk |
| `%irksistemi_level%` | Oyuncunun seviyesini gösterir | 15 |
| `%irksistemi_xp%` | Oyuncunun mevcut XP'sini gösterir | 1250 |
| `%irksistemi_xp_needed%` | Sonraki seviyeye geçmek için gereken XP'yi gösterir | 3500 |
| `%irksistemi_xp_percentage%` | Seviye ilerleme yüzdesini gösterir | 35.7% |
| `%irksistemi_xp_progress_bar%` | 10 karakterlik bir ilerleme çubuğu gösterir | ■■■■□□□□□□ |
| `%irksistemi_holokron%` | Oyuncunun holokron bakiyesini gösterir | 750 |
| `%irksistemi_skill_points%` | Oyuncunun mevcut yetenek puanlarını gösterir | 3 |
| `%irksistemi_active_skills%` | Oyuncunun açtığı aktif yetenek sayısını gösterir | 2 |
| `%irksistemi_passive_skills%` | Oyuncunun açtığı pasif yetenek sayısını gösterir | 5 |
| `%irksistemi_total_skills%` | Oyuncunun açtığı toplam yetenek sayısını gösterir | 7 |
| `%irksistemi_health_boost%` | Irktan kaynaklanan sağlık bonusunu gösterir | +2 |
| `%irksistemi_damage_multiplier%` | Irktan kaynaklanan hasar çarpanını gösterir | 1.2x |
| `%irksistemi_skill_cooldown_<skill>%` | Belirli bir yeteneğin bekleme süresini gösterir | 15s |
| `%irksistemi_top_race_<position>%` | En popüler ırklar listesinde belirtilen pozisyondaki ırkı gösterir | Cüce (25 oyuncu) |
| `%irksistemi_highest_level_player%` | En yüksek seviyeli oyuncuyu gösterir | Notch (Lvl 87) |

### Örnek Kullanım

```
[%irksistemi_race_color%&f] &e%player_name% &7- &eSeviye: &f%irksistemi_level%
&7Holokron: &f%irksistemi_holokron% &7XP: &f%irksistemi_xp_progress_bar% &7(%irksistemi_xp_percentage%)
```

Bu format, oyuncunun üzerinde görünecek bir hologram için kullanılabilir ve şuna benzer bir çıktı üretir:

```
[Cüce] Notch - Seviye: 24
Holokron: 1250 XP: ■■■■■□□□□□ (53.2%)
```

## Yapılandırma

Tüm eklenti ayarları `plugins/IrkSistemi/config.yml` dosyasından özelleştirilebilir.

### Ana Yapılandırma Kategorileri

1. **Genel Plugin Ayarları**: Prefix, debug modu vb.
2. **Holokron Ayarları**: Düşme şansı, maksimum değerler
3. **Seviye ve XP Ayarları**: XP gereksinimleri, formül ayarları
4. **Irk Ayarları**: Irk özellikleri ve yetenekleri
5. **Yetenek Ayarları**: Yetenek puanları, cooldown süreleri
6. **Market Ayarları**: Eşya fiyatları ve özellikleri

### Örnek Yapılandırma

```yaml
# Genel Plugin Ayarları
plugin:
  prefix: "&5[&dIrkSistemi&5] &r"
  debug: false

# Holokron Ayarları
holokron:
  max-holokron: 0
  default_drop_chance: 25.0

# Seviye ve XP Ayarları
leveling:
  base_xp: 1000
  multiplier: 2
  max_level: 500
  skill_point_per_level: 1
```

Tüm yapılandırma seçenekleri için `config.yml` dosyasını inceleyin.

## LuckPerms Entegrasyonu

IrkSistemi, oyuncuların ırklarına göre otomatik olarak izinler atamak için LuckPerms eklentisiyle entegre çalışır.

### Nasıl Çalışır?

1. LuckPerms eklentisi sunucunuzda yüklüyse, entegrasyon otomatik olarak aktif olur
2. Oyuncu bir ırk seçtiğinde, uygun izin (`irk.insan`, `irk.cuce`, vb.) otomatik olarak atanır
3. Oyuncu ırkını değiştirdiğinde, eski ırk izni kaldırılır ve yeni ırk izni atanır

### İzinlerin Kullanımı

Bu izinleri diğer eklentilerde koşul olarak kullanabilirsiniz. Örneğin:
- Belirli bölgelere sadece belirli ırkların erişimine izin verme
- Irklar için özel komutlar oluşturma
- Sunucunuzda benzersiz deneyimler oluşturma


## Sık Sorulan Sorular

**S: Irkımı değiştirirsem ne olur?**  
C: Tüm yetenekleriniz sıfırlanır, seviyeniz 1'e düşer ve XP'niz sıfırlanır. Holokron bakiyeniz etkilenmez.

**S: Yetenek puanlarını nasıl kazanırım?**  
C: Seviye atladıkça yetenek puanı kazanırsınız. Her seviye için 1 yetenek puanı kazanırsınız.

**S: Holokronları nasıl toplayabilirim?**  
C: Canavar öldürdüğünüzde düşen holokronları, `/holokron topla` komutuyla toplayabilirsiniz.

**S: Bir aktif yeteneği tekrar kullanmak için ne kadar beklemeliyim?**  
C: Her yeteneğin kendine özgü bir bekleme süresi vardır. Bu süre config dosyasından özelleştirilebilir.

**S: LuckPerms olmadan eklenti çalışır mı?**  
C: Evet, LuckPerms olmadan da eklenti tamamen çalışır. Sadece ırk bazlı izin sistemi çalışmaz.

## İletişim

**Discord**: https://discord.gg/irksistemine-katil  
**E-posta**: irksistemi@example.com

---

### Teşekkürler

- Eklentiyi kullandığınız için teşekkür ederiz!
- Geri bildirim ve önerileriniz için bize ulaşın.
- Yeni özellikler ve güncellemeler için Discord sunucumuza katılın.

© 2025 IrkSistemi Eklentisi | Tüm hakları saklıdır. 
