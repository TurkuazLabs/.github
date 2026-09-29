# 📄 Dosya Yolu: TurkuazLabs/.github/ORGANIZATION_MODEL.md
# 📌 Amac: Turkuaz ekosistemindeki Community, Commercial ve Game Technology organizasyon sinirlarini tanimlamak
# 📌 Modul - Markdown
# Version: 1.0.0
# Aciklama: TurkuazLabs, TurkuazSoft ve LevelUpGT sorumluluklarini ve repository bagimlilik kurallarini tanimlar
# Bagimli Oldugu Katman: Config

# Organization Model

## 1. TurkuazLabs

Rol: Community, Open Source ve public developer technology.

Bu organizasyonda:

- Community edition kaynaklari
- Public SDK ve API contractlari
- Acik kaynak developer tools
- Public extension ve adapterlar
- Ornekler ve dokumantasyon

bulunur.

Community repository, build veya test icin private Pro repository'ye bagimli olamaz.

## 2. TurkuazSoft

Rol: Pro, Business, Enterprise ve commercial software.

Bu organizasyonda:

- Pro moduller
- Business / Enterprise moduller
- Private service implementation
- Entitlement ve device policy
- Private update feed
- Signing/release orchestration
- Musteriye ozel entegrasyon
- Ticari backend ve operasyon servisleri

bulunabilir.

Community kodu public package, tag, release veya contract uzerinden tuketilebilir.

Bagimlilik yonu:

```text
TurkuazLabs Community
        ^
        |
TurkuazSoft Pro / Business
```

Ters bagimlilik yasaktir.

## 3. LevelUpGT

Gorunen marka: LevelUp Games & Game Technology.

Rol: Games, multiplayer systems ve game technology.

Bu organizasyonda:

- Oyun kaynaklari
- Game server/backend
- Launcher
- Matchmaking
- Game telemetry
- Anti-cheat
- Game asset pipeline
- Oyunlara ozel servisler

bulunabilir.

Game projeleri gerekli oldugunda TurkuazSoft commercial servislerini contract/API seviyesinde kullanabilir.

## Lisans Modeli

Public Community repository'lerinde varsayilan hedef Apache License 2.0'dur; ancak ucuncu taraf lisanslari ve proje-bazli istisnalar ayrica korunur.

Pro/Business kaynaklari ayri private repository veya package olarak tutulur ve ayri ticari lisans kosullarina tabidir.

Daha once public olarak Apache-2.0 altinda yayinlanan kaynak sonradan yalniz dosya silerek private hale getirilmis sayilmaz. Bu nedenle public/private siniri kod public edilmeden once belirlenir.

## Secret ve Credential Kurali

Asagidaki veriler public Community repository'ye yazilmaz:

- private signing key
- PFX/private certificate
- production token
- API secret
- private entitlement policy
- musteri credential
- production private endpoint credential
- private package/feed credential

## CI Siniri

TurkuazLabs CI:
- Community compile/test
- public security checks
- package/release verification

TurkuazSoft CI:
- Pro/Business compile/test
- Community compatibility
- private packages
- code signing
- commercial release

LevelUpGT CI:
- game build/test
- server validation
- asset/tooling validation
- game-specific release pipeline

Local Gitea mirror ve self-hosted runner kullanimi organizasyon sinirlarini bozmadan devam edebilir.
