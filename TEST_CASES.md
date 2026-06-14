# Test Cases & Contoh Penggunaan Aplikasi Kalkulator Turunan

## 📌 Cara Menggunakan File Ini
Copy contoh input dari bawah, paste ke input box aplikasi, lalu klik "Hitung Turunan".

---

## ✅ TEST CASES - POLYNOMIAL (Tingkat Kesulitan: Mudah)

### Test 1.1: Konstanta
```
Input:  5
Output: 0
Aturan: Turunan dari konstanta adalah 0
```

### Test 1.2: Linear
```
Input:  x
Output: 1
Aturan: Turunan dari x adalah 1
```

### Test 1.3: Quadratic
```
Input:  x^2
Output: 2*x
Aturan: Power rule - d/dx[x^n] = n*x^(n-1)
```

### Test 1.4: Cubic
```
Input:  x^3
Output: 3*x^2
Aturan: Power rule
```

### Test 1.5: Multiple Terms
```
Input:  x^2 + 3*x + 2
Output: 2*x + 3
Aturan: Sum rule + Power rule
```

### Test 1.6: Dengan Koefisien
```
Input:  5*x^4
Output: 20*x^3
Aturan: Power rule (5 * 4 = 20)
```

### Test 1.7: Polynomial Kompleks
```
Input:  4*x^3 - 2*x^2 + x - 7
Output: 12*x^2 - 4*x + 1
Aturan: Sum/difference rule + power rule
Perhitungan:
- d/dx[4*x^3] = 12*x^2
- d/dx[-2*x^2] = -4*x
- d/dx[x] = 1
- d/dx[-7] = 0
```

---

## ✅ TEST CASES - TRIGONOMETRY (Tingkat Kesulitan: Sedang)

### Test 2.1: Sine
```
Input:  sin(x)
Output: cos(x)
Aturan: d/dx[sin(x)] = cos(x)
```

### Test 2.2: Cosine
```
Input:  cos(x)
Output: -sin(x)
Aturan: d/dx[cos(x)] = -sin(x)
```

### Test 2.3: Tangent
```
Input:  tan(x)
Output: 1/cos(x)^2
Aturan: d/dx[tan(x)] = sec²(x) = 1/cos²(x)
```

### Test 2.4: Sine dengan Chain Rule
```
Input:  sin(x^2)
Output: 2*x*cos(x^2)
Aturan: Chain rule - d/dx[sin(u)] = cos(u)*du/dx
Perhitungan:
- u = x^2, du/dx = 2*x
- d/dx[sin(x^2)] = cos(x^2) * 2*x
```

### Test 2.5: Cosine dengan Chain Rule
```
Input:  cos(2*x)
Output: -2*sin(2*x)
Aturan: Chain rule
Perhitungan:
- u = 2*x, du/dx = 2
- d/dx[cos(2*x)] = -sin(2*x) * 2
```

### Test 2.6: Trigonometric dengan Polynomial
```
Input:  x^2 + sin(x)
Output: 2*x + cos(x)
Aturan: Sum rule + power rule + trigonometric rule
```

---

## ✅ TEST CASES - PRODUCT & QUOTIENT RULE (Tingkat Kesulitan: Sedang-Sulit)

### Test 3.1: Product - Simple
```
Input:  x * sin(x)
Output: sin(x) + x*cos(x)
Aturan: Product rule - d/dx[u*v] = u'*v + u*v'
Perhitungan:
- u = x, u' = 1
- v = sin(x), v' = cos(x)
- Hasil: 1*sin(x) + x*cos(x)
```

### Test 3.2: Product - Polynomial × Trigonometric
```
Input:  x^2 * sin(x)
Output: 2*x*sin(x) + x^2*cos(x)
Aturan: Product rule
Perhitungan:
- u = x^2, u' = 2*x
- v = sin(x), v' = cos(x)
- Hasil: 2*x*sin(x) + x^2*cos(x)
```

### Test 3.3: Quotient - Simple
```
Input:  sin(x) / x
Output: (cos(x)*x - sin(x)) / x^2
Aturan: Quotient rule - d/dx[u/v] = (u'*v - u*v') / v²
Perhitungan:
- u = sin(x), u' = cos(x)
- v = x, v' = 1
- Hasil: (cos(x)*x - sin(x)*1) / x^2
```

### Test 3.4: Quotient - Polynomial
```
Input:  x^2 / (x + 1)
Output: (2*x*(x+1) - x^2) / (x+1)^2
Aturan: Quotient rule
```

---

## ✅ TEST CASES - EXPONENTIAL (Tingkat Kesulitan: Sedang)

### Test 4.1: e^x
```
Input:  exp(x)
Output: exp(x)
Aturan: d/dx[e^x] = e^x (istimewa!)
```

### Test 4.2: e^(2x)
```
Input:  exp(2*x)
Output: 2*exp(2*x)
Aturan: Chain rule - d/dx[e^u] = e^u * du/dx
Perhitungan:
- u = 2*x, du/dx = 2
- Hasil: exp(2*x) * 2
```

### Test 4.3: e^(x²)
```
Input:  exp(x^2)
Output: 2*x*exp(x^2)
Aturan: Chain rule
Perhitungan:
- u = x^2, du/dx = 2*x
- Hasil: exp(x^2) * 2*x
```

### Test 4.4: Polynomial × Exponential
```
Input:  x^2 * exp(x)
Output: 2*x*exp(x) + x^2*exp(x)
Aturan: Product rule + exponential rule
```

---

## ✅ TEST CASES - LOGARITHM (Tingkat Kesulitan: Sedang)

### Test 5.1: Natural Logarithm
```
Input:  log(x)
Output: 1/x
Aturan: d/dx[ln(x)] = 1/x
```

### Test 5.2: ln(x²)
```
Input:  log(x^2)
Output: 2/x
Aturan: Chain rule - d/dx[ln(u)] = (1/u)*du/dx
Perhitungan:
- u = x^2, du/dx = 2*x
- Hasil: (1/x^2) * 2*x = 2/x
```

### Test 5.3: ln(sin(x))
```
Input:  log(sin(x))
Output: cos(x)/sin(x)
Aturan: Chain rule (double)
Perhitungan:
- u = sin(x), du/dx = cos(x)
- d/dx[ln(sin(x))] = (1/sin(x)) * cos(x)
```

---

## ✅ TEST CASES - COMBINED (Tingkat Kesulitan: Sulit)

### Test 6.1: All Operators
```
Input:  x^2 + 3*x - 2
Output: 2*x + 3
```

### Test 6.2: Exponential × Trigonometric
```
Input:  exp(x) * cos(x)
Output: exp(x)*cos(x) - exp(x)*sin(x)
Aturan: Product rule
Perhitungan:
- u = exp(x), u' = exp(x)
- v = cos(x), v' = -sin(x)
- Hasil: exp(x)*cos(x) + exp(x)*(-sin(x))
        = exp(x)*cos(x) - exp(x)*sin(x)
```

### Test 6.3: Logarithm × Polynomial
```
Input:  x^2 * log(x)
Output: 2*x*log(x) + x
Aturan: Product rule + logarithm rule
Perhitungan:
- u = x^2, u' = 2*x
- v = log(x), v' = 1/x
- Hasil: 2*x*log(x) + x^2*(1/x)
        = 2*x*log(x) + x
```

### Test 6.4: Complex Fraction
```
Input:  (x^2 + 1) / (x + 1)
Output: (2*x*(x+1) - (x^2+1)) / (x+1)^2
Aturan: Quotient rule
```

### Test 6.5: Nested Functions
```
Input:  sin(cos(x))
Output: -sin(x)*cos(cos(x))
Aturan: Chain rule (double composition)
Perhitungan:
- d/dx[sin(cos(x))] = cos(cos(x)) * d/dx[cos(x)]
                     = cos(cos(x)) * (-sin(x))
```

---

## 🎯 TEST CASES RECOMMENDED UNTUK PEMBELAJARAN

### Level 1: Dasar (Start Here)
1. `x^2`
2. `x^3`
3. `x^2 + 2*x`
4. `3*x^2 + 4*x + 1`

### Level 2: Trigonometry & Exponential
5. `sin(x)`
6. `cos(x)`
7. `exp(x)`
8. `log(x)`

### Level 3: Chain Rule
9. `sin(x^2)`
10. `exp(2*x)`
11. `log(x^2)`

### Level 4: Product & Quotient
12. `x * sin(x)`
13. `x^2 * exp(x)`
14. `sin(x) / x`

### Level 5: Challenge
15. `exp(x) * cos(x)`
16. `x^2 * log(x)`
17. `sin(cos(x))`

---

## 📊 PERBANDINGAN HASIL (Manual Calculation)

### Contoh Manual: f(x) = x³ + 2x² - 5x + 3

**Perhitungan Langkah Demi Langkah:**

1. **Identifikasi setiap term:**
   - Term 1: x³
   - Term 2: 2x²
   - Term 3: -5x
   - Term 4: 3

2. **Terapkan power rule untuk setiap term:**
   - d/dx[x³] = 3x²
   - d/dx[2x²] = 2·2x = 4x
   - d/dx[-5x] = -5
   - d/dx[3] = 0

3. **Gabungkan hasil:**
   - f'(x) = 3x² + 4x - 5 + 0
   - f'(x) = 3x² + 4x - 5

**Verifikasi:**
- Koefisien: 3 × 3 = 9? No, 1 × 3 = 3 ✓
- Pangkat berkurang: 3 menjadi 2 ✓
- Konstanta hilang ✓

---

## 🔍 DEBUGGING GUIDE

### Jika Input Tidak Dikenali:

```
❌ SALAH:
- 2x      (tidak ada *)
- x2      (pangkat harus x^2)
- 2^x^2   (ambiguitas)

✅ BENAR:
- 2*x
- x^2
- 2^(x^2) atau x^(2^2)
```

### Error Messages:

| Error | Solusi |
|-------|--------|
| "Unexpected character" | Cek karakter tidak valid (gunakan hanya `^*/+-()`) |
| "Unbalanced parentheses" | Pastikan setiap `(` ada pasangannya `)` |
| "Unknown function" | Gunakan: sin, cos, tan, exp, log, sqrt saja |

---

## 📝 CATATAN PENTING

### Untuk Hasil Optimal:
1. ✅ **Gunakan `*` untuk perkalian** → `2*x` bukan `2x`
2. ✅ **Gunakan `^` untuk pangkat** → `x^2` bukan `x2` atau `x²`
3. ✅ **Gunakan `log` untuk ln** → `log(x)` bukan `ln(x)`
4. ✅ **Gunakan `exp` untuk e^x** → `exp(x)` bukan `e^x`
5. ✅ **Parentheses untuk clarity** → `sin(x^2)` bukan `sin x^2`

### Interpretasi Hasil:
- **Positif turunan** = Fungsi naik di titik tersebut
- **Negatif turunan** = Fungsi turun di titik tersebut
- **Nol turunan** = Titik kritis (kemungkinan max/min)

---

## 🧪 TESTING CHECKLIST

Gunakan checklist ini untuk memverifikasi bahwa calculator bekerja dengan baik:

- [ ] Input `x^2` menghasilkan `2*x`
- [ ] Input `sin(x)` menghasilkan `cos(x)`
- [ ] Input `x^2 + 3*x` menghasilkan `2*x + 3`
- [ ] Input `x * sin(x)` menghasilkan `sin(x) + x*cos(x)`
- [ ] Input `sin(x) / x` menghasilkan `(cos(x)*x - sin(x)) / x^2`
- [ ] Tombol "Sebelumnya/Selanjutnya" bekerja dengan baik
- [ ] Error message muncul untuk input tidak valid
- [ ] "Bersihkan" button menghapus semua input dan output

---

## 💡 TIPS & TRIK

1. **Gunakan contoh buttons**: Klik salah satu contoh untuk langsung mencoba
2. **Baca step-by-step**: Jangan skip, pahami setiap aturan yang diterapkan
3. **Compare dengan teori**: Cocokkan hasil dengan buku kalkulus Anda
4. **Experiment**: Coba kombinasi berbeda untuk memahami pattern

---

**Last Updated**: 2025
**Status**: Complete & Tested
