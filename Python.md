Tamam **TkMatE**. Aşağıda **emoji kullanmadan**, sade ve ders/sınav odaklı şekilde **temel Python araçlarını** veriyorum.

---

# Temel Python Araçları (for, if, while vb.)

## 1. print() – Ekrana Yazdırma

```python
print("Merhaba Python")
print(5 + 3)
```

---

## 2. Değişkenler (Variables)

```python
x = 10
name = "Ahmet"
pi = 3.14
```

Python dinamik tipli bir dildir, değişken türü önceden belirtilmez.

---

## 3. Temel Veri Tipleri

```python
int     # Tam sayı
float   # Ondalıklı sayı
str     # Metin
bool    # True / False
```

```python
type(10)   # <class 'int'>
```

---

## 4. if / elif / else – Koşul Yapısı

```python
age = 18

if age >= 18:
    print("Resit")
elif age == 17:
    print("Sinirda")
else:
    print("Resit degil")
```

Python’da süslü parantez yoktur. Kod blokları girinti (indentation) ile belirlenir.

---

## 5. for Döngüsü

### Liste Üzerinde for

```python
numbers = [1, 2, 3, 4]

for n in numbers:
    print(n)
```

### range() ile for

```python
for i in range(5):
    print(i)
```

```python
for i in range(1, 10, 2):
    print(i)
```

---

## 6. while Döngüsü

```python
i = 0

while i < 5:
    print(i)
    i += 1
```

Koşul doğru olduğu sürece çalışır. Yanlış koşul yazılırsa sonsuz döngü oluşabilir.

---

## 7. break ve continue

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

break döngüyü tamamen bitirir.  
continue o adımı atlayıp devam eder.

---

## 8. Listeler (List)

```python
nums = [10, 20, 30]

nums.append(40)
nums.remove(20)

print(nums)
```

```python
nums[0]     # İlk eleman
nums[-1]    # Son eleman
```

---

## 9. Tuple (Değiştirilemez Liste)

```python
colors = ("red", "green", "blue")
```

Tuple elemanları sonradan değiştirilemez.

---

## 10. Dictionary (Sözlük)

```python
user = {
    "name": "Ahmet",
    "age": 22
}

print(user["name"])
```

```python
for key, value in user.items():
    print(key, value)
```

---

## 11. Fonksiyonlar (def)

```python
def greet(name):
    return "Merhaba " + name

print(greet("TkMatE"))
```

---

## 12. input() – Kullanıcıdan Veri Alma

```python
name = input("Adinizi girin: ")
print(name)
```

```python
age = int(input("Yasinizi girin: "))
```

input her zaman string döndürür, gerekirse dönüşüm yapılır.

---

## 13. Hata Yönetimi (try / except)

```python
try:
    x = int("abc")
except ValueError:
    print("Donusum hatasi")
```

Programın çökmesini engeller.

---

## 14. Hazır Fonksiyonlar

```python
nums = [1, 2, 3]

len(nums)
sum(nums)
min(nums)
max(nums)
```

---

## 15. enumerate()

```python
names = ["Ali", "Veli", "Ayse"]

for index, name in enumerate(names):
    print(index, name)
```
