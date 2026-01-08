# 1) NumPy (Numerical Python)

## 1.1 NumPy Nedir?

NumPy, Python’da **sayısal hesaplama** yapmak için kullanılan temel kütüphanedir.

- Çok boyutlu diziler (ndarray)
    
- Yüksek performans
    
- Matematiksel ve istatistiksel işlemler
    
- Bilimsel ve veri analizinin temeli
    

Kurulum:

```bash
pip install numpy
```

İçe aktarma:

```python
import numpy as np
```

---

## 1.2 ndarray (NumPy Dizisi)

### Liste vs NumPy Dizisi

```python
import numpy as np

liste = [1, 2, 3]
dizi = np.array([1, 2, 3])

print(liste * 2)   # [1, 2, 3, 1, 2, 3]
print(dizi * 2)    # [2 4 6]
```

NumPy dizileri **eleman bazlı işlem** yapar.

---

## 1.3 Dizi Oluşturma Yöntemleri

```python
np.array([1, 2, 3])
np.zeros(5)
np.ones(5)
np.arange(0, 10, 2)
np.linspace(0, 1, 5)
np.random.rand(3)
np.random.randint(1, 10, 5)
```

---

## 1.4 Çok Boyutlu Diziler (Matrix)

```python
matris = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(matris)
print(matris.shape)   # (2, 3)
print(matris.ndim)    # 2
```

---

## 1.5 Indexleme ve Dilimleme

```python
dizi = np.array([10, 20, 30, 40, 50])

print(dizi[0])
print(dizi[-1])
print(dizi[1:4])
```

Matris:

```python
matris = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(matris[0, 1])   # 2
print(matris[:, 1])   # 2. sütun
```

---

## 1.6 Matematiksel İşlemler

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print(a + b)
print(a * b)
print(a ** 2)
print(np.sqrt(a))
```

---

## 1.7 İstatistiksel Fonksiyonlar

```python
dizi = np.array([10, 20, 30, 40])

print(np.mean(dizi))
print(np.sum(dizi))
print(np.min(dizi))
print(np.max(dizi))
print(np.std(dizi))
```

---

## 1.8 Mantıksal İşlemler ve Filtreleme

```python
dizi = np.array([10, 25, 30, 5, 60])

print(dizi[dizi > 20])
```

---

# 2) Matplotlib

## 2.1 Matplotlib Nedir?

Matplotlib, Python’da **grafik ve veri görselleştirme** için kullanılan kütüphanedir.

Kurulum:

```bash
pip install matplotlib
```

İçe aktarma:

```python
import matplotlib.pyplot as plt
```

---

## 2.2 Basit Çizgi Grafiği

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 25, 30]

plt.plot(x, y)
plt.show()
```

---

## 2.3 Başlık ve Etiketler

```python
plt.plot(x, y)
plt.title("Satış Grafiği")
plt.xlabel("Ay")
plt.ylabel("Satış")
plt.show()
```

---

## 2.4 Çoklu Çizgi Grafiği

```python
y2 = [5, 15, 20, 35]

plt.plot(x, y, label="Ürün A")
plt.plot(x, y2, label="Ürün B")
plt.legend()
plt.show()
```

---

## 2.5 Scatter (Nokta) Grafiği

```python
plt.scatter(x, y)
plt.show()
```

---

## 2.6 Bar (Sütun) Grafiği

```python
urunler = ["A", "B", "C"]
satis = [100, 150, 80]

plt.bar(urunler, satis)
plt.show()
```

---

## 2.7 Histogram

```python
import numpy as np

veri = np.random.randn(1000)
plt.hist(veri, bins=30)
plt.show()
```

---

## 2.8 Figure ve Subplot

```python
plt.figure(figsize=(8, 4))
plt.plot(x, y)
plt.show()
```

```python
plt.subplot(1, 2, 1)
plt.plot(x, y)

plt.subplot(1, 2, 2)
plt.plot(x, y2)

plt.show()
```

---

# 3) datetime

## 3.1 datetime Nedir?

`datetime`, Python’un **tarih ve saat** işlemleri için yerleşik kütüphanesidir.

```python
from datetime import datetime, date, time, timedelta
```

---

## 3.2 Şu Anki Tarih ve Saat

```python
now = datetime.now()
print(now)
```

---

## 3.3 Tarih Oluşturma

```python
tarih = date(2025, 1, 9)
print(tarih)
```

---

## 3.4 Saat Oluşturma

```python
saat = time(14, 30, 0)
print(saat)
```

---

## 3.5 Tarih + Saat Birlikte

```python
dt = datetime(2025, 1, 9, 14, 30)
print(dt)
```

---

## 3.6 Tarih Bileşenleri

```python
print(now.year)
print(now.month)
print(now.day)
print(now.hour)
```

---

## 3.7 timedelta (Tarih Hesaplama)

```python
bugun = datetime.now()
yarin = bugun + timedelta(days=1)
once = bugun - timedelta(days=7)

print(yarin)
print(once)
```

---

## 3.8 String ↔ datetime Dönüşümü

### String → datetime

```python
tarih_str = "2025-01-09 15:45"
dt = datetime.strptime(tarih_str, "%Y-%m-%d %H:%M")
print(dt)
```

### datetime → String

```python
print(dt.strftime("%d/%m/%Y %H:%M"))
```

---

# 4) NumPy + Matplotlib + datetime Birlikte Örnek

```python
import numpy as np
import matplotlib.pyplot as plt
from datetime import datetime, timedelta

gunler = [datetime.now() + timedelta(days=i) for i in range(7)]
satis = np.random.randint(50, 150, 7)

plt.plot(gunler, satis)
plt.title("7 Günlük Satış")
plt.xlabel("Tarih")
plt.ylabel("Satış")
plt.show()
```

---

## Özet

- **NumPy**: Veri üretme, matematik, istatistik
    
- **Matplotlib**: Veriyi görselleştirme
    
- **datetime**: Zaman ve tarih yönetimi
    
- Birlikte kullanıldığında **veri analizi ve raporlama** yapılır
    

