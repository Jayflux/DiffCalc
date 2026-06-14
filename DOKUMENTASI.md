# Dokumentasi Aplikasi Kalkulator Turunan Fungsi

## 📋 Daftar Isi
1. [Gambaran Umum](#gambaran-umum)
2. [Fitur Utama](#fitur-utama)
3. [Cara Penggunaan](#cara-penggunaan)
4. [Jenis Fungsi yang Didukung](#jenis-fungsi-yang-didukung)
5. [Teori Matematika](#teori-matematika)
6. [Panduan Teknis](#panduan-teknis)
7. [Contoh Penggunaan](#contoh-penggunaan)

---

## Gambaran Umum

**Kalkulator Turunan Fungsi** adalah aplikasi web interaktif yang dirancang untuk:
- Menghitung turunan (derivative) dari berbagai jenis fungsi matematika
- Menampilkan langkah-langkah penyelesaian secara detail
- Memberikan penjelasan untuk setiap aturan turunan yang digunakan
- Membantu pemahaman konsep kalkulus diferensial

Aplikasi ini dibangun menggunakan:
- **Frontend**: HTML5, CSS3, JavaScript ES6+
- **Parsing**: Abstract Syntax Tree (AST) untuk menganalisis ekspresi matematika
- **Algoritma**: Recursive derivative calculation dengan simplification

---

## Fitur Utama

### 1. Input Fungsi Fleksibel
- Mendukung notasi matematika standar
- Menggunakan `^` untuk pangkat (power)
- Menggunakan `*` untuk perkalian
- Menggunakan `/` untuk pembagian
- Contoh: `x^2 + 3*x + 5`

### 2. Library Fungsi Lengkap
Mendukung jenis-jenis fungsi:
- **Polynomial**: `x^2`, `3*x^3 + 2*x`
- **Trigonometri**: `sin(x)`, `cos(x)`, `tan(x)`
- **Eksponensial**: `exp(x)` untuk e^x
- **Logaritma**: `log(x)` untuk ln(x)
- **Akar**: `sqrt(x)` untuk √x
- **Kombinasi**: `x^2 * sin(x)`, `exp(x) * cos(x)`

### 3. Langkah-Langkah Terperinci
- Menampilkan setiap aturan turunan yang diterapkan
- Navigasi antar langkah dengan tombol Sebelumnya/Selanjutnya
- Counter langkah untuk memudahkan tracking

### 4. Antarmuka Interaktif
- Tombol contoh cepat untuk fungsi populer
- Tampilan responsif (mobile-friendly)
- Verifikasi hasil dengan penjelasan matematis
- Error handling yang jelas dan informatif

### 5. Simplifikasi Otomatis
- Menghilangkan suku-suku yang bernilai 0
- Menghilangkan koefisien 1 yang tidak perlu
- Menyederhanakan pangkat (^0 = 1, ^1 = basis)

---

## Cara Penggunaan

### Langkah 1: Buka Aplikasi
Buka file `derivative_calculator.html` di browser (Chrome, Firefox, Safari, Edge, dll)

### Langkah 2: Masukkan Fungsi
```
Contoh input:
- x^2                    → f(x) = x²
- 3*x^3 + 2*x           → f(x) = 3x³ + 2x
- sin(x)                 → f(x) = sin(x)
- exp(x) * cos(x)        → f(x) = e^x · cos(x)
```

### Langkah 3: Klik "Hitung Turunan"
Aplikasi akan:
- Memparse input Anda
- Menghitung turunan
- Menampilkan hasil dan langkah-langkah

### Langkah 4: Pelajari Langkah-Langkahnya
- Baca deskripsi setiap langkah
- Lihat formula yang diterapkan
- Gunakan tombol navigasi untuk menelusuri proses

### Langkah 5: Verifikasi Hasil
Bagian "Verifikasi Hasil" menampilkan:
- Fungsi asli f(x)
- Turunan f'(x)
- Catatan untuk pemeriksaan lebih lanjut

---

## Jenis Fungsi yang Didukung

### A. Fungsi Polynomial
**Aturan yang diterapkan**: Power Rule

Rumus: d/dx[x^n] = n·x^(n-1)

**Contoh:**
- f(x) = x² → f'(x) = 2x
- f(x) = x³ → f'(x) = 3x²
- f(x) = 5x⁴ → f'(x) = 20x³

### B. Fungsi Polynomial Berlapis
**Aturan yang diterapkan**: Sum/Difference Rule, Power Rule

Rumus: d/dx[f(x) ± g(x)] = f'(x) ± g'(x)

**Contoh:**
- f(x) = x² + 3x + 2 → f'(x) = 2x + 3
- f(x) = 4x³ - 2x² + x → f'(x) = 12x² - 4x + 1

### C. Fungsi Trigonometri
**Aturan yang diterapkan**: Chain Rule + Trigonometric Derivatives

Rumus dasar:
- d/dx[sin(x)] = cos(x)
- d/dx[cos(x)] = -sin(x)
- d/dx[tan(x)] = sec²(x) = 1/cos²(x)

**Contoh:**
- f(x) = sin(x) → f'(x) = cos(x)
- f(x) = cos(x²) → f'(x) = -2x·sin(x²)

### D. Fungsi Eksponensial
**Aturan yang diterapkan**: Chain Rule + Exponential Rule

Rumus dasar:
- d/dx[e^x] = e^x
- d/dx[e^u] = e^u · du/dx

**Contoh:**
- f(x) = e^x → f'(x) = e^x
- f(x) = e^(2x) → f'(x) = 2e^(2x)

### E. Fungsi Logaritma
**Aturan yang diterapkan**: Chain Rule + Logarithmic Rule

Rumus dasar:
- d/dx[ln(x)] = 1/x
- d/dx[ln(u)] = (1/u)·du/dx

**Contoh:**
- f(x) = ln(x) → f'(x) = 1/x
- f(x) = ln(x²) → f'(x) = 2/x

### F. Fungsi Komposit (Product/Quotient)
**Aturan yang diterapkan**: Product Rule, Quotient Rule

**Product Rule:**
d/dx[u·v] = u'·v + u·v'

**Quotient Rule:**
d/dx[u/v] = (u'·v - u·v')/v²

**Contoh:**
- f(x) = x²·sin(x) → f'(x) = 2x·sin(x) + x²·cos(x)
- f(x) = sin(x)/x → f'(x) = (x·cos(x) - sin(x))/x²

---

## Teori Matematika

### 1. Pengertian Turunan
Turunan adalah laju perubahan sesaat dari suatu fungsi. Secara matematis:

f'(x) = lim(h→0) [f(x+h) - f(x)] / h

### 2. Aturan-Aturan Turunan

#### Power Rule (Aturan Pangkat)
d/dx[x^n] = n·x^(n-1)

#### Sum/Difference Rule (Aturan Penjumlahan/Pengurangan)
d/dx[f(x) ± g(x)] = f'(x) ± g'(x)

#### Product Rule (Aturan Perkalian)
d/dx[f(x)·g(x)] = f'(x)·g(x) + f(x)·g'(x)

#### Quotient Rule (Aturan Pembagian)
d/dx[f(x)/g(x)] = [f'(x)·g(x) - f(x)·g'(x)] / [g(x)]²

#### Chain Rule (Aturan Rantai)
d/dx[f(g(x))] = f'(g(x))·g'(x)

#### Trigonometric Derivatives
- d/dx[sin(x)] = cos(x)
- d/dx[cos(x)] = -sin(x)
- d/dx[tan(x)] = sec²(x)

#### Exponential & Logarithmic
- d/dx[e^x] = e^x
- d/dx[ln(x)] = 1/x

### 3. Interpretasi Geometris
- Turunan f'(x) mewakili **kemiringan garis singgung** kurva f(x) di titik x
- Jika f'(x) > 0: fungsi sedang naik
- Jika f'(x) < 0: fungsi sedang turun
- Jika f'(x) = 0: titik kritisi (maksimum/minimum lokal)

---

## Panduan Teknis

### Struktur Kode

#### 1. Class DerivativeCalculator
Menangani:
- **tokenize()**: Mengubah string input menjadi token
- **parse()**: Mengubah token menjadi AST (Abstract Syntax Tree)
- **derivative()**: Menghitung turunan secara recursive
- **simplify()**: Menyederhanakan hasil
- **astToString()**: Mengubah AST kembali ke string

#### 2. AST (Abstract Syntax Tree)
Struktur data untuk merepresentasikan ekspresi matematika:

```javascript
// Contoh: 2x + 3
{
  type: 'binary',
  op: '+',
  left: {
    type: 'binary',
    op: '*',
    left: { type: 'number', value: 2 },
    right: { type: 'variable', name: 'x' }
  },
  right: { type: 'number', value: 3 }
}
```

#### 3. Node Types dalam AST
- **number**: Konstanta numerik
- **variable**: Variabel (x, y, dll)
- **binary**: Operasi biner (+, -, *, /)
- **power**: Pangkat (^)
- **function**: Fungsi (sin, cos, exp, log, dll)
- **unary**: Operasi unary (-)

### Browser Requirements
- **Minimum**: IE11 (dengan polyfill)
- **Recommended**: Modern browsers (Chrome 60+, Firefox 55+, Safari 11+)
- **Fitur yang diperlukan**: 
  - ES6+ support (arrow functions, const/let, classes)
  - DOM API
  - Fetch API (untuk future expansion)

---

## Contoh Penggunaan

### Contoh 1: Polynomial Sederhana
```
Input:  x^2 + 3*x + 2
Output: f'(x) = 2*x + 3

Langkah-langkah:
1. Gunakan sum rule: d/dx[u + v] = du/dx + dv/dx
2. d/dx[x^2] = 2*x (power rule)
3. d/dx[3*x] = 3 (power rule)
4. d/dx[2] = 0 (constant rule)
5. Hasil: 2*x + 3 + 0 = 2*x + 3
```

### Contoh 2: Product Rule
```
Input:  x^2 * sin(x)
Output: f'(x) = 2*x*sin(x) + x^2*cos(x)

Langkah-langkah:
1. Gunakan product rule: d/dx[u*v] = u'*v + u*v'
2. u = x^2, u' = 2*x
3. v = sin(x), v' = cos(x)
4. Hasil: 2*x*sin(x) + x^2*cos(x)
```

### Contoh 3: Chain Rule
```
Input:  sin(x^2)
Output: f'(x) = 2*x*cos(x^2)

Langkah-langkah:
1. Gunakan chain rule: d/dx[f(g(x))] = f'(g(x))*g'(x)
2. f(u) = sin(u), f'(u) = cos(u)
3. g(x) = x^2, g'(x) = 2*x
4. Hasil: cos(x^2)*2*x = 2*x*cos(x^2)
```

### Contoh 4: Quotient Rule
```
Input:  sin(x) / x
Output: f'(x) = (cos(x)*x - sin(x)) / x^2

Langkah-langkah:
1. Gunakan quotient rule: d/dx[u/v] = (u'*v - u*v') / v^2
2. u = sin(x), u' = cos(x)
3. v = x, v' = 1
4. Hasil: (cos(x)*x - sin(x)*1) / x^2 = (cos(x)*x - sin(x)) / x^2
```

### Contoh 5: Exponential dan Logaritma
```
Input:  exp(x) * log(x)
Output: f'(x) = exp(x)*log(x) + exp(x)/x

Langkah-langkah:
1. Gunakan product rule
2. d/dx[exp(x)] = exp(x)
3. d/dx[log(x)] = 1/x
4. Hasil: exp(x)*log(x) + exp(x)*(1/x)
```

---

## Keterbatasan & Catatan

### Keterbatasan Saat Ini
1. **Tidak mendukung**: u^v (eksponensial dengan basis dan pangkat variabel)
2. **Simplifikasi terbatas**: Hasil mungkin tidak sepenuhnya simplified
3. **Variabel ganda**: Hanya mendukung turunan terhadap x
4. **Fungsi khusus**: Tidak mendukung arcsin, arccos, sinh, cosh, dll (bisa ditambahkan)

### Catatan Implementasi
- Parsing menggunakan teknik **recursive descent parser**
- Derivative calculation bersifat **symbolic** (bukan numerical)
- AST memungkinkan extension mudah untuk fungsi-fungsi baru

---

## Pengembangan Lebih Lanjut

### Fitur yang Bisa Ditambahkan
1. **Turunan Kedua & Lebih Tinggi** (higher derivatives)
2. **Integral** (antiderivative)
3. **Taylor Series Expansion**
4. **Numerical Evaluation** (hitung nilai f'(a) untuk x tertentu)
5. **Grafik Visualisasi** (plot f(x) dan f'(x))
6. **Export PDF** (simpan hasil ke PDF)
7. **Multilingual Support** (Inggris, Mandarin, dll)
8. **Mobile App** (React Native / Flutter)

### Optimisasi Potential
1. Caching hasil turunan untuk query yang sama
2. WebWorker untuk fungsi kompleks
3. Progressive Web App (PWA) untuk offline access

---

## Referensi Matematika

1. **Stewart, James**. *Calculus: Early Transcendentals*
2. **Larson, Ron**. *Calculus* (9th Edition)
3. **MIT OpenCourseWare**: Single Variable Calculus
4. **Khan Academy**: Calculus Derivatives Section

---

## Troubleshooting

| Masalah | Solusi |
|---------|--------|
| "Unexpected character" | Pastikan menggunakan `*` untuk perkalian, `^` untuk pangkat |
| Output terlalu panjang | Coba fungsi yang lebih sederhana terlebih dahulu |
| Error di browser lama | Update browser ke versi terbaru |
| Hasil terlihat aneh | Verifikasi input Anda dan periksa langkah-langkahnya |

---

**Dibuat untuk**: Studi Kasus Aplikasi Kalkulator Turunan Fungsi
**Bahasa**: JavaScript (Vanilla ES6+)
**Format**: Single HTML File (No Dependencies)
**Lisensi**: Free to Use & Modify
