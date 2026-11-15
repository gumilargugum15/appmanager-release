# Kagoem AppManager — rilis Android

Control center aplikasi ekosistem Kagoem (WarungKu, ServisKu, GerakYuk!, TagihKu).
Server: `https://app-manager.kagoemdigital.my.id/api/v1`. Kode sumber: `gumilargugum15/appmanager`.

| Versi | Tanggal | APK | SHA-256 |
|---|---|---|---|
| **1.1.1 (build 3)** — terbaru | 2026-11-15 | [`releases/v1.1.1/kagoem-appmanager-1.1.1.apk`](releases/v1.1.1/kagoem-appmanager-1.1.1.apk) | `d7c4ff6f57146d7caeb19658e73392c73ec8cbb97f4d8fb74ab77f9a00104ffa` |
| 1.1.0 (build 2) | 2026-11-14 | [`releases/v1.1.0/kagoem-appmanager-1.1.0.apk`](releases/v1.1.0/kagoem-appmanager-1.1.0.apk) | `10fb3fec2b1d284f6da88e31d05d4aa563d95fee8fd06252a6f9fddb635fd550` |
| 1.0.0 (build 1) | 2026-11-14 | [`releases/v1.0.0/kagoem-appmanager-1.0.0.apk`](releases/v1.0.0/kagoem-appmanager-1.0.0.apk) | `27a8c547472f2b9830bebd1f76c12a218524441908ccd6957e77873608631ddb` |

## Instal
1. Unduh APK versi terbaru, cocokkan checksum: `sha256sum -c kagoem-appmanager-<versi>.apk.sha256`.
2. Izinkan "Instal aplikasi tidak dikenal" untuk browser/file manager, lalu buka APK.
3. Login dengan akun Super Admin atau akun dari undangan developer.

Catatan: APK ditandatangani **debug key** (distribusi internal/sideload, bukan Play Store). Rilis berikutnya yang
memakai keystore rilis tidak bisa dipasang menimpa versi ini — uninstall dulu.

## v1.1.1
- **Ganti password** sendiri: Pengaturan → *Ganti password*. Wajib password saat ini; password baru minimal
  10 karakter berisi huruf dan angka. Setelah diganti, sesi di perangkat lain otomatis dikeluarkan dan tercatat di audit.
- Butuh server AppManager ≥ 2026-11-15. Update dari 1.1.0/1.0.0: pasang langsung (menimpa), data login tetap.

## v1.1.0
- **Data Explorer: semua tabel** database aplikasi target (kecuali tabel token/session/job/cache yang diblokir);
  kolom rahasia disembunyikan dan data pribadi dimasking otomatis.
- **CRUD per baris** (tambah/ubah/hapus) untuk Super Admin, hanya bila diaktifkan di server aplikasi target
  (`APPMANAGER_WRITE_ENABLED`). Setiap perubahan wajib alasan, production wajib konfirmasi ketik "production",
  dan tercatat di audit (nilai sebelum/sesudah). Tabel transaksi/stok/sinkronisasi dapat dikunci read-only.
- Icon aplikasi baru (adaptive icon Android 8+).
- Butuh server AppManager ≥ 2026-11-14 dan adapter `kagoem/app-manager-adapter` ≥ 0.2.0 untuk fitur baru.
- Update dari 1.0.0: pasang langsung (menimpa), data login tetap.

## v1.0.0
MVP: login/undangan developer, dashboard monitoring, App Registry & environment (credential HMAC, test connection),
Database Manager & Data Explorer read-only (PII dimasking), Sync Monitor, Backup & restore dengan approval,
Schema monitor, Alerts, aktivitas/audit, manajemen tim. Android minimal sesuai Flutter default.
