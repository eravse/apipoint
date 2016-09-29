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
Ülkeye ait şehirlerin listelenmesine yarar. GetCountry metodundan alınan değerin POST edilmesi sureti ile ülkeye ait şehirlerin listesini döndürür. 

> POST Metodu ile https://apipoint.sharepoint-tr.com/salatTimes/getCities adresinden tetiklenir.

### Sample Request 
<code>
{
  "CountryID": 2 // Türkiye
}
</code>

### Sample Response 
<code>
[
  {
    "SehirAdi": "ADANA",
    "SehirAdiEn": "ADANA",
    "SehirID": "500"
  },
  {
    "SehirAdi": "ADIYAMAN",
    "SehirAdiEn": "ADIYAMAN",
    "SehirID": "501"
  },
</code>

## GetTown
GetTown mevcut namaz vakitlerinin tanımlandığı ilçeleri listelemek için kullanılan metoddur. 

> POST Metodu ile https://apipoint.sharepoint-tr.com/salatTimes/getTown adresinden tetiklenir.


### Sample Request 
<code>
{<br>
  "CityID": 501 // ADIYAMAN<br>
}<br>
</code>

### Sample Response 
<code>
[
  {
    "IlceAdi": "ADIYAMAN",
    "IlceAdiEn": "ADIYAMAN",
    "IlceID": "9158"
  },
  {
    "IlceAdi": "BESNİ",
    "IlceAdiEn": "BESNI",
    "IlceID": "9159"
  },.....
</code>


## GetDailySalatTimes
