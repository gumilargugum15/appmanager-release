# Kagoem AppManager — rilis Android

Control center aplikasi ekosistem Kagoem (WarungKu, ServisKu, GerakYuk!, TagihKu).
Server: `https://app-manager.kagoemdigital.my.id/api/v1`. Kode sumber: `gumilargugum15/appmanager`.

| Versi | Tanggal | APK | SHA-256 |
|---|---|---|---|
| 1.0.0 (build 1) | 2026-11-14 | [`releases/v1.0.0/kagoem-appmanager-1.0.0.apk`](releases/v1.0.0/kagoem-appmanager-1.0.0.apk) | `27a8c547472f2b9830bebd1f76c12a218524441908ccd6957e77873608631ddb` |

## Instal
1. Unduh APK, cocokkan checksum: `sha256sum -c kagoem-appmanager-1.0.0.apk.sha256`.
2. Izinkan "Instal aplikasi tidak dikenal" untuk browser/file manager, lalu buka APK.
3. Login dengan akun Super Admin atau akun dari undangan developer.

Catatan: APK ditandatangani **debug key** (distribusi internal/sideload, bukan Play Store). Rilis berikutnya yang
memakai keystore rilis tidak bisa dipasang menimpa versi ini — uninstall dulu.

## v1.0.0
MVP: login/undangan developer, dashboard monitoring, App Registry & environment (credential HMAC, test connection),
Database Manager & Data Explorer read-only (PII dimasking), Sync Monitor, Backup & restore dengan approval,
Schema monitor, Alerts, aktivitas/audit, manajemen tim. Android minimal sesuai Flutter default.
