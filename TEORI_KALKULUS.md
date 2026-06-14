# 📚 TEORI KALKULUS DIFERENSIAL - Referensi Lengkap

## Daftar Isi
1. [Konsep Dasar Turunan](#konsep-dasar)
2. [Aturan-Aturan Turunan](#aturan-turunan)
3. [Aplikasi Turunan](#aplikasi-turunan)
4. [Contoh Soal & Pembahasan](#contoh-soal)

---

## Konsep Dasar Turunan

### 1.1 Definisi Turunan

Turunan dari fungsi $f(x)$ pada titik $x$ didefinisikan sebagai:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

Dengan syarat limit tersebut ada (converge).

**Interpretasi Geometris:**
- $f'(x)$ adalah **kemiringan (slope) garis singgung** pada kurva $y = f(x)$ di titik $(x, f(x))$
- Mengukur **laju perubahan** fungsi pada titik tersebut

**Contoh Numerik:**
```
Jika f(x) = x²
Pada x = 2:
f(2) = 4
f(2.01) = 4.0401
Selisih = 0.0401 / 0.01 = 4.01 ≈ 4 (derivative)
```

### 1.2 Notasi Turunan

Berbagai notasi untuk turunan fungsi $y = f(x)$:

| Notasi | Pembaca | Penggunaan |
|--------|---------|-----------|
| $f'(x)$ | f prime | Paling umum |
| $\frac{df}{dx}$ | df dx | Leibniz notation |
| $\frac{dy}{dx}$ | dy dx | Untuk y = f(x) |
| $Df(x)$ | D of f | Operator notation |
| $y'$ | y prime | Singkat untuk y = f(x) |

**Contoh:**
```
Untuk f(x) = x³
f'(x) = 3x² (notasi f prime)
df/dx = 3x² (notasi Leibniz)
```

### 1.3 Differentiability (Terdiferensiasikan)

Fungsi $f$ terdiferensiasikan pada $x = a$ jika $f'(a)$ ada.

**Kondisi untuk differentiable:**
1. $f$ kontinyu pada $x = a$
2. Limit kiri dan kanan limit definition sama

**Contoh tidak differentiable:**
- $f(x) = |x|$ pada $x = 0$ (titik cusp)
- $f(x) = \sqrt[3]{x}$ pada $x = 0$ (vertical tangent)

---

## Aturan-Aturan Turunan

### 2.1 Aturan Pangkat (Power Rule)

**Formula:**
$$\frac{d}{dx}[x^n] = n \cdot x^{n-1}$$

**Bukti:** Dari definisi limit
$$f'(x) = \lim_{h \to 0} \frac{(x+h)^n - x^n}{h}$$

Menggunakan binomial expansion dan limit properties, diperoleh hasil di atas.

**Contoh:**
```
d/dx[x²] = 2x
d/dx[x³] = 3x²
d/dx[x^(-1)] = -x^(-2) = -1/x²
d/dx[x^(1/2)] = (1/2)x^(-1/2) = 1/(2√x)
```

**Generalisasi untuk ax^n:**
$$\frac{d}{dx}[ax^n] = a \cdot n \cdot x^{n-1}$$

### 2.2 Aturan Konstanta (Constant Rule)

**Formula:**
$$\frac{d}{dx}[c] = 0$$

dimana $c$ adalah konstanta apapun.

**Interpretasi:** Fungsi konstan tidak berubah, jadi laju perubahannya = 0.

**Contoh:**
```
d/dx[5] = 0
d/dx[π] = 0
d/dx[-100] = 0
```

### 2.3 Aturan Penjumlahan & Pengurangan (Sum/Difference Rule)

**Formula:**
$$\frac{d}{dx}[f(x) \pm g(x)] = f'(x) \pm g'(x)$$

**Prinsip:** Turunan dari jumlah = jumlah dari turunan.

**Contoh:**
```
d/dx[x² + 3x] = d/dx[x²] + d/dx[3x]
               = 2x + 3

d/dx[sin(x) - cos(x)] = cos(x) - (-sin(x))
                       = cos(x) + sin(x)
```

### 2.4 Aturan Perkalian Konstan (Constant Multiple Rule)

**Formula:**
$$\frac{d}{dx}[c \cdot f(x)] = c \cdot f'(x)$$

**Contoh:**
```
d/dx[5x²] = 5 · d/dx[x²]
          = 5 · 2x
          = 10x

d/dx[3sin(x)] = 3 · cos(x)
```

### 2.5 Aturan Perkalian (Product Rule)

**Formula:**
$$\frac{d}{dx}[u \cdot v] = u' \cdot v + u \cdot v'$$

**Intuisi:** Perubahan hasil kali = perubahan u × v lama + u baru × perubahan v.

**Bukti singkat:**
```
d/dx[u·v] = lim[h→0] [u(x+h)·v(x+h) - u(x)·v(x)] / h

Tambah & kurangi u(x+h)·v(x):
= lim[h→0] [u(x+h)·v(x+h) - u(x+h)·v(x) + u(x+h)·v(x) - u(x)·v(x)] / h
= lim[h→0] [u(x+h)·(v(x+h)-v(x)) + v(x)·(u(x+h)-u(x))] / h
= u(x)·v'(x) + v(x)·u'(x)
```

**Contoh:**
```
d/dx[x · sin(x)]
u = x, u' = 1
v = sin(x), v' = cos(x)
Hasil: 1·sin(x) + x·cos(x) = sin(x) + x·cos(x)

d/dx[(x²+1)(x³-2)]
u = x²+1, u' = 2x
v = x³-2, v' = 3x²
Hasil: 2x(x³-2) + (x²+1)·3x²
     = 2x⁴ - 4x + 3x⁴ + 3x²
     = 5x⁴ + 3x² - 4x
```

### 2.6 Aturan Pembagian (Quotient Rule)

**Formula:**
$$\frac{d}{dx}\left[\frac{u}{v}\right] = \frac{u'v - uv'}{v^2}$$

**Mnemonik:** "Low d-high minus high d-low, over low-low" (dengan "low" = denominator, "high" = numerator).

**Contoh:**
```
d/dx[sin(x)/x]
u = sin(x), u' = cos(x)
v = x, v' = 1
Hasil: (cos(x)·x - sin(x)·1) / x²
     = (x·cos(x) - sin(x)) / x²

d/dx[(x²+1)/(x²-1)]
u = x²+1, u' = 2x
v = x²-1, v' = 2x
Hasil: (2x(x²-1) - (x²+1)·2x) / (x²-1)²
     = (2x³ - 2x - 2x³ - 2x) / (x²-1)²
     = -4x / (x²-1)²
```

### 2.7 Aturan Rantai (Chain Rule)

**Formula:**
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

atau dengan notasi Leibniz:
$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

**Prinsip:** Turunan dari komposisi fungsi = perkalian turunan "outer" dan turunan "inner".

**Contoh 1 - Sederhana:**
```
d/dx[sin(x²)]
f(u) = sin(u), f'(u) = cos(u)
g(x) = x², g'(x) = 2x
Hasil: cos(x²) · 2x = 2x·cos(x²)
```

**Contoh 2 - Berlapis:**
```
d/dx[sin(x³ + 2x)]
Outer: sin(...), derivative = cos(...)
Middle: x³ + 2x, derivative = 3x² + 2
Hasil: cos(x³ + 2x) · (3x² + 2)
```

**Contoh 3 - Triple nested:**
```
d/dx[sin²(x)]  = d/dx[(sin(x))²]
f(u) = u², f'(u) = 2u
g(x) = sin(x), g'(x) = cos(x)
Hasil: 2·sin(x) · cos(x) = 2sin(x)cos(x) = sin(2x)
```

---

## Turunan Fungsi Khusus

### 3.1 Trigonometric Functions

| Fungsi | Turunan | Contoh |
|--------|---------|--------|
| sin(x) | cos(x) | d/dx[sin(2x)] = 2cos(2x) |
| cos(x) | -sin(x) | d/dx[cos(x²)] = -2x·sin(x²) |
| tan(x) | sec²(x) = 1/cos²(x) | d/dx[tan(3x)] = 3sec²(3x) |

**Bukti untuk sin(x):**
```
d/dx[sin(x)] = lim[h→0] [sin(x+h) - sin(x)] / h

Gunakan formula: sin(A) - sin(B) = 2cos((A+B)/2)sin((A-B)/2)

= lim[h→0] [2cos(x + h/2)sin(h/2)] / h
= lim[h→0] cos(x + h/2) · [sin(h/2)/(h/2)]
= cos(x) · 1    [karena lim[u→0] sin(u)/u = 1]
```

### 3.2 Exponential & Logarithmic

| Fungsi | Turunan |
|--------|---------|
| e^x | e^x |
| a^x (a > 0) | a^x · ln(a) |
| ln(x) | 1/x |
| log_a(x) | 1/(x·ln(a)) |

**Sifat istimewa e^x:**
Fungsi $e^x$ adalah satu-satunya fungsi yang turunannya sama dengan dirinya sendiri!

**Contoh:**
```
d/dx[e^(2x)] = 2·e^(2x)  (chain rule)
d/dx[3^x] = 3^x · ln(3)
d/dx[ln(x²)] = (1/x²) · 2x = 2/x  (chain rule)
```

### 3.3 Inverse Trigonometric

| Fungsi | Turunan |
|--------|---------|
| arcsin(x) | 1/√(1-x²) |
| arccos(x) | -1/√(1-x²) |
| arctan(x) | 1/(1+x²) |

*(Catatan: Aplikasi belum support ini, tapi ditamahkan untuk referensi)*

---

## Aplikasi Turunan

### 4.1 Analisis Fungsi

**Kriteria Pertama untuk Extrema:**
- Jika $f'(c) = 0$ atau undefined, maka $c$ adalah **critical point**
- Jika $f'$ berubah dari positif ke negatif di $c$: $c$ adalah **local maximum**
- Jika $f'$ berubah dari negatif ke positif di $c$: $c$ adalah **local minimum**

**Contoh:**
```
f(x) = x² - 4x + 3
f'(x) = 2x - 4

Critical point: 2x - 4 = 0 → x = 2
f(2) = 4 - 8 + 3 = -1

Jadi (2, -1) adalah local minimum
```

### 4.2 Optimization (Optimisasi)

Mencari nilai maksimum/minimum fungsi.

**Prosedur:**
1. Hitung f'(x)
2. Selesaikan f'(x) = 0 (critical points)
3. Evaluasi f pada critical points dan endpoints
4. Pilih nilai terbesar/terkecil

**Contoh - Volume Box:**
```
Dari karton 20×30 cm, buatlah box dengan memotong sudut persegi.
Jika panjang potongan = x, volume V(x) = x(20-2x)(30-2x)

V(x) = 600x - 100x² + 4x³
V'(x) = 600 - 200x + 12x²

Set V'(x) = 0:
12x² - 200x + 600 = 0
3x² - 50x + 150 = 0
x = 3.82 atau x = 13.18

Valid: x = 3.82 cm (karena 2x < 20)
Maximum volume ≈ 1054 cm³
```

### 4.3 Related Rates

Menghubungkan laju perubahan dari beberapa variabel.

**Prosedur:**
1. Gambar situasi
2. Identifikasi variabel yang berubah
3. Buat persamaan hubungan antar variabel
4. Diferensiasi terhadap waktu (chain rule)
5. Substitusi nilai yang diketahui

**Contoh - Ladder Problem:**
```
Ladder 10m menyandar tembok. Bottom slide away at 2 m/s.
Seberapa cepat top slide down ketika bottom 6m dari wall?

x = jarak bottom dari wall
y = jarak top dari ground
x² + y² = 100 (Pythagorean)

Diferensiasi terhadap t:
2x(dx/dt) + 2y(dy/dt) = 0
dy/dt = -x/y · dx/dt

Ketika x = 6: y = √(100-36) = 8
dy/dt = -(6/8) · 2 = -1.5 m/s

Top bergerak turun 1.5 m/s
```

### 4.4 Linear Approximation

Menggunakan tangent line untuk approximate fungsi di dekat titik.

**Formula:**
$$f(x) ≈ f(a) + f'(a)(x-a)$$

untuk $x$ dekat dengan $a$.

**Contoh:**
```
Approximate √4.1 menggunakan f(x) = √x, a = 4
f(4) = 2
f'(x) = 1/(2√x)
f'(4) = 1/4

√4.1 ≈ 2 + (1/4)(4.1 - 4)
     = 2 + 0.025
     = 2.025

Actual value: 2.0248... (sangat dekat!)
```

---

## Contoh Soal & Pembahasan

### Soal 1: Power Rule
**Cari turunan dari $f(x) = 5x^3 - 2x^2 + 7x - 3$**

**Pembahasan:**
```
f'(x) = d/dx[5x³] - d/dx[2x²] + d/dx[7x] - d/dx[3]
      = 5·3x² - 2·2x + 7 - 0
      = 15x² - 4x + 7
```

### Soal 2: Product Rule
**Cari turunan dari $f(x) = (x^2 + 1)(x^3 - 2)$**

**Pembahasan (Cara 1 - Product Rule):**
```
u = x² + 1, u' = 2x
v = x³ - 2, v' = 3x²

f'(x) = u'v + uv'
      = 2x(x³ - 2) + (x² + 1)·3x²
      = 2x⁴ - 4x + 3x⁴ + 3x²
      = 5x⁴ + 3x² - 4x
```

**Pembahasan (Cara 2 - Expand terlebih dahulu):**
```
f(x) = x⁵ - 2x² + x³ - 2
f'(x) = 5x⁴ - 4x + 3x² = 5x⁴ + 3x² - 4x
```

### Soal 3: Chain Rule
**Cari turunan dari $f(x) = \sin(3x^2 + 1)$**

**Pembahasan:**
```
Outer: sin(u), derivative = cos(u)
Inner: 3x² + 1, derivative = 6x

f'(x) = cos(3x² + 1) · 6x
      = 6x·cos(3x² + 1)
```

### Soal 4: Quotient Rule
**Cari turunan dari $f(x) = \frac{x^2 + 1}{x - 1}$**

**Pembahasan:**
```
u = x² + 1, u' = 2x
v = x - 1, v' = 1

f'(x) = (u'v - uv') / v²
      = (2x(x-1) - (x²+1)·1) / (x-1)²
      = (2x² - 2x - x² - 1) / (x-1)²
      = (x² - 2x - 1) / (x-1)²
```

### Soal 5: Kombinasi Rules
**Cari turunan dari $f(x) = e^x \sin(x)$**

**Pembahasan:**
```
Product Rule: u·v
u = e^x, u' = e^x
v = sin(x), v' = cos(x)

f'(x) = e^x·sin(x) + e^x·cos(x)
      = e^x(sin(x) + cos(x))
```

### Soal 6: Optimization
**Seekor sapi diikat di pojok gudang berbentuk persegi. 
Gudang 12m × 8m. Rope panjang 10m. 
Berapa area maksimal yang bisa dijangkau sapi?**

**Pembahasan:**
```
Sapi bisa menjangkau:
1. Sektor 3/4 lingkaran (radius 10) di area terbuka
   Area = (3/4)π(10²) = 75π m²

2. Sektor tambahan (radius 10-12) ketika rope membungkus sudut
   Area = (1/4)π(10-12)² + ... (calculation lebih complex)

Total Area ≈ 75π m² ≈ 235.6 m²
```

---

## Tips & Tricks

### Tip 1: Chain Rule adalah King
Banyak masalah rumit bisa dipecah dengan chain rule. Selalu identifikasi "outer" dan "inner" function.

### Tip 2: Product Rule vs Expand
Kadang lebih mudah expand dulu sebelum turunkan.

```
f(x) = (x+1)²
Cara 1: Product rule - rumit
Cara 2: Expand jadi x² + 2x + 1, lalu turunkan 2x + 2 - lebih mudah!
```

### Tip 3: Logarithmic Differentiation
Untuk y = x^x atau y = u^v (complex exponential), gunakan:
```
ln(y) = x·ln(x)
Diferensiasi kedua sisi:
y'/y = ln(x) + 1
y' = y(ln(x) + 1) = x^x(ln(x) + 1)
```

### Tip 4: Simplify Sebelum Turunkan
Sederhanakan dulu expression sebelum diferensiasi, akan lebih mudah.

```
f(x) = (2x² + 4x) / (2x)
     = x + 2  [setelah simplify]
f'(x) = 1  [jauh lebih mudah!)
```

---

## Referensi Penting

**Limit yang Sering Dipakai:**
- $\lim_{h→0} \frac{\sin(h)}{h} = 1$
- $\lim_{h→0} \frac{e^h - 1}{h} = 1$
- $\lim_{x→∞} (1 + 1/x)^x = e$

**Identitas Trigonometri:**
- $\sin²(x) + \cos²(x) = 1$
- $\sin(2x) = 2\sin(x)\cos(x)$
- $\cos(2x) = \cos²(x) - \sin²(x)$

---

**Conclusion**: Mastering derivatives bukan hanya tentang menghafal rules, tapi memahami konsepnya & banyak practice! 🎓

---

*Last Updated: Juni 2025*
