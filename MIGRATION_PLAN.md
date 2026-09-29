# 📄 Dosya Yolu: TurkuazLabs/.github/MIGRATION_PLAN.md
# 📌 Amac: TurkuazLabs, TurkuazSoft ve LevelUpGT repository tasima ve edition split planini takip etmek
# 📌 Modul - Markdown
# Version: 1.0.0
# Aciklama: Tamamlanan tasimalari, siradaki edition auditlerini ve yeni private repository ihtiyaclarini kaydeder
# Bagimli Oldugu Katman: Config

# Repository Migration Plan

## Tamamlanan - LevelUpGT

Asagidaki game repository'leri LevelUpGT altina tasindi ve private tutuluyor:

- LevelUpGT/CarArena
- LevelUpGT/DivineRealms
- LevelUpGT/RagnarOnline
- LevelUpGT/versus.com
- LevelUpGT/playnebula
- LevelUpGT/RagnarokServer
- LevelUpGT/RagnarokClient

Transfer sonrasi eski TurkuazLabs hard-coded repository referansi bulunmadi.

## TurkuazLabs - Public Community Baseline

Mevcut public Community repository'leri:

- TurkuazLabs/TurkuazInstaller
- TurkuazLabs/UniZip
- TurkuazLabs/JExporter
- TurkuazLabs/Turkuaz-PhoneBook
- TurkuazLabs/PixelTone

UniZip ve JExporter Community/Pro edition dokumani ve Apache-2.0 Community lisans baseline'i tamamlandi.

## Community + Pro Split Adaylari

Bu projelerde hedef, kullanilabilir Community Core'u TurkuazLabs'ta tutmak ve Pro/Business modullerini TurkuazSoft private repository'lerine ayirmaktir:

- JHoster
- TurkuazMuhasebe
- Start3POS
- TurkuazOffice
- TurkuazVM
- Nova9
- TurkuazPasswordManager

Public edilmeden once repository history icinde secret, credential, private policy veya Pro-only source bulunup bulunmadigi audit edilmelidir.

## Community Public Adaylari

Edition audit sonrasi TurkuazLabs public repository olarak degerlendirilecek araclar:

- Turkuaz-Pip-Firefox
- Turkuaz-FTP-Viewer-Firefox
- Turkuaz-MediaPlayer

## Commercial / Private Audit

Asagidaki projeler Community olarak public edilmeden once urun modeli karari gerektirir:

- Nexus4
- FonRadar
- ColorTone

Nexus4 kimlik, commerce, entitlement ve platform operation katmanlari nedeniyle TurkuazSoft commercial platform adayi olarak oncelikli incelenecektir.

## TurkuazSoft Ilk Private Repository Seti

Olusturulmasi planlanan repository'ler:

- TurkuazSoft/TurkuazEntitlement
- TurkuazSoft/TurkuazInstaller-Pro
- TurkuazSoft/UniZip-Pro
- TurkuazSoft/JExporter-Pro
- TurkuazSoft/JHoster-Pro
- TurkuazSoft/TurkuazMuhasebe-Pro

Sonraki edition auditlerine gore:

- TurkuazSoft/Start3POS-Pro
- TurkuazSoft/TurkuazOffice-Pro
- TurkuazSoft/TurkuazVM-Pro
- TurkuazSoft/Nova9-Pro

eklenebilir.

## Tasima Sirasi

1. LevelUpGT transferlerini ve CI durumlarini dogrula.
2. TurkuazSoft private repository shell'lerini olustur.
3. Ortak TurkuazEntitlement kontratini ve policy sinirini kur.
4. JHoster Community/Pro split.
5. TurkuazMuhasebe Community/Pro/Business split.
6. TurkuazInstaller, UniZip ve JExporter Pro modullerini private repository'lere bagla.
7. Start3POS, TurkuazOffice, TurkuazVM ve Nova9 edition audit.
8. Kalan private repository'leri commercial/community sinirina gore yeniden siniflandir.
9. TurkuazLabs altinda gereksiz private commercial repository birakma.

## Guvenlik Notu

Bir private repository public hale getirilmeden once sadece current tree degil Git history de denetlenmelidir. Gecmiste commit edilmis secret veya Pro-only source varsa repository history temizlenmeden public yapilmaz.
