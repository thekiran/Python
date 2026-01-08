# Python Hazır Fonksiyonlar 

## 1. Hazır Fonksiyon Nedir?

Hazır fonksiyonlar, Python içinde önceden tanımlı olarak gelen ve belirli işlemleri kolayca yapmamızı sağlayan fonksiyonlardır.

Örnek:

- print()
    
- input()
    
- int(), float(), str()
    
- len(), max(), min(), sum()
    

---

## 2. Matematiksel Fonksiyonlar (math modülü)

Matematiksel işlemler için `math` modülü kullanılır.

```python
import math
```

---

## 3. Mutlak Değer Alma

### math.fabs()

- Float değer döndürür
    
- math modülüne aittir
    

```python
import math
math.fabs(-7.5)
```

### abs()

- Python’un yerleşik fonksiyonudur
    
- int, float ve complex için çalışır
    

```python
abs(-10)
```

---

## 4. Sayı Yuvarlama Fonksiyonları

### math.ceil()

Sayıyı yukarı yuvarlar.

```python
import math
math.ceil(2.015)   # 3
math.ceil(-4.7)    # -4
```

### math.floor()

Sayıyı aşağı yuvarlar.

```python
math.floor(2.456)  # 2
math.floor(-4.7)   # -5
```

### round()

En yakın tam sayıya yuvarlar.  
0.5 durumunda en yakın **çift sayıya** yuvarlar.

```python
round(4.5)   # 4
round(3.7)   # 4
```

---

## 5. Üs Alma İşlemi (pow)

### pow()

```python
pow(2, 3)        # 8
pow(2, 3, 5)     # (2^3) % 5 = 3
```

### math.pow()

Sonucu float döndürür.

```python
import math
math.pow(3, 2)
```

---

## 6. Karekök Alma (sqrt)

```python
import math
math.sqrt(25)   # 5.0
```

Negatif sayı girilirse hata verir.

---

## 7. Logaritma Fonksiyonları

```python
import math

math.log(7)        # doğal log (e tabanı)
math.log(8, 2)     # 2 tabanında log
math.log10(1000)   # 10 tabanı
math.log2(8)       # 2 tabanı
```

---

## 8. Trigonometrik Fonksiyonlar

Trigonometrik fonksiyonlar **radyan** ile çalışır.

```python
import math

aci = math.radians(30)
math.sin(aci)
math.cos(aci)
math.tan(aci)
```

---

## 9. max() ve min()

Bir dizideki en büyük ve en küçük değeri bulur.

```python
sayilar = [-10, -5.5, 0, 3, 7.2]
max(sayilar)
min(sayilar)
```

---

## 10. sum() Fonksiyonu

Listedeki tüm sayıların toplamını verir.

```python
sum([1, 2, 3, 4])
```

---

## 11. divmod() Fonksiyonu

Bölüm ve kalanı birlikte döndürür.

```python
divmod(56, 10)   # (5, 6)
```

---

## 12. İkili Tabana Dönüştürme (bin)

```python
bin(5)   # '0b101'
```

---

# String Fonksiyonları

## 13. replace()

```python
s = "Python güçlü bir programlama dilidir"
s.replace("Python", "Java")
```

Belirli sayıda değiştirme:

```python
"element".replace("e", "", 1)
```

---

## 14. upper() ve lower()

```python
"python".upper()
"PYTHON".lower()
```

---

## 15. capitalize() ve title()

```python
"python programlama".capitalize()
"python programlama".title()
```

---

## 16. swapcase()

```python
"aYvA".swapcase()
```

---

## 17. strip(), lstrip(), rstrip()

Boşluk ve özel karakterleri temizler.

```python
s = "  merhaba  "
s.strip()
s.lstrip()
s.rstrip()
```

Belirli karakter için:

```python
"ayva".rstrip("a")
```

---

## 18. startswith() ve endswith()

```python
"ayva".startswith("ay")
"ayva".endswith("va")
```

---

## 19. format() ve f-string

```python
a = 5
b = 3

f"{a} + {b} = {a + b}"
"{} + {} = {}".format(a, b, a + b)
```
