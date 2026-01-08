
## TAM VE ÇALIŞAN KOD

```python
import numpy as np
import matplotlib.pyplot as plt
import datetime

# 1. Tarih oluşturma (son 7 gün)
bugun = datetime.date.today()
tarihler = [bugun - datetime.timedelta(days=i) for i in range(6, -1, -1)]

# 2. NumPy ile günlük satış verileri (rastgele)
satislar = np.array([120, 150, 100, 170, 160, 180, 200])

# 3. NumPy ile istatistiksel işlemler
ortalama = satislar.mean()
toplam = satislar.sum()
maksimum = satislar.max()
minimum = satislar.min()

print("Satış Ortalaması:", ortalama)
print("Toplam Satış:", toplam)
print("En Yüksek Satış:", maksimum)
print("En Düşük Satış:", minimum)

# 4. Tarihleri string formata çevirme
tarih_str = [t.strftime("%d-%m-%Y") for t in tarihler]

# 5. Matplotlib ile grafik çizimi
plt.figure()
plt.plot(tarih_str, satislar, marker='o')

plt.title("Son 7 Günlük Satış Grafiği")
plt.xlabel("Tarih")
plt.ylabel("Satış Miktarı")

plt.grid(True)
plt.show()
```

---

## KODDA NE VAR? (Özet)

### datetime

- `date.today()`
    
- `timedelta(days=)`
    
- `strftime()` ile string dönüşümü
    

### NumPy

- `np.array`
    
- `mean()`
    
- `sum()`
    
- `max()`
    
- `min()`
    

### Matplotlib

- `plot()`
    
- `title()`
    
- `xlabel()`, `ylabel()`
    
- `show()`
    

