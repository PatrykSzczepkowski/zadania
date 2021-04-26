zad1 

import numpy as jd
print(jd.arange(3,48,3))

zad2
import numpy as jd
before = jd.array([2.2,2.1])
after = jd.array(before, dtype="int64")
print(after)

zad3
import numpy as jd
def a(n):
    if type(n) != int:
        return -1
    return jd.arange(n*n).reshape((n,n))
print(a(3))

zad4
import numpy as jd
def p(a,b):
    return jd.logspace(1,b,b,base=a)
print(p(2,3))
