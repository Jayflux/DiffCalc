# 📐 Kalkulator Turunan Fungsi (DiffCalc)

> Aplikasi web interaktif berbasis JavaScript untuk menghitung turunan (derivative) fungsi matematika secara simbolik, dilengkapi langkah-langkah penyelesaian yang terperinci.

---

## 📋 Daftar Isi

1. [Deskripsi Project](#deskripsi-project)
2. [Quick Start](#quick-start)
3. [Cara Penggunaan](#cara-penggunaan)
4. [Fungsi yang Didukung](#fungsi-yang-didukung)
5. [Aturan Turunan](#aturan-turunan)
6. [Teori Kalkulus Diferensial](#teori-kalkulus-diferensial)
7. [Test Cases](#test-cases)
8. [Panduan Teknis](#panduan-teknis)
9. [Troubleshooting](#troubleshooting)
10. [Roadmap](#roadmap)
11. [Referensi](#referensi)
12. [Kesimpulan](#kesimpulan)

---

## Deskripsi Project

**Kalkulator Turunan Fungsi** adalah aplikasi web yang membantu siswa dan profesional untuk:

- Menghitung turunan dari fungsi matematika secara otomatis
- Memahami proses penghitungan melalui langkah-langkah yang terperinci
- Belajar berbagai aturan diferensial (power rule, chain rule, product rule, dll)

**Teknologi yang digunakan:** HTML5 · CSS3 · JavaScript ES6+ (tanpa dependensi eksternal)

**Fitur unggulan:**
- ✅ Fungsi polynomial, trigonometri, eksponensial, logaritma
- ✅ Step-by-step explanation dengan navigasi antar langkah
- ✅ Offline ready — single HTML file, tidak butuh internet
- ✅ Responsif (desktop & mobile)
- ✅ Error handling yang informatif

**Statistik aplikasi:**

| Metrik | Nilai |
|---|---|
| File Size | < 200KB |
| Load Time | < 1 detik |
| Supported Functions | 12+ types |
| Supported Rules | 11+ rules |
| Test Cases | 50+ |
| Dependencies | 0 |

---

## Quick Start

### Persyaratan Sistem

| Requirement | Detail |
|---|---|
| Browser | Chrome 60+, Firefox 55+, Safari 11+, Edge 79+ |
| OS | Windows, macOS, Linux, iOS, Android |
| Internet | Tidak diperlukan (fully offline) |
| Instalasi | Tidak ada! |

### Langkah Penggunaan

**1. Download/Clone repo:**
```bash
git clone https://github.com/Jayflux/DiffCalc.git
```

**2. Buka di browser:**
```
Double-click: derivative_calculator.html
```

**3. Coba langsung:**
```
Input:  x^2
Klik:   "Hitung Turunan"
Output: 2*x  ✅
```

---

## Cara Penggunaan

### Syntax Input

| Operator | Simbol | Contoh |
|---|---|---|
| Pangkat | `^` | `x^2` untuk x² |
| Perkalian | `*` | `3*x` untuk 3x |
| Pembagian | `/` | `x/2` |
| Penjumlahan | `+` | `x + 1` |
| Pengurangan | `-` | `x - 1` |
| Grouping | `()` | `(x+1)^2` |

### Input Valid vs Tidak Valid

```
✅ VALID:
x^2
3*x^3 + 2*x
sin(x)
cos(x) + x^2
exp(x) * sin(x)
log(x) / x
sqrt(x^2 + 1)

❌ TIDAK VALID:
2x          → tulis 2*x
x2          → tulis x^2
ln(x)       → tulis log(x)
e^x         → tulis exp(x)
sinx        → tulis sin(x)
```

### Fitur Aplikasi

**1. Input Fleksibel** — mendukung berbagai format fungsi matematika dengan auto-correction spacing dan real-time validation.

**2. Step-by-Step Explanation** — setiap langkah ditampilkan dengan jelas beserta aturan yang digunakan. Navigasi dengan tombol Previous/Next.

**3. Simplifikasi Otomatis** — menghilangkan suku bernilai 0, koefisien 1 yang redundan, dan menyederhanakan pangkat.

**4. Error Handling** — pesan error yang jelas disertai saran perbaikan.

---

## Fungsi yang Didukung

### Trigonometri
```
sin(x)   // Sinus
cos(x)   // Cosinus
tan(x)   // Tangen
```

### Eksponensial & Logaritma
```
exp(x)   // e^x
log(x)   // ln(x) — natural logarithm
sqrt(x)  // √x
```

### Polynomial
```
x^2
3*x^3 + 2*x - 1
(x+1)^4
```

### Kombinasi Kompleks
```
exp(x) * sin(x)
log(x) / x
sin(x^2 + 1)
x^2 * cos(x) + log(x)
```

---

## Aturan Turunan

Semua aturan berikut didukung oleh aplikasi:

| Aturan | Formula | Status |
|---|---|---|
| Power Rule | d/dx[x^n] = n·x^(n-1) | ✅ |
| Constant Rule | d/dx[c] = 0 | ✅ |
| Sum Rule | d/dx[f+g] = f' + g' | ✅ |
| Difference Rule | d/dx[f-g] = f' - g' | ✅ |
| Product Rule | d/dx[f·g] = f'·g + f·g' | ✅ |
| Quotient Rule | d/dx[f/g] = (f'·g - f·g')/g² | ✅ |
| Chain Rule | d/dx[f(g(x))] = f'(g)·g' | ✅ |
| Sin Rule | d/dx[sin(x)] = cos(x) | ✅ |
| Cos Rule | d/dx[cos(x)] = -sin(x) | ✅ |
| Tan Rule | d/dx[tan(x)] = sec²(x) | ✅ |
| Exp Rule | d/dx[e^x] = e^x | ✅ |
| Log Rule | d/dx[ln(x)] = 1/x | ✅ |
| Sqrt Rule | d/dx[√x] = 1/(2√x) | ✅ |

---

## Teori Kalkulus Diferensial

### Definisi Turunan

Turunan dari fungsi f(x) didefinisikan sebagai:

```
f'(x) = lim(h→0) [f(x+h) - f(x)] / h
```

**Interpretasi geometris:**
- f'(x) adalah kemiringan garis singgung kurva y = f(x) di titik x
- f'(x) > 0 → fungsi naik
- f'(x) < 0 → fungsi turun
- f'(x) = 0 → titik kritis (kemungkinan maksimum/minimum lokal)

### Notasi Turunan

| Notasi | Penggunaan |
|---|---|
| f'(x) | Paling umum |
| df/dx | Leibniz notation |
| dy/dx | Untuk y = f(x) |
| y' | Singkatan |

### Penjelasan Tiap Aturan

**Power Rule:**
```
d/dx[x²] = 2x
d/dx[x³] = 3x²
d/dx[5x⁴] = 20x³
```

**Sum/Difference Rule:**
```
d/dx[x² + 3x] = 2x + 3
d/dx[sin(x) - cos(x)] = cos(x) + sin(x)
```

**Product Rule** — d/dx[u·v] = u'·v + u·v':
```
d/dx[x · sin(x)]
  u = x, u' = 1 | v = sin(x), v' = cos(x)
  = sin(x) + x·cos(x)
```

**Quotient Rule** — d/dx[u/v] = (u'v - uv') / v²:
```
d/dx[sin(x)/x]
  u = sin(x), u' = cos(x) | v = x, v' = 1
  = (cos(x)·x - sin(x)) / x²
```

**Chain Rule** — d/dx[f(g(x))] = f'(g(x)) · g'(x):
```
d/dx[sin(x²)]
  outer: sin(u), f'(u) = cos(u)
  inner: x², g'(x) = 2x
  = cos(x²) · 2x = 2x·cos(x²)
```

**Trigonometri:**
```
d/dx[sin(x)]  = cos(x)
d/dx[cos(x)]  = -sin(x)
d/dx[tan(x)]  = 1/cos²(x)
```

**Eksponensial & Logaritma:**
```
d/dx[e^x]   = e^x    ← satu-satunya fungsi yang turunannya = dirinya sendiri
d/dx[ln(x)] = 1/x
d/dx[e^(2x)] = 2·e^(2x)  (chain rule)
d/dx[ln(x²)] = 2/x       (chain rule)
```

### Aplikasi Turunan

**Mencari titik kritis (optimisasi):**
```
f(x) = x² - 4x + 3
f'(x) = 2x - 4

f'(x) = 0 → x = 2
f(2) = -1  → (2, -1) adalah minimum lokal
```

**Linear Approximation** — f(x) ≈ f(a) + f'(a)(x-a):
```
Approximate √4.1 dengan f(x) = √x, a = 4
f(4) = 2, f'(4) = 1/4

√4.1 ≈ 2 + (1/4)(0.1) = 2.025
Nilai aktual: 2.0248... ✓
```

### Tips Diferensiasi

**Tip 1: Expand dulu jika memungkinkan**
```
f(x) = (x+1)²
→ Expand jadi x² + 2x + 1
→ f'(x) = 2x + 2  (jauh lebih mudah dari product rule)
```

**Tip 2: Sederhanakan sebelum turunkan**
```
f(x) = (2x² + 4x) / (2x) = x + 2
f'(x) = 1
```

**Tip 3: Chain Rule berlapis**
```
d/dx[sin²(x)] = d/dx[(sin(x))²]
outer: u², f'(u) = 2u
inner: sin(x), g'(x) = cos(x)
= 2·sin(x)·cos(x) = sin(2x)
```

---

## Test Cases

### Level 1 — Dasar (Polynomial)

| Input | Output | Aturan |
|---|---|---|
| `5` | `0` | Constant rule |
| `x` | `1` | Power rule |
| `x^2` | `2*x` | Power rule |
| `x^3` | `3*x^2` | Power rule |
| `x^2 + 3*x + 2` | `2*x + 3` | Sum + power rule |
| `5*x^4` | `20*x^3` | Power rule |
| `4*x^3 - 2*x^2 + x - 7` | `12*x^2 - 4*x + 1` | Sum/diff + power rule |

### Level 2 — Trigonometri & Eksponensial

| Input | Output | Aturan |
|---|---|---|
| `sin(x)` | `cos(x)` | Trig rule |
| `cos(x)` | `-sin(x)` | Trig rule |
| `tan(x)` | `1/cos(x)^2` | Trig rule |
| `exp(x)` | `exp(x)` | Exp rule |
| `log(x)` | `1/x` | Log rule |
| `x^2 + sin(x)` | `2*x + cos(x)` | Sum + trig |

### Level 3 — Chain Rule

| Input | Output |
|---|---|
| `sin(x^2)` | `2*x*cos(x^2)` |
| `cos(2*x)` | `-2*sin(2*x)` |
| `exp(2*x)` | `2*exp(2*x)` |
| `exp(x^2)` | `2*x*exp(x^2)` |
| `log(x^2)` | `2/x` |
| `log(sin(x))` | `cos(x)/sin(x)` |

### Level 4 — Product & Quotient Rule

| Input | Output |
|---|---|
| `x * sin(x)` | `sin(x) + x*cos(x)` |
| `x^2 * sin(x)` | `2*x*sin(x) + x^2*cos(x)` |
| `sin(x) / x` | `(cos(x)*x - sin(x)) / x^2` |
| `x^2 / (x + 1)` | `(2*x*(x+1) - x^2) / (x+1)^2` |
| `x^2 * exp(x)` | `2*x*exp(x) + x^2*exp(x)` |

### Level 5 — Kombinasi Kompleks

| Input | Output |
|---|---|
| `exp(x) * cos(x)` | `exp(x)*cos(x) - exp(x)*sin(x)` |
| `x^2 * log(x)` | `2*x*log(x) + x` |
| `(x^2 + 1) / (x + 1)` | `(2*x*(x+1) - (x^2+1)) / (x+1)^2` |
| `sin(cos(x))` | `-sin(x)*cos(cos(x))` |

### Testing Checklist

- [ ] Input `x^2` menghasilkan `2*x`
- [ ] Input `sin(x)` menghasilkan `cos(x)`
- [ ] Input `x^2 + 3*x` menghasilkan `2*x + 3`
- [ ] Input `x * sin(x)` menghasilkan `sin(x) + x*cos(x)`
- [ ] Input `sin(x) / x` menghasilkan `(cos(x)*x - sin(x)) / x^2`
- [ ] Tombol Sebelumnya/Selanjutnya bekerja dengan baik
- [ ] Error message muncul untuk input tidak valid
- [ ] Tombol "Bersihkan" menghapus semua input dan output

---

## Panduan Teknis

### Struktur File

```
DiffCalc/
├── derivative_calculator.html   ← FILE UTAMA
└── README.md                    ← File ini
```

### Arsitektur Kode

Aplikasi menggunakan **recursive descent parser** dengan representasi **Abstract Syntax Tree (AST)**:

**Class DerivativeCalculator:**
- `tokenize()` — mengubah string input menjadi token
- `parse()` — mengubah token menjadi AST
- `derivative()` — menghitung turunan secara rekursif
- `simplify()` — menyederhanakan hasil
- `astToString()` — mengubah AST kembali ke string

**Contoh AST untuk `2*x + 3`:**
```json
{
  "type": "binary",
  "op": "+",
  "left": {
    "type": "binary",
    "op": "*",
    "left": { "type": "number", "value": 2 },
    "right": { "type": "variable", "name": "x" }
  },
  "right": { "type": "number", "value": 3 }
}
```

**Node types dalam AST:**

| Type | Keterangan |
|---|---|
| `number` | Konstanta numerik |
| `variable` | Variabel (x) |
| `binary` | Operasi biner (+, -, *, /) |
| `power` | Pangkat (^) |
| `function` | Fungsi (sin, cos, exp, log, ...) |
| `unary` | Operasi unary (-) |

### Keterbatasan

- Tidak mendukung `u^v` (basis dan pangkat keduanya variabel)
- Simplifikasi hasil tidak selalu maksimal — nilai matematiknya tetap benar
- Hanya mendukung turunan terhadap variabel `x`
- Fungsi seperti `arcsin`, `arccos`, `sinh`, `cosh` belum didukung

---

## Troubleshooting

| Masalah | Solusi |
|---|---|
| "Unexpected character at position X" | Gunakan `*` untuk perkalian, `^` untuk pangkat |
| "Unbalanced parentheses" | Pastikan setiap `(` ada pasangannya `)` |
| "Unknown function" | Gunakan: `sin`, `cos`, `tan`, `exp`, `log`, `sqrt` |
| Output terlihat aneh | Nilai matematiknya benar, hanya bentuk presentasinya bisa berbeda |
| Browser tidak merespons | Refresh (F5), clear cache, atau coba browser lain |
| Crash di fungsi kompleks | Coba input yang lebih sederhana terlebih dahulu |

### Contoh perbaikan input:

```
❌ SALAH → ✅ BENAR
2x        → 2*x
x2        → x^2
ln(x)     → log(x)
e^x       → exp(x)
sinx      → sin(x)
```

---

## Use Cases

**Untuk Siswa:** belajar kalkulus diferensial, memahami step-by-step solving, verifikasi PR/homework, persiapan ujian.

**Untuk Guru:** demonstrasi di kelas, membuat soal latihan, interactive learning tool.

**Untuk Profesional:** quick reference, verification calculation, research helper.

---

## Roadmap

- [ ] Higher order derivatives (turunan ke-2, ke-3, dst)
- [ ] Integration (antiderivative)
- [ ] Function graphing dengan Chart.js
- [ ] Taylor series expansion
- [ ] Numerical differentiation (evaluasi f'(a) untuk x tertentu)
- [ ] Inverse trigonometric (arcsin, arccos, arctan)
- [ ] Hyperbolic functions (sinh, cosh)
- [ ] Export to PDF/PNG
- [ ] Dark mode toggle
- [ ] Multiple languages support
- [ ] Progressive Web App (PWA)

---

## Referensi

**Teori Matematika:**
- Stewart, James. *Calculus: Early Transcendentals*
- Larson, Ron. *Calculus* (9th Edition)
- MIT OpenCourseWare — Single Variable Calculus
- Khan Academy — Calculus Derivatives Section

**Limit penting yang sering dipakai:**
```
lim(h→0) sin(h)/h  = 1
lim(h→0) (e^h-1)/h = 1
lim(x→∞) (1+1/x)^x = e
```

**Identitas trigonometri:**
```
sin²(x) + cos²(x) = 1
sin(2x) = 2·sin(x)·cos(x)
cos(2x) = cos²(x) - sin²(x)
```

---

## Kesimpulan

Kalkulator Turunan Fungsi (DiffCalc) adalah aplikasi web berbasis HTML, CSS, dan JavaScript yang membantu pengguna menghitung turunan fungsi matematika secara simbolik dengan cepat dan mudah. Selain menampilkan hasil akhir, aplikasi ini juga menyediakan langkah-langkah penyelesaian secara rinci sehingga dapat digunakan sebagai media pembelajaran kalkulus diferensial.

DiffCalc mendukung berbagai jenis fungsi, seperti polinomial, trigonometri, eksponensial, dan logaritma, serta menerapkan aturan turunan penting seperti Power Rule, Product Rule, Quotient Rule, dan Chain Rule. Dengan desain yang ringan, responsif, dan dapat digunakan secara offline, aplikasi ini cocok untuk siswa, mahasiswa, guru, maupun pengguna umum.

Secara keseluruhan, DiffCalc merupakan alat bantu pembelajaran yang praktis, interaktif, dan mudah diakses. Pengembangan fitur lanjutan di masa depan diharapkan dapat meningkatkan fungsi dan manfaat aplikasi ini.

---
