# Salat Times Service ( Namaz Vakitleri Servisi )
Namaz vakitleri servisi Türkiye Cumhuriyeti Diyanet İşleri Bakanlığınca sağlanan namaz vakitlerini kullanıcılara hızlı arayüz olarak döndürür.

API erişim adresi https://apipoint.sharepoint-tr.com/salatTimes/ altında çalışmaktadır. Metodların URL leri için metod açıklamalarını takip ediniz.

> SalatTimes servisindeki tüm metodlar POST yöntemi ile çağırılmalıdır.

## Metodlar

* GetCountry
* GetCity
* GetTown
* GetDailySalatTimes

## GetCountry

GetCountry mevcut namaz vakitlerinin tanımlandığı ülkeleri listelemek için kullanılan metoddur. 
https://apipoint.sharepoint-tr.com/salatTimes/GetCountry adresinden <b>POST</b> yöntemi ile çağırılır.

### Sample Response
<code>
[
  {
    "UlkeAdi": "ABD",
    "UlkeAdiEn": "ABD",
    "UlkeID": "33"
  },
  {
    "UlkeAdi": "AFGANISTAN",
    "UlkeAdiEn": "AFGANISTAN",
    "UlkeID": "166"
  },....
</code>

## GetCity
## GetTown
## GetDailySalatTimes
