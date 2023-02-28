# Tugas-3-Sistem-Kendali-
# Nama : Rr. Herlina Kusumaningrum
# NIM : 21/480564/PA/20879

!pip install tbcontrol

import sympy
import tbcontrol
from tbcontrol.symbolic import routh

s = sympy.Symbol('s')
K = sympy.Symbol('K')

print("1. Polynomial Value")
p = 4*s**4 + 3*s**3 + 2*s**2 +  s + 7
p = sympy.Poly(p, s)
p

print("2. Routh Table")
a = routh(sympy.Poly(p, s))
a
