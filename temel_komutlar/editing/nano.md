# nano ve pico

nano ve pico programları aslında birbirlerinin aynısıdır. Pico (Pine composer) geliştirildiğinde bir *free software license* altında dağıtılmadığından, kodun değiştirilerek dağıtılması yasal değildi. Dolayısıyla GNU Projesi kapsamında pico'nun işlemlerini taklit eden bir program geliştirildi ve ismi **nano** oldu. Bugün **nano** orijinal pico'dan daha kapsamlı duruma gelmiştir. Kullandığınız Linux dağıtımlarında pico komutu da aslında nano'yu çalıştırmaktadır.

Aslında pico için özgür lisanslı bir yazılım amacıyla Chris Allegretta tarafından nano ile geliştirildiğinde ismi TIP konuldu *(This isn't Pico)*, ancak Unix üzerindeki *tip* yazılımı ile karışabileceği gerekçesiyle ismi daha sonra *nano* olarak değiştirildi. *nano* SI birim sisteminde *pico*dan 1000 kat daha büyük olan bir uzunluk birimidir.

nano ve pico farklarının yaratacağı kafa karışıklığını giderdiysek, programın genel kullanımına bakabiliriz.

Önceki bölümde crc8.py dosyamızın yetkilerini görüntülemiştik.

Eğer aşağıdaki örnekleri gerçek crc8.py dosyasıyla kullanmak istiyorsanız **wget** ile dosyayı edinebilirsiniz.

```bash
wget http://bit.ly/1kBiBAE -O crc8.py
```

Yukarıdaki komut, *github* üzerinde ilgili *gist*'i indirip mevcut dizinin *crc8.py* dosyasına yazacaktır.

Şimdi dosyanın içeriğine göz atalım. Dosyaya GNU/Linux üzerinde cat, less, more, head gibi komutlarla göz atabiliriz. Ancak dosyanın içeriğini değiştirmek için bu yöntemler pratik olmayacaktır. Dosyanın bulunduğu dizinde aşağıdaki komutlardan birini çalıştırarak dosyayı nano ile açabiliriz.

```bash
nano crc8.py
pico crc8.py
```

![](nano.png)

Burada dosyamızın içeriğini görüyoruz. Kullandığımız dağıtımda nano dosyanın uzantısına bakarak dosyamızın içeriğinin bir Python kodu olduğunu anlıyor ve gerekli renklendirmeyi yapıyor.

Alt iki satırda gördüğünüz komutlar, klavye kısayollarıyla erişiliyor. Komutlara erişmek için CTRL ile birlikte ilgili kısayolu kullanmak gerekiyor. Örneğin "Get Help" fonksiyonunu çağırmak için CTRL+g tuşlarına basmak gerekiyor. Gelen menüden nano için kullanılabilecek bütün komutları görebilirsiniz.

![](nano2.png)

nano içerisinde gezinmek için ok tuşlarını kullanmanız yeterli. Değiştirmek/eklemek/silmek istediğiniz noktaya imleci getirdiğinizde istediğiniz değişikliği yaptıktan sonra dosyayı kaydetmek için CTRL+o programdan çıkmak içinse CTRL+x tuşlarını kullanmanız yeterlidir.

Dosyamızın en başında # işaretleriyle başlayan bir dizi satır görülüyor. Bu satırlar açıklama satırlarıdır, yani Python yorumlayıcısı tarafından bu satırlar gözardı edilecektir. Çoğu programlama dilinde ve çoğu ayar dosyasında açıklama satırları # işareti ile başlar.

nano, açıklama satırlarını istersek hizalı hale getirebilir. Bunun için 
*Justify* ve *Unjustify* komutları kullanılabilir.

İmleci açıklama satırlarının olduğu bölgeye getirip CTRL+j ile satırları hizalayabiliriz. 

![](nano3.png)

Ekranda *Can now UnJustify!* yazısı belirdi. Değişikliği gördükten sonra CTRL+u ile tekrar eski haline getirebiliriz.