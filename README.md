# Tugas-3-Sistem-Kendali-
# Nama : Rr. Herlina Kusumaningrum
# NIM : 21/480564/PA/20879

- !pip install tbcontrol : berfungsi untuk menginstal package bernama tbcontrol, package tersebut berguna untuk mengolah data terkait dinamika dan kontrol/kendali
- import sympy 
- import tbcontrol
- from tbcontrol.symbolic import routh : berfungsi untuk memanggil library yang dibutuhkan. Sympy untuk library matematika simbolik, tbcontrol digunakan untuk kendali, sedangkan routh digunakan untuk metode pengolahan sistem
- s = sympy.Symbol('s')  : mendeklarasi simbol dalam persamaan matematika agar dapat dideteksi oleh sistem
- K = sympy.Symbol('K') : mendeklarasi simbol dalam persamaan matematika agar dapat dideteksi oleh sistem
- print("1. Polynomial Value") : menampilkan hasil nilai polinomial
- p = 4*s**4 + 3*s**3 + 2*s**2 +  s + 7 : mendeklarasi persamaan polinomial yang disimpan dalam variabel 'p'
- p = sympy.Poly(p, s) : berfungsi untuk merubah persamaan P menjadi persamaan polinomial dengan representasi simbolik yang benar
- p : berfungsi untuk menampilkan persamaan 
- print("2. Routh Table") : menampilkan hasil Routh Table 
- a = routh(sympy.Poly(p, s)) : berfungsi untuk membuat Routh Table dari persamaan polinomial yang diberikan, dan disimpan dalam variabel R
- a : berfungsi untuk menampilkan persamaan 
- print("3. K value which can be changed via user input") : berfungsi untuk menampilkan nilai K yang dapat diubah melalui input pengguna
- sympy.solve([e > 0 for e in a[:, 0]], K) : berfungsi untuk menampilkan nilai K yang sesuai agar persamaan stabil
