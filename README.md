# II3160 Final Project - LogiTrack

**Tugas Ujian Akhir Semester**  
**Mata Kuliah:** II3160 - Teknologi Sistem Terintegrasi  

---

## Anggota Kelompok:
| Nama | NIM |
|------|-----|
| Darryl Rayhananta Adenan | 18223042 |
| Muhammad Adam Mirza | 18223015 |

---

## Project Overview
Website ini adalah antarmuka pengguna (Integrated UI) untuk sistem manajemen logistik yang mengintegrasikan dua layanan mikro (microservices):
1. **Warehouse Service**: Mengelola inventaris barang.
2. **Shipment Service**: Mengelola status pengiriman dan pelacakan paket.

### Fitur Utama
- **Dashboard (`index.html`)**: Menampilkan ringkasan statistik sistem secara real-time (Total Inventory, In Transit, Pending, Delivered).
- **Inventory Management (`inventory.html`)**: 
  - Melihat daftar stok barang di gudang.
  - Menambahkan barang baru.
  - Memulai proses pengiriman ke kurir.
- **Shipment Tracking (`shipment.html`)**: 
  - Melacak status paket menggunakan nomor resi.
  - Memperbarui lokasi paket.
  - Menandai paket sebagai "Delivered".

## Tech Stack
- **Frontend**: HTML5, CSS3
- **Styling**: TailwindCSS (via CDN), Custom CSS (Glassmorphism & Eco-Futuristic Theme)
- **Icons**: Lucide Icons
- **Font**: Plus Jakarta Sans

---

## Cara Menjalankan

### Prasyarat
- Browser modern (Chrome, Edge, Firefox)
- Koneksi internet (untuk TailwindCSS CDN dan Lucide Icons)
- Backend services sudah berjalan dan dapat diakses

### Langkah-langkah

#### 1. Clone Repository
```bash
git clone https://github.com/username/II3160-FinalProject-18223042.git
cd II3160-FinalProject-18223042
```

#### 2. Jalankan dengan Live Server (Rekomendasi)
**Menggunakan VS Code:**
1. Install extension **Live Server**
2. Klik kanan pada `index.html`
3. Pilih **Open with Live Server**
4. Browser akan terbuka otomatis di `http://127.0.0.1:5500`

**Atau menggunakan Python:**
```bash
# Python 3
python -m http.server 5500

# Buka browser ke http://localhost:5500
```

**Atau menggunakan Node.js:**
```bash
npx serve .

# Buka browser ke http://localhost:3000
```

#### 3. Akses Aplikasi
| Halaman | URL | Fungsi |
|---------|-----|--------|
| Dashboard | `index.html` | Lihat statistik sistem |
| Inventory | `inventory.html` | Kelola package |
| Shipment | `shipment.html` | Track pengiriman |

---

## API Endpoints

### Warehouse API (18223015)
| Method | Endpoint | Keterangan |
|--------|----------|------------|
| GET | `/api/packages/` | Ambil semua package |
| POST | `/api/packages/` | Buat package baru |
| GET | `/api/packages/{id}/` | Detail package |
| PATCH | `/api/packages/{id}/` | Update package |

### Shipment API (18223042)
| Method | Endpoint | Keterangan |
|--------|----------|------------|
| GET | `/api/shipments/` | Ambil semua shipment |
| POST | `/api/shipments/` | Buat shipment baru |
| GET | `/api/shipments/{id}/` | Detail shipment |
| PATCH | `/api/shipments/{id}/` | Update status/lokasi |

### Authorization
Semua API endpoint memerlukan header:
```
Authorization: Bearer {API_TOKEN}
```

---

## Struktur Folder
```
II3160-FinalProject-18223042/
├── index.html        # Dashboard
├── inventory.html    # Inventory Management
├── shipment.html     # Shipment Tracking
├── style.css         # Custom Styles
└── README.md         # Dokumentasi
```
