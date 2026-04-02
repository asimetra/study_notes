# LINEER CEBIR: MODELLEME VE NOTASYON

## 1. LINEER SISTEMLERIN MATRIS FORMU

[cite_start]Doğrusal denklem sistemleri, katsayıların ayrıştırılması yoluyla $AX = B$ formunda standardize edilir[cite: 678, 679].

**Sistem:**
$$3x - 2y - 5z = 10$$
$$x + 6y + z = 8$$

**Matris Notasyonu:**
$$
\begin{bmatrix} 
3 & -2 & -5 \\ 
1 & 6 & 1 
\end{bmatrix}
\begin{bmatrix} 
x \\ 
y \\ 
z 
\end{bmatrix}
=
\begin{bmatrix} 
10 \\ 
8 
\end{bmatrix}
$$

> [cite_start]**Katsayılar Matrisi ($A$):** Bilinmeyen katsayılarını içeren $m \times n$ tablodur[cite: 686, 687].

---

## 2. BOYUT VE GÖSTERIM (DIMENSIONS)

[cite_start]Matrisler büyük harflerle ($A, B, C$) simgelenir[cite: 163, 208]. [cite_start]Boyut, "Satır $\times$ Sütun" ($m \times n$) olarak tanımlanır[cite: 164].

* [cite_start]**Satır ($m$):** Denklem sayısı[cite: 159, 164].
* [cite_start]**Sütun ($n$):** Bilinmeyen sayısı[cite: 159, 164].

**Örnekler:**
* [cite_start]$A_{3 \times 3} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 3 \\ 4 & 5 & 2 \end{bmatrix}$ (Kare Matris: $m = n$)[cite: 165, 168].
* [cite_start]$B_{2 \times 3} = \begin{bmatrix} 1 & 0 & 2 \\ 1 & 1 & -3 \end{bmatrix}$[cite: 184].

---

## 3. ELEMAN ADRESLEME (INDEXING)

[cite_start]Her eleman, bulunduğu satır ($i$) ve sütun ($j$) numarası ile $a_{ij}$ şeklinde adreslenir[cite: 161, 162].

$$A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix}$$

* [cite_start]**İndis Kuralları:** İlk sayı ($i$) satırı, ikinci sayı ($j$) sütunu belirtir[cite: 161, 162].
* [cite_start]**Örnek:** $a_{21}$, ikinci satırın birinci sütundaki elemanıdır[cite: 162].