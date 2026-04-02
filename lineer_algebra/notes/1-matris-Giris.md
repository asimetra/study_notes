# MATRIS NEDIR VE TEMEL MATRIS KAVRAMLARI

Bu doküman, doğrusal denklem sistemlerinin matris formunda nasıl modelleneceğini ve temel matris notasyonlarını tanımlamaktadır.

---

## 1. Denklem Sisteminin Soyutlanması

Çok bilinmeyenli doğrusal denklem sistemleri, değişkenlerinden arındırılarak saf katsayı tablolarına dönüştürülür. 

**Örnek Denklem Sistemi:**
$$3x - 2y - 5z = 10$$
$$x + 6y + z = 8$$

**Matris Formasyonuna Çevrilmesi:**
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
Not: Yukarıdaki eşitlikte sol taraftaki ilk matris "Katsayılar Matrisi" olarak adlandırılır.

---

## 2. Boyut ve Kapasite Tanımlamaları

Bir matrisin mimarisi, sahip olduğu satır (m) ve sütun (n) sayıları ile belirlenir ve genel notasyonda "m x n" formatında ifade edilir.

* **Satır Sayısı (m):** Sistemdeki toplam denklem sayısına eşittir.
* **Sütun Sayısı (n):** Sistemdeki toplam bilinmeyen sayısına eşittir.

---

## 3. İsimlendirme ve Boyut Örnekleri

Matrisler hiyerarşik olarak büyük harflerle (A, B, C) tanımlanırken, ilgili boyutlar alt indis olarak belirtilir.

**Örnek 1 (3x3 Matris):**
$$A = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 3 \\ 4 & 5 & 2 \end{bmatrix}$$
Boyutu: 3x3. Gösterimi: $A_{3 \times 3}$

**Örnek 2 (2x3 Matris):**
$$B = \begin{bmatrix} 1 & 0 & 2 \\ 1 & 1 & -3 \end{bmatrix}$$
Boyutu: 2x3. Gösterimi: $B_{2 \times 3}$

---

## 4. Eleman İndeksleme (Addressing)

Matris içindeki her bir veri noktası, bulunduğu satır ve sütun numarasına göre küçük harflerle ($a_{ij}$) indekslenir. 

**İndeksleme Örneği:**
$$A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix}_{2 \times 3}$$

* $a_{13}$ Tanımı: Matrisin 1. satırında ve 3. sütununda bulunan spesifik elemanı (veriyi) temsil eder.