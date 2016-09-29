# Kuran-ı Kerim Servisi 
Kuran-ı Kerim servisi şu an için sadece türkçe ve arapça olarak hizmet vermektedir. İstenilen sure ya da ayetin arapçasını ve türkçe mealini sizlere döner.
 
API erişim adresi https://apipoint.sharepoint-tr.com/quran/ altında çalışmaktadır. Metodların URL leri için metod açıklamalarını takip ediniz.

> Quran servisindeki tüm metodlar POST yöntemi ile çağırılmalıdır.

## Metodlar

* GetQuranList 
* GetPage
* GetJuz
* GetSurah
* GetAyah
* GetRandomAyah


## GetQuranList
Türkçe Kuran-ı Kerimlerin listesini verir. Bu lsteye göre istediğiniz mealleri API üzerinden çekebilirsiniz. 
API  https://apipoint.sharepoint.com/quran/getQuranList adresinden POST Methodu ile erişilir. Metod şu an için herhangi bir parametre almamaktadır. 

### Sample Response 
```javascript
[
  {
    "QuranID": "tr.ates",
    "AuthorName": "Süleyman Ateş",
    "TextSource": "Tanzil.net"
  },
  {
    "QuranID": "tr.bulac",
    "AuthorName": "Ali Bulaç",
    "TextSource": "Tanzil.net"
  },......
```
 
 QuranID : Mealin benzersiz adıdır ve diğer methodlarda kullanılmaktadır.
 AuthorName : Meal yazarının adı veya yayıncı kurumun adıdır. Bilglendirme amaçlıdır.
 TextSource : Mealin kaynak adresidir.
 
 
## GetPage
Sayfa numarasına göre Kuran-ı Kerim meali döndürür.

## GetJuz

## GetSurah

## GetAyah

## GetRandomAyah


<hr>
> Eğer QuranID değeri boş geçilirse QuranID ihtiyacı duyan tüm methodlar Diyanet Vakfı meaili döndürür.