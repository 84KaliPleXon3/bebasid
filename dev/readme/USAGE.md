# Cara Penggunaan
## Windows

Jalankan BEBASID.exe dengan "Run as administrator". Kemudian ikuti instruksi yang ada.

Untuk instalasi secara manual, bisa copy file hosts bebasid ke
```
C:\Windows\System32\drivers\etc
```
Jika halaman masih belum bisa terbuka, silahkan lakukan flush dns di cmd.

```
ipconfig /release
ipconfig /renew
ipconfig /flushdns
```

## Android

Salin file hosts dan paste di folder /etc kemudian restart HP.

Alternatif (jika ingin install melewati aplikasi atau menambahkan list hosts lain)

Install aplikasi [AdAway](https://f-droid.org/en/packages/org.adaway)

```
https://raw.githubusercontent.com/gvoze32/bebasid/master/releases/hosts
```

Buka aplikasinya, pilih Add, kemudian salin kode diatas lalu tambahkan.

Centang opsi "Allow Redirections" di Settings.

**Cara di atas memerlukan akses root, jika HP belum diroot, bisa memakai cara ini.**

Install aplikasi [Hosts Go](https://play.google.com/store/apps/details?id=dns.hosts.server.change), buka aplikasinya, klik "Hosts Settings", lalu pilih hosts. Kemudian jalankan.

## Linux

Buka terminal, lalu ketik atau salin kode di bawah ini, lalu enter.

```
# Install
sudo curl -sfLS https://raw.githubusercontent.com/gvoze32/bebasid/master/dev/scripts/bebasid.sh >> /usr/local/bin/bebasid

# Alternatif Install (Gunakan jika saat menggunakan curl muncul permission denied, kamu bisa memakai wget)
sudo wget https://raw.githubusercontent.com/gvoze32/bebasid/master/dev/scripts/bebasid.sh -O /usr/local/bin/bebasid

# Kemudian berikan permission ke folder bash
sudo chmod +x /usr/local/bin/bebasid

# Bantuan
bebasid --help
```

Alternatif (jika hanya ingin memasang file hosts):
```
sudo curl -sfLS https://raw.githubusercontent.com/gvoze32/bebasid/master/releases/hosts >> /etc/hosts
```
atau
```
sudo wget https://raw.githubusercontent.com/gvoze32/bebasid/master/releases/hosts -O /etc/hosts
```

## BSD / macOS

Buka terminal, lalu ketik atau salin kode di bawah ini lalu enter.

```
sudo curl -sfLS https://raw.githubusercontent.com/gvoze32/bebasid/master/releases/hosts >> /etc/hosts
```

Alternatif
```
sudo wget https://raw.githubusercontent.com/gvoze32/bebasid/master/releases/hosts -O /etc/hosts
```
