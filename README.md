# POS Retail — Unduhan

Repo **hanya untuk distribusi installer** POS Retail. Source code tidak ada di
sini.

## Unduh

Tautan permanen — selalu menunjuk ke installer terbaru:

```
https://github.com/scriptwriter123/pos-downloads/releases/latest/download/AnjayRetailSoft.exe
```

Atau pindai QR ini:

![QR Unduhan Installer POS](docs/qr-download.png)

Daftar semua versi: https://github.com/scriptwriter123/pos-downloads/releases

Buat ulang QR dengan `python scripts/make_download_qr.py` dari repo sumber.

## Instalasi

1. Jalankan `AnjayRetailSoft.exe` — instalasi untuk pengguna saat ini, tidak
   perlu administrator.
2. Aktivasi lisensi offline: simpan permintaan `.posreq` dari layar aktivasi,
   minta file `.poslic` ke penerbit, lalu impor.
3. Buat akun OWNER pada layar pertama.

Data tersimpan di `%LOCALAPPDATA%\POSApp\data`, atau folder `POS_DATA_DIR` bila
di-set (untuk deployment server RDS).

## Verifikasi

Setiap catatan rilis memuat checksum SHA256 installer:

```powershell
Get-FileHash .\AnjayRetailSoft.exe -Algorithm SHA256
```
