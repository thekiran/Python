# Python Listeler (List)

## 1. List Nedir?

List, Python’da sıralı, değiştirilebilir ve birden fazla veri tipini aynı anda tutabilen bir koleksiyon yapısıdır.

```python
numbers = [1, 2, 3, 4]
mixed = [1, "python", True, 3.14]
empty = []
```

## 3. Index ve Negatif Index

```python
items = ["a", "b", "c", "d"]

print(items[0])   # a
print(items[-1])  # d
```

---

## 4. Slicing (Dilimleme)

```python
nums = [0, 1, 2, 3, 4, 5]

nums[1:4]    # [1, 2, 3]
nums[:3]     # [0, 1, 2]
nums[::2]    # [0, 2, 4]
nums[::-1]   # [5, 4, 3, 2, 1, 0]
```

---

## 5. Listeye Eleman Ekleme

### append()

```python
lst = [1, 2]
lst.append(3)
```

### insert()

```python
lst.insert(1, 100)
```

### extend()

```python
lst.extend([4, 5, 6])
```

---

## 6. Listeden Eleman Silme

### remove()

```python
lst.remove(100)
```

### pop()

```python
lst.pop()    # sondan siler
lst.pop(0)   # index 0
```

### del

```python
del lst[1]
```

### clear()

```python
lst.clear()
```

---

## 7. Arama ve Kontrol

```python
nums = [10, 20, 30]

20 in nums
nums.index(30)
nums.count(10)
```

---

## 8. Döngüler ile Listeler

```python
for item in nums:
    print(item)
```

Index ile:

```python
for i in range(len(nums)):
    print(i, nums[i])
```

---

## 9. Sıralama ve Ters Çevirme

```python
nums.sort()
nums.sort(reverse=True)
```

```python
sorted_nums = sorted(nums)
```

```python
nums.reverse()
```

---

## 10. Liste Kopyalama (Önemli)

```python
a = [1, 2, 3]
b = a          # referans
c = a.copy()   # gerçek kopya
```

Referans ile kopyalama, iki değişkenin aynı listeyi göstermesine sebep olur.

---

## 11. List Comprehension

```python
squares = [i * i for i in range(5)]
```

Şartlı kullanım:

```python
evens = [i for i in range(10) if i % 2 == 0]
```

---

## 12. İç İçe Listeler (Nested List)

```python
matrix = [
    [1, 2],
    [3, 4],
    [5, 6]
]

matrix[1][0]  # 3
```

---

## 13. Listeler ile Fonksiyonlar

```python
nums = [1, 2, 3, 4]

len(nums)
max(nums)
min(nums)
sum(nums)
```

---

## 14. String ve Liste Dönüşümleri

### String → List

```python
text = "python"
chars = list(text)
```

### List → String

```python
words = ["hello", "world"]
result = " ".join(words)
```

---

## 15. Performans Bilgisi

- append(): O(1)
    
- pop(): O(1)
    
- insert(): O(n)
    
- remove(): O(n)
    
- arama: O(n)
    

Büyük listelerde append tercih edilmelidir.

---

## 16. Sık Yapılan Hatalar

```python
lst = [1, 2, 3]
lst = lst.append(4)
```

append metodu None döndürür. Doğru kullanım:

```python
lst.append(4)
```

---
