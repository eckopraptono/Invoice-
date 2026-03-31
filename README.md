# 📄 Invoice Manager - DotCom Partner

Invoice digital tool yang modern dan responsive untuk membuat, mengedit, dan export invoice dalam format PDF dengan hasil sempurna di halaman A4.

---

## ✨ Fitur Utama

### 1. **Invoice Number Otomatis**
- Format: `INV/YYYY/MMDD` (berdasarkan tanggal penerbitan)
- Auto-update saat tanggal berubah
- Nama file PDF: `INV-YYYY-MMDD-Invoice.pdf`

### 2. **Tanggal Fleksibel**
- Tanggal penerbitan (input manual)
- Jatuh tempo otomatis +7 hari

### 3. **Data Client Editable**
- Nama, email, kontak, alamat → editable
- Nomor PO (opsional)
- Catatan pembayaran (max 2 baris)

### 4. **Rekening Bank Dinamis**
- Bank: BCA (Bank Central Asia)
- Nomor rekening editable
- Nama pemilik rekening

### 5. **Line Items Unlimited**
- ✅ Tambah item unlimited dengan tombol **"+"**
- ✅ Edit deskripsi panjang (textarea auto-resize)
- ✅ Qty & Harga otomatis kalkulasi total per item
- ✅ Hapus item dengan tombol **🗑️** (minimal 1 item)
- ✅ **Optimal fit 1 halaman A4 bahkan dengan 5 item penuh**

### 6. **PPN Toggle (Pajak 11%)**
- Switch on/off PPN (Pajak Pertambahan Nilai)
- Kalkulasi otomatis: Subtotal + (11% PPN) = Total Akhir
- Default: OFF

### 7. **Status Badge - 3 Pilihan**
- Klik untuk cycle: "Menunggu Pembayaran" → "Lunas Terbayar" → "Dibatalkan"
- Warna: Kuning (waiting), Hijau (paid), Merah (cancelled)

### 8. **Export PDF Sempurna**
- 📄 **Fit 1 halaman A4** (210mm × 297mm portrait)
- 🎨 Layout rapi & professional
- 🔧 HTML2PDF optimized: scale 1.2, windowWidth 794px
- 📱 Responsive: auto-adapt dari screen ke A4 print
- 📛 Nama file otomatis dari invoice number
- ⚡ Quality JPEG 0.98 untuk hasil sharp

### 9. **Reset Invoice**
- Tombol reset untuk clear semua data (dengan konfirmasi)

---

## 🎯 Cara Penggunaan

### Input Invoice

1. **Tanggal & Nomor**
   - Isi `Tgl. Terbit` → Invoice number auto-generate
   - `Jatuh Tempo` default +7 hari (edit jika perlu)

2. **Info Client**
   - Nama client, email, kontak, alamat (editable)
   - PO (opsional)

3. **Rekening Pembayaran**
   - Bank: BCA (fixed)
   - Nomor rekening & nama owner (editable)
   - Catatan: max 2 baris

4. **Line Items - Produk/Jasa**
   - **Deskripsi**: klik textarea, tulis deskripsi panjang (auto-resize)
   - **Qty**: jumlah unit
   - **Harga**: harga per unit (Rp)
   - **Total**: auto = qty × harga
   - **Tombol +**: tambah item baru
   - **Tombol 🗑️**: hapus item (minimal 1)

5. **PPN (Pajak)**
   - Toggle switch untuk aktifkan/nonaktifkan PPN 11%
   - Lihat perubahan langsung di total akhir

6. **Status**
   - Klik badge untuk ganti status
   - 3 pilihan: Menunggu / Lunas / Dibatalkan

### Export ke PDF

1. Klik tombol **"Cetak Satu Halaman"**
2. PDF ter-download otomatis
3. Nama file: `INV-YYYY-MMDD-Invoice.pdf`
4. Siap print atau email ke client

---

## 🔧 Spesifikasi Teknis

### Tech Stack
- **HTML5** dengan lang="id" (Indonesian)
- **CSS3** (custom properties, flexbox, grid)
- **Vanilla JavaScript** (no framework dependencies)
- **html2pdf.js** v0.10.1 (PDF export)
- **Google Fonts**: Plus Jakarta Sans, Space Grotesk

### Responsive Design
- 📱 Mobile: Flexible layout
- 💻 Desktop: Max-width 850px, centered
- 📄 Print: Optimized A4 210mm × 297mm

### File Structure
```
index.html (single file, semua CSS + JS integrated)
```

### CSS Variables Theme
```
--primary: #2563eb (Biru primary)
--navy: #0f172a (Navy/Hitam)
--border: #f1f5f9 (Abu-abu muda)
--text-light: #94a3b8 (Teks gelap)
--bg-body: #f8fafc (Background)
```

---

## 📊 Optimasi PDF

| Parameter | Nilai | Deskripsi |
|-----------|-------|-----------|
| **Format** | A4 Portrait | 210mm × 297mm |
| **Scale** | 1.2 | Presisi render tanpa distortion |
| **Window Width** | 794px | A4 width responsive |
| **Margin** | 0mm | Full page utilization |
| **Image Quality** | JPEG 0.98 | Sharp & tidak blur |
| **Max Content** | 5 items | Fit 1 halaman A4 |

### Print Mode Optimasi
- Content padding: 18px × 22px
- Section gap: 12px (reduce dari 16-20px)
- Meta item: 3px (reduce dari 6px)
- Signature section: 20px gap (reduce dari 40px)
- Font size (print): 7-10px (dari 10-12px)

---

## 🎨 UI/UX Details

### Warna Status Badge
| Status | Warna | Hex Code |
|--------|-------|----------|
| Menunggu Pembayaran | Kuning | #fffbeb |
| Lunas Terbayar | Hijau | #f0fdf4 |
| Dibatalkan | Merah | #fef2f2 |

### Font Sizes
- **Heading**: 22px (brand)
- **Invoice #**: 36px (Space Grotesk)
- **Body text**: 10-11px
- **Print**: 7-10px (scaled down)

### Spacing
- Gap antar section: 20px
- Padding container: 30px (screen), 18px (print)
- Table row spacing: 4px

---

## ✅ Quality Assurance

### Tested Scenarios
- ✅ 1 item pada 1 halaman
- ✅ 5 items pada 1 halaman (fit A4)
- ✅ PPN on/off
- ✅ Status cycle 3x
- ✅ Invoice number auto-update
- ✅ PDF export tanpa terpotong
- ✅ Mobile responsive
- ✅ All fields editable

---

## 🐛 Troubleshoot

### Q: PDF terpotong/tidak fit 1 halaman?
**A:** ✅ Fixed di v1.2. Gunakan:
- Scale: 1.2 (optimal)
- WindowWidth: 794px (A4 width)
- Margin: 0mm

### Q: Invoice number tidak update?
**A:** 
- Pastikan input tanggal terisi (YYYY-MM-DD)
- Trigger onChange akan auto-update

### Q: Item tidak muncul?
**A:**
- Refresh browser (Ctrl+R)
- Pastikan qty > 0 dan harga terisi

### Q: PPN tidak terlihat?
**A:**
- Klik toggle switch untuk aktifkan
- Perhatikan section "PAJAK PERTAMBAHAN NILAI"

### Q: Font jelek saat print?
**A:**
- Browser zoom: 100% (jangan 90% atau 110%)
- Scale 1.2 di html2pdf sudah optimal

---

## 📝 Update History

### v1.2 - PDF Fix (Mar 31, 2026)
- ✅ Fixed PDF export (terpotong → sempurna)
- ✅ Scale 1.2 + WindowWidth 794px (A4 accurate)
- ✅ Optimasi padding print (18px × 22px)
- ✅ Signature section compact (20px gap)
- ✅ Fit 1 halaman A4 dengan 5 item full
- ✅ Filename otomatis dari invoice number
- ✅ Error handling PDF export

### v1.1 - Features (Mar 31, 2026)
- ✅ Invoice number otomatis (INV/YYYY/MMDD)
- ✅ Dynamic line items (add/remove unlimited)
- ✅ PPN toggle 11%
- ✅ Status badge cycle 3 kondisi
- ✅ Responsive design

### v1.0 - Initial Release
- ✅ Basic invoice template
- ✅ HTML2PDF export
- ✅ Indonesian UI

---

## 📞 Support

Untuk pertanyaan atau issue, silakan buka ticket atau hubungi DotCom Partner.

**Last Updated**: March 31, 2026  
**Version**: 1.2  
**Status**: ✅ Production Ready