![WhatsApp Image 2025-12-27 at 12 59 23](https://github.com/user-attachments/assets/db155d48-f201-4d4b-8712-b68472c7fddb)

---

### 1) Artan Üçgen

```
*
* *
* * *
* * * *
* * * * *
```

```python
rows = 5

for i in range(rows):
    for j in range(i + 1):
        print("*", end=" ")
    print()
```

---

### 2) Artan Üçgen (Kısa Yöntem)

```
*
* *
* * *
* * * *
* * * * *
```

```python
rows = 5

for i in range(1, rows + 1):
    print("* " * i)
```

---

### 3) Azalan Üçgen

```
* * * * *
* * * *
* * *
* *
*
```

```python
rows = 5

for i in range(rows, 0, -1):
    for j in range(i):
        print("*", end=" ")
    print()
```

---

### 4) Sağdan Hizalı Azalan Üçgen

```
* * * * *
  * * * *
    * * *
      * *
        *
```

```python
rows = 5
space = 0

for i in range(rows, 0, -1):
    for s in range(space):
        print(" ", end=" ")
    for j in range(i):
        print("*", end=" ")
    print()
    space += 1
```

---

### Özet

* `for` döngüsü
* iç içe döngü
* `range`
* `print(end=" ")`
* hizalama mantığı

---
