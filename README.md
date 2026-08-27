# LogiTrack

> Dashboard logistik terpadu yang menghubungkan Warehouse Service dan Shipment Service dalam satu antarmuka web.

## Ringkasan

LogiTrack adalah frontend final project **II3160 — Teknologi Sistem Terintegrasi**. Aplikasi ini memperlihatkan bagaimana dua microservice dapat digunakan dari satu alur pengguna: paket dicatat di gudang, dikirim ke kurir, menerima nomor resi, lalu dilacak hingga selesai.

| Aspek | Detail |
|---|---|
| Jenis proyek | Integrated frontend untuk dua REST service |
| Teknologi | HTML5, Tailwind CSS, JavaScript, Lucide Icons |
| Gaya UI | Responsive glassmorphism dengan tema logistik |
| Build step | Tidak ada; dapat dijalankan sebagai static site |

## Alur Pengguna

```text
Dashboard
   ├── Inventory ──► Warehouse API
   │                    │
   │                    └── buat / perbarui paket
   └── Shipments ──► Shipment API
                        └── buat resi / lacak / tandai delivered
```

## Fitur

- Dashboard statistik total paket, pending, in transit, dan delivered.
- Daftar serta pembuatan paket pada Warehouse Service.
- Inisiasi pengiriman dan penampilan nomor resi.
- Pelacakan shipment berdasarkan nomor resi.
- Pembaruan status pengiriman menjadi `DELIVERED`.
- Indikator ketersediaan kedua API.

## Halaman

| File | Fungsi |
|---|---|
| `index.html` | Ringkasan sistem dan status integrasi |
| `inventory.html` | Pengelolaan stok dan proses dispatch |
| `shipment.html` | Daftar, pencarian, dan pembaruan shipment |
| `style.css` | Styling tambahan di luar Tailwind CSS |

## Menjalankan Secara Lokal

```bash
git clone https://github.com/darrylrayhananta/II3160-FinalProject-LogiTrack.git
cd II3160-FinalProject-LogiTrack
python -m http.server 5500
```

Buka `http://localhost:5500`.

Frontend membutuhkan koneksi internet untuk memuat Tailwind CSS dan Lucide Icons dari CDN. Backend Warehouse dan Shipment juga harus dapat diakses dari browser.

## Catatan Integrasi dan Keamanan

URL API dan token pada versi ini dikonfigurasi langsung di file HTML untuk kebutuhan demonstrasi akademik. Pada sistem produksi, konfigurasi tersebut sebaiknya dipindahkan ke backend-for-frontend atau mekanisme environment/runtime config agar token tidak terekspos di browser.

## Tim

- Darryl Rayhananta Adenan — 18223042
- Muhammad Adam Mirza — 18223015

