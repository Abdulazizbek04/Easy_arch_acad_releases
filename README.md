# Easy_arch for AutoCAD — relizlar

Ochiq (public) repo: plagin shu yerdan yangilanishni tekshiradi va yuklab oladi.

- `channels/stable.json` — hamma uchun
- `channels/beta.json`   — ishlab chiquvchi uchun
- `files/<versiya>/Easy_arch_acad_<versiya>.zip` — yangilanish to'plami (Plugins\*.bundle + PdfImzo)

## Reliz qanday chiqariladi (Windows)
1. `build_all.ps1` bilan `Vexar_Setup\` (Plugins + PdfImzo) yasaladi.
2. `Vexar_Setup` ni ZIP qiling → `Easy_arch_acad_<versiya>.zip`.
3. SHA256 ni hisoblang: `Get-FileHash Easy_arch_acad_<versiya>.zip -Algorithm SHA256`.
4. ZIP ni `files/<versiya>/` ga qo'ying, `channels/stable.json` dagi `version`, `url`, `sha256` ni yangilang.
5. Commit + push.
6. `Updater.Version` (plagin kodida) ham shu versiyaga oshirilsin.
