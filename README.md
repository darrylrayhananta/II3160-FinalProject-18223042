# II3160 Final Project - LogiTrack

**Tugas Ujian Akhir Semester**  
**Mata Kuliah:** II3160 - Teknologi Sistem Terintegrasi  

---

## Dibuat Oleh:
**Nama:** Darryl Rayhananta Adenan  
**NIM:** 18223042  

---

## Project Overview
Website ini adalah antarmuka pengguna (Integrated UI) untuk sistem manajemen logistik yang mengintegrasikan dua layanan mikro (microservices):
1. **Warehouse Service** (Port 8000): Mengelola inventaris barang.
2. **Shipment Service** (Port 8001): Mengelola status pengiriman dan pelacakan paket.

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

## Cara Menjalankan
1. Pastikan kedua backend service (Warehouse & Shipment) sudah berjalan pada port masing-masing:
   - Warehouse Service: `http://localhost:8000`
   - Shipment Service: `http://localhost:8001`
2. Buka file `index.html` menggunakan browser modern (Chrome, Edge, Firefox).
3. Navigasi melalui menu di bagian atas untuk mengakses fitur Inventory dan Shipment.
