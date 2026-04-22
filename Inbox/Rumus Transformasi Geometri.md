
|**No.**|**Tipe Transformasi**|**Hasil (Bayangan)**|**Matriks Transformasi**|
|---|---|---|---|
|1.|Translasi $\binom{a}{b}$|$P(x, y) \rightarrow P(x + a, y + b)$|$\binom{a}{b}$|
|2.|Pencerminan terhadap sumbu X|$P(x, y) \rightarrow P(x, -y)$|$\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$|
|3.|Pencerminan terhadap sumbu Y|$P(x, y) \rightarrow P(-x, y)$|$\begin{pmatrix} -1 & 0 \\ 0 & 1 \end{pmatrix}$|
|4.|Pencerminan terhadap titik asal $(0, 0)$|$P(x, y) \rightarrow P(-x, -y)$|$\begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$|
|5.|Pencerminan terhadap garis $y = x$|$P(x, y) \rightarrow P(y, x)$|$\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$|
|6.|Pencerminan terhadap garis $y = -x$|$P(x, y) \rightarrow P(-y, -x)$|$\begin{pmatrix} 0 & -1 \\ -1 & 0 \end{pmatrix}$|
|7.|Pencerminan terhadap garis $x = h$|$P(x, y) \rightarrow P(2h - x, y)$|-|
|8.|Pencerminan terhadap garis $y = k$|$P(x, y) \rightarrow P(x, 2k - y)$|-|
|9.|Pencerminan terhadap titik $(a, b)$|$P(x, y) \rightarrow P(2a - x, 2b - y)$|-|
|10.|Rotasi terhadap titik pusat $O(0, 0)$ sejauh $\theta$|$P(x, y) \rightarrow P(x \cos \theta - y \sin \theta, x \sin \theta + y \cos \theta)$|$\begin{pmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{pmatrix}$|
|11.|Rotasi terhadap titik pusat $A(a, b)$ sejauh $\theta$|$P(x, y) \rightarrow P((x - a) \cos \theta - (y - b) \sin \theta + a, (x - a) \sin \theta + (y - b) \cos \theta + b)$|$\begin{pmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{pmatrix} \binom{x - a}{y - b} + \binom{a}{b}$|
|12.|Dilatasi terhadap titik pusat $O(0, 0)$|$P(x, y) \rightarrow P(kx, ky)$|$\begin{pmatrix} k & 0 \\ 0 & k \end{pmatrix}$|
|13.|Dilatasi terhadap titik pusat $A(a, b)$|$P(x, y) \rightarrow P(k(x - a), k(y - b))$|$\begin{pmatrix} k & 0 \\ 0 & k \end{pmatrix} \binom{x - a}{y - b} + \binom{a}{b}$|