# Aplikasi Web "Uptime Kuma"

## Sekilas Tentang
Uptime Kuma adalah aplikasi pemantauan uptime/downtime berbasis web yang intuitif dan open-source. Aplikasi ini digunakan untuk memantau ketersediaan layanan jaringan (HTTP, Ping, DNS, Port) secara real-time.

## Instalasi

### Prasyarat
- Ubuntu Server 16.04/22.04 LTS
- Docker
- Port 3001 terbuka

### Langkah Instalasi
1. Update sistem dan install Docker:
   ```bash
   sudo apt update && sudo apt install docker.io -y
   ```

2. Jalankan container Uptime Kuma via Docker:
   ```bash
   sudo docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
   ```

3. Akses antarmuka web melalui `http://localhost:3001`.

## Konfigurasi
- **Monitoring**: Penambahan pemantauan layanan seperti Portal IPB University, Google DNS, dan GitHub Service.
- **Public Status Page**: Konfigurasi halaman status publik untuk menampilkan ketersediaan sistem kepada pengguna akhir.

## Cara Pemakaian
Aplikasi dapat diakses melalui browser pada port 3001. Antarmuka menampilkan status real-time, grafik latency, dan statistik ketersediaan layanan.

## Pembahasan

### Kelebihan
- Antarmuka sangat modern, ringan, dan user-friendly.
- Mendukung berbagai macam protokol pemantauan (HTTP/HTTPS, Ping, DNS, Docker, dll).
- Memiliki fitur Public Status Page bawaan tanpa konfigurasi rumit.

### Kekurangan
- Belum memiliki fitur agent pemantauan terdistribusi secara native layaknya kombinasi Prometheus/Grafana.

### Perbandingan
Dibandingkan dengan UptimeRobot (layanan SaaS populer), Uptime Kuma memberikan kebebasan interval pemantauan hingga hitungan detik dan pemantauan tanpa batas tanpa biaya berlangganan bulanan.

## Referensi
1. Source Code Repository: [https://github.com/louislam/uptime-kuma](https://github.com/louislam/uptime-kuma)
2. Official Site: [https://uptime.kuma.pet/](https://uptime.kuma.pet/)
