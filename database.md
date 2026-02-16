# Dokumentasi Database

Database yang digunakan pada Sistem Peminjaman Ruangan Kampus adalah **SQLite**.

---

## Teknologi Database

- Database: SQLite
- ORM: Entity Framework Core
- File database: `RoomBooking.db`

---

## Struktur Data Utama

Sistem memiliki satu entitas utama:

### Tabel: PeminjamanRuangan
Field, Tipe Data, Keterangan
Id: int (Primary Key) 
NamaPeminjam: string (Nama peminjam ruangan)
NRP: string (Nomor induk mahasiswa)
Ruangan: string (Nama/kode ruangan)
Tanggal: date (Tanggal peminjaman)
JamMulai: string (Jam mulai penggunaan)
JamSelesai: string (Jam selesai penggunaan)
Keperluan: string (Alasan peminjaman)
Status: string (Menunggu / Disetujui / Ditolak)

---

## Migration & Seeder

Database dibuat menggunakan migration:

```bash
dotnet ef migrations add InitialCreate
dotnet ef database update
