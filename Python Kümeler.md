## 1. Set Nedir?

Set, Python’da:

- Sırasız (unordered)
    
- Benzersiz (unique)
    
- Değiştirilebilir (mutable)
    

olan bir koleksiyon yapısıdır.

Aynı elemandan **birden fazla olamaz**.

```python
numbers = {1, 2, 3, 4}
mixed = {1, "python", True, 3.14}
empty = set()      # boş set
```

Not: `{}` boş dictionary oluşturur, boş set değildir.

---

## 2. Temel Özellikler

- Sırasızdır (index yoktur)
    
- Elemanlar benzersizdir
    
- Değiştirilebilir
    
- Iterable (döngü ile gezilebilir)
    
- Matematiksel küme işlemlerini destekler
    

---

## 3. Set Oluşturma

```python
s1 = {1, 2, 3}
s2 = set([3, 4, 5])
```

Tekrar eden değerler otomatik silinir:

```python
s = {1, 2, 2, 3, 3}
print(s)   # {1, 2, 3}
```

---

## 4. Set’e Eleman Ekleme

### add()

```python
s = {1, 2}
s.add(3)
```

### update()

```python
s.update([4, 5, 6])
```

---

## 5. Set’ten Eleman Silme

### remove()

```python
s.remove(2)   # yoksa hata verir
```

### discard()

```python
s.discard(10)  # yoksa hata vermez
```

### pop()

```python
s.pop()   # rastgele eleman siler
```

### clear()

```python
s.clear()
```

---

## 6. Eleman Kontrolü

```python
nums = {10, 20, 30}

20 in nums
40 not in nums
```

---

## 7. Döngü ile Set

```python
for item in nums:
    print(item)
```

Set sırasız olduğu için her çalışmada farklı sırada gelebilir.

---

## 8. Küme İşlemleri (ÇOK ÖNEMLİ)

```python
a = {1, 2, 3}
b = {3, 4, 5}
```

### Birleşim (Union)

```python
a | b
a.union(b)
```

### Kesişim (Intersection)

```python
a & b
a.intersection(b)
```

### Fark (Difference)

```python
a - b
a.difference(b)
```

### Simetrik Fark

```python
a ^ b
a.symmetric_difference(b)
```

---

## 9. Küme Karşılaştırmaları

```python
a = {1, 2}
b = {1, 2, 3}
```

```python
a.issubset(b)     # True
b.issuperset(a)   # True
a.isdisjoint({5}) # True
```

---

## 10. Set Comprehension

```python
squares = {x * x for x in range(5)}
```

Şartlı kullanım:

```python
evens = {x for x in range(10) if x % 2 == 0}
```

---

## 11. List → Set / Set → List

### Tekrarları Temizleme (çok yaygın kullanım)

```python
nums = [1, 2, 2, 3, 3, 4]
unique_nums = list(set(nums))
```

---

## 12. Set ile Fonksiyonlar

```python
nums = {1, 2, 3, 4}

len(nums)
max(nums)
min(nums)
sum(nums)
```

---

## 13. Performans Bilgisi

- Eleman arama: O(1)
    
- add(): O(1)
    
- remove(): O(1)
    

Set, **arama ve karşılaştırma** işlemlerinde listeden çok daha hızlıdır.

---

## 14. Sık Yapılan Hatalar

Index kullanımı:

```python
s = {1, 2, 3}
s[0]   # HATA
```

Set sırasızdır, index yoktur.

---

## 15. Set ve List Karşılaştırması

|Set|List|
|---|---|
|Sırasız|Sıralı|
|Benzersiz|Tekrar olabilir|
|Hızlı arama|Daha yavaş arama|
|Index yok|Index var|

---
