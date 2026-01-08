## 1. Fonksiyon Nedir?

Fonksiyon, belirli bir işi yapan, tekrar kullanılabilir kod bloklarıdır.  
Kod tekrarını azaltır ve programın okunabilirliğini artırır.

```python
def selamla():
    print("Merhaba")
```

---

## 2. Fonksiyon Çağırma

```python
selamla()
```

---

## 3. Parametre ve Argüman

```python
def selamla(isim):
    print("Merhaba", isim)

selamla("Ahmet")
```

- Parametre: Fonksiyon tanımındaki değişken
    
- Argüman: Fonksiyon çağrılırken verilen değer
    

---

## 4. Birden Fazla Parametre

```python
def topla(a, b):
    return a + b
```

---

## 5. return Kullanımı

```python
def kare(x):
    return x * x

sonuc = kare(5)
```

return:

- Fonksiyonu sonlandırır
    
- Değer döndürür
    

return yoksa fonksiyon `None` döner.

---

## 6. Varsayılan (Default) Parametreler

```python
def selamla(isim="Misafir"):
    print("Merhaba", isim)

selamla()
selamla("Ayşe")
```

---

## 7. Anahtar Kelime Argümanları

```python
def bilgiler(ad, yas):
    print(ad, yas)

bilgiler(yas=25, ad="Ali")
```

Sıra önemli değildir.

---

## 8. *args (Değişken Sayıda Argüman)

```python
def toplam(*args):
    return sum(args)

toplam(1, 2, 3, 4)
```

args bir tuple’dır.

---

## 9. **kwargs (Anahtar-Değer Argümanlar)

```python
def yazdir(**kwargs):
    for key, value in kwargs.items():
        print(key, value)

yazdir(ad="Ali", yas=30)
```

kwargs bir dictionary’dir.

---

## 10. Fonksiyon İçinde Fonksiyon

```python
def dis():
    def ic():
        print("İç fonksiyon")
    ic()

dis()
```

---

## 11. Global ve Local Değişkenler

```python
x = 10

def fonk():
    x = 5
    print(x)

fonk()
print(x)
```

global kullanımı:

```python
x = 10

def fonk():
    global x
    x = 5

fonk()
```

---

## 12. Fonksiyonlarda Docstring

```python
def topla(a, b):
    """
    İki sayıyı toplar.
    """
    return a + b
```

```python
help(topla)
```

---

## 13. Lambda Fonksiyonlar

```python
kare = lambda x: x * x
kare(4)
```

Kısa, tek satırlık fonksiyonlar için kullanılır.

---

## 14. Fonksiyonları Parametre Olarak Gönderme

```python
def uygula(f, x):
    return f(x)

uygula(lambda x: x + 1, 5)
```

---

## 15. map, filter, reduce

### map

```python
nums = [1, 2, 3]
list(map(lambda x: x * 2, nums))
```

### filter

```python
list(filter(lambda x: x % 2 == 0, nums))
```

### reduce

```python
from functools import reduce

reduce(lambda a, b: a + b, nums)
```

---

## 16. Recursive (Özyinelemeli) Fonksiyonlar

```python
def faktoriyel(n):
    if n == 1:
        return 1
    return n * faktoriyel(n - 1)
```

---

## 17. Type Hinting (Tür Belirtme)

```python
def topla(a: int, b: int) -> int:
    return a + b
```

---

## 18. Fonksiyonlarda Hata Yönetimi

```python
def bol(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Sıfıra bölünemez"
```

---

## 19. Sık Yapılan Hatalar

```python
def f():
    print("Merhaba")

x = f()
```

x değeri `None` olur çünkü return yoktur.

---

