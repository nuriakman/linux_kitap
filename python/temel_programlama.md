# Temel Programlama

Python, kolay okunabilen, platform bağımsız, yorumlanan bir dildir. Bugün sadece sistem yöneticileri tarafından değil, pek çok ticari yazılım geliştiricisi tarafından da yaygınca kullanılmaktadır. Ayrıca geniş kütüphane desteği ve yüksek matematiksel hassasiyeti sayesinde temel bilimcilerin programlama alanında da oldukça yaygın hale gelmiştir.

Aşağıda örnek bir Python kodu görülmektedir.

```python
# ornek1.py
cumle = "Python'un ismi Monty Python'dan gelir."
if len(cumle) > 37:
    print cumle
```
Yukarıdaki programı ornek1.py ismiyle kaydedip çalıştırdığımızda aşağıdaki gibi bir sonuç alırız.

```
python ornek1.py
Python'un ismi Monty Python'dan gelir.
```

Yazılımın yaptığı işlem oldukça basittir. **cumle** değişkeninin değerinin uzunluğu 37 karakterdan fazlaysa, kendisini ekrana yazdırır.

Burada dikkat edilmesi gereken nokta, Python'un "indentation" hassasiyetinin olmasıdır. Yani kullandığımız "if" bloğunu bir parantez içinde ifade edemezdik, Python bu bloğun içindeki karakterlerin hizalı olmasını ister. Bu hizalılık ister boşluk karakterleriyle, ister tab karakterleriyle verilmelidir, yeter ki programın tamamında tutarlı olunsun.

* Indentation için kullanılan standart genellikle 4 karakter olup tab yerine boşluk kullanmaktır.

Şimdi aşağıdaki örneğe bakalım.

```python
# ornek2.py
isim = "Rossum"
cumle = "Python'un ismi %s'dan gelir." % isim
if len(cumle) > 37:
    print cumle
else:
    print cumle[:-7] + " gelmez mi?"
```

```
python ornek2.py
Python'un ismi Rossum'dan gelmez mi?
```

Bu örnekte birkaç işlemi bir arada kullandık. Öncelikle **isim** değişkeni tanımladık, daha sonra bu değişkenin değerini **cumle** değişkeninin içinde kullandık. Ancak cümleyi ekrana yazdırırken, eğer uzunluğu 37'den kısaysa cümlenin son 7 karakterini almadan kullandık, sonra da peşine " gelmez mi?" ifadesini ekledik.

Bu örneği daha parametrik hale getirmek istersek,

```python
# ornek3.py
def yazdir(isim):
    cumle = "Python'un ismi %s'dan gelir." % isim
    if len(cumle) > 37:
        print cumle
    else:
        print cumle[:-7] + " gelmez mi?"

yazdir("Monty Python")
yazdir("Rossum") 
```

Koddan anlaşılacağı üzere, önce bir fonksiyon tanımladık. Bu fonksiyon aldığı değeri cümlemizin içine yerleştiriyor. Sonra oluşan uzunluğa göre karar veriyor: Eğer oluşan cümle 37 karakter'den uzunsa doğrudan ekrana yazdırıyor, değilse farklı bir cümle yazdırıyor.

Tanımladığımız fonksiyonun ekrana yazdırmasını sağlamak yerine, değeri döndürmesini de sağlayabilirdik. Bu durumda dönen değeri ayrıca ekrana yazmamız gerekirdi. Aynı kodun değiştirilmiş aşağıdaki hali bu paragrafı daha anlamlı kılacaktır.

```python
# ornek3.py
def yazdir(isim):
    cumle = "Python'un ismi %s'dan gelir." % isim
    if len(cumle) > 37:
        return cumle
    else:
        return cumle[:-7] + " gelmez mi?"

print yazdir("Monty Python")
print yazdir("Rossum") 
```

