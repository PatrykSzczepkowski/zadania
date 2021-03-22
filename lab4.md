zad1
import sys
lista=[x for x in range(100) if x%4==0]
print(lista)
plik=open("note.txt","w+")
plik.writelines(str(lista))

zad2
import sys
plik=open("note.txt","r")
print(plik.read())

zad3
x = input("Podaj tekst")
with open("note.txt", "w") as plik:
    plik.write(x)

zad4

class NaZakupy:
     """Klasa NaZakupy"""
     def __init__(self, nazwa, ilosc, jednostka_miary, cena):
         self.nazwa = nazwa
         self.ilosc = float(ilosc)
         self.jednostka_miary = jednostka_miary
         self.cena = float(cena)
     def wyswietl_produkt(self):
         return self.nazwa
     def ile_produktu(self):
         return str(self.ilosc)+str(self.jednostka_miary)
     def ile_kosztuje(self):
         return self.ilosc*self.cena

x = NaZakupy("kasztany","2","kg",20)
print(x.wyswietl_produkt())
print(x.ile_produktu())
print(x.ile_kosztuje())

zad5
class Ciagi:
    def __init__(self, a1, r, n):
        self.a1 = float(a1)
        self.a2 = float(a1 + r)
        self.a3 = float(a1 + 2 * r)
        self.r = float(r)
        self.n = float(n)

    def wyswietl_dane(self):
        print(self.a1)
        print(self.a2)
        print(self.a3)
        print(self.r)
        print(self.n)

    def pobierz_elementy(self):
        self.a1 = float(input("Podaj a1:"))
        self.a2 = float(input("Podaj a2:"))
        self.a3 = float(input("Podaj a3:"))

    def pobierz_parametry(self):
        self.a1 = float(input("Podaj a1:"))
        self.r = float(input("Podaj r:"))
        self.n = float(input("Podaj n:"))

    def policz_sume(self):
        suma = ((2 * self.a1 + (self.n - 1) * self.r) / 2) * self.n
        print(suma)

    def policz_elementy(self):
        print(self.a1 + (self.n - 1) * self.r)

ciag = Ciagi()
ciag.wyswietl_dane()
ciag.pobierz_elementy()
ciag.pobierz_parametry()
ciag.policz_sume()
ciag.policz_elementy()
