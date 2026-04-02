<style>
.katex-mathml { display: none; }

body, .markdown-body {
  font-family: "Times New Roman", Times, serif;
  font-size: 0.95em;
  background: #fffff8;
  color: #111;
  max-width: 780px;
  margin: 1.2em auto;
  padding: 0 1.2em;
  line-height: 1.45;
}

h1 {
  font-size: 1.5em;
  text-align: center;
  border-bottom: 3px double #333;
  padding-bottom: 0.25em;
  margin: 0.4em 0 1em;
  letter-spacing: 0.03em;
}

h2 {
  font-size: 1em;
  background: #eee;
  border-left: 4px solid #555;
  padding: 0.18em 0.6em;
  margin: 1.1em 0 0.5em;
}

.def-box {
  border: 1px solid #aaa;
  background: #f9f9f2;
  padding: 0.3em 0.8em;
  margin: 0.5em 0;
  font-size: 0.93em;
}

.side-by-side {
  display: flex;
  gap: 1em;
  align-items: flex-start;
  margin: 0.5em 0;
  flex-wrap: wrap;
}

.side-by-side > div {
  flex: 1;
  min-width: 140px;
  border: 1px solid #ccc;
  background: #fdfdfa;
  padding: 0.3em 0.7em;
  text-align: center;
}

.side-by-side > div strong {
  display: block;
  margin-bottom: 0.2em;
  font-size: 0.85em;
  color: #444;
  border-bottom: 1px solid #ddd;
  padding-bottom: 0.15em;
}

.side-by-side .katex-display { margin: 0.3em 0 !important; }

.inline-def {
  display: flex;
  gap: 1.5em;
  margin: 0.4em 0 0.4em 0.5em;
  font-size: 0.93em;
}
.inline-def span b { margin-right: 0.3em; }

.grid2 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.7em;
  margin: 0.5em 0;
}
.grid2 > div {
  border: 1px solid #ccc;
  background: #fdfdfa;
  padding: 0.35em 0.8em 0.45em;
  text-align: center;
}
.grid2 > div > b {
  display: block;
  font-size: 0.87em;
  color: #444;
  border-bottom: 1px solid #ddd;
  padding-bottom: 0.15em;
  margin-bottom: 0.25em;
}

hr { border: none; border-top: 1px solid #bbb; margin: 0.9em 0; }
</style>

# Matris Kavramına Giriş

## 1. Lineer Sistemlerin Matris Formu

Doğrusal denklem sistemleri, katsayıların ayrıştırılması yoluyla $AX = B$ formunda standardize edilir.

<div class="grid2">

<div>

**Denklem Sistemi**

3x − 2y − 5z = 10

x + 6y + z = 8

</div>

<div>

**Matris Formu** *AX = B*

$\displaystyle\begin{bmatrix}3 & -2 & -5 \\ 1 & 6 & 1\end{bmatrix}\begin{bmatrix}x \\ y \\ z\end{bmatrix}=\begin{bmatrix}10 \\ 8\end{bmatrix}$

</div>

</div>

<div class="def-box">

**Katsayılar Matrisi (*A*):** Bilinmeyen katsayılarını içeren *m*×*n* tablodur.

</div>

---

## 2. Boyut ve Gösterim (Dimensions)

Matrisler büyük harflerle ($A, B, C$) simgelenir. Boyut **Satır $\times$ Sütun** ($m \times n$) olarak tanımlanır.

<div class="inline-def">

**Satır (*m*):** Denklem sayısı. &nbsp;&nbsp; **Sütun (*n*):** Bilinmeyen sayısı.

</div>

<div class="grid2">

<div>

**Kare Matris — 3×3** *(m = n)*

$\displaystyle A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 3 \\ 4 & 5 & 2 \end{bmatrix}$

</div>

<div>

**Dikdörtgen Matris — 2×3**

$\displaystyle B = \begin{bmatrix} 1 & 0 & 2 \\ 1 & 1 & -3 \end{bmatrix}$

</div>

</div>

---

## 3. Eleman Adresleme (Indexing)

Her eleman, bulunduğu satır ($i$) ve sütun ($j$) ile $a_{ij}$ şeklinde adreslenir.

$$A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix}$$

<div class="def-box">

**İndis kuralı:** İlk sayı (*i*) satırı, ikinci sayı (*j*) sütunu gösterir. Örnek: $a_{21}$ → 2. satır, 1. sütun.

</div>
