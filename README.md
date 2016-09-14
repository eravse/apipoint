# ApiPoint

ApiPoint SharePoint-Tr tarafından geliştirilen ve yayınlanan ücretsiz bir Json ve XML servisleridir. Bu sevisler SharePoint Online ve SharePoint on-prem kullanıcılarının web partları üzerinde kullanabileceği basit ve hızlı entegrasyonlar için arayüzler sağlamayı hedeflemektedir. 

ApiPoint geliştirilme esnasında token olmaksızın hizmete girecek olup, release aşamasında kullanıcıların sharepoint tenant ve gerekli bilgileri girerek secret key ve token oluşturulmaları istenecektir.

ApiPoint base adres olarak https://apipoint.sharepoint-tr.com adresinden çalışmaktadır. Metodların kullanım detayları aşağıda belirtilmiştir. 

Saygılarımızla 

#Weather Service
Weather Servis API üzerinden bulunduğunuz il yada coordinatların hava durumunu Open Weather Servisini kullanarak size döndürür.

Weather Api çağırım adresi https://apipoint.sharepoint-tr.com/apipoint/weather/getWeather dur. 
## Parametreler 
* RequestType: 0 <b> (  ByCityName = 0,        ByCoordinates = 1,        ByCityId = 2 )</b>
* Format : 0  <b>(jSon = 0,        Xml = 1,        Html = 2,) // Servis şu anda sadece json olarak dönüş yapmaktadır.</b>
* UnitType: 1 <b>(Imperial = 0,        Metrics = 1) </b>
* Q: "Çanakkale" <b>(şehir ismi Request Type'a göre değer alır.)</b>
* Lat: "sample string 2" <b>(Request Type ByCoordinates seçilirse kullanılır)</b>
* Lon: "sample string 3" <b>(Request Type ByCoordinates seçilirse kullanılır)</b>


## Sample Request  
> Requestler sadece POST olarak çalışır.

<code>
{
"RequestType": 0,
"Format": 0,
"UnitType": 1,
"Q": "Çanakkale",
"Lat": "sample string 2",
"Lon": "sample string 3"
}
</code>

## Weather Service Limits
Servis ücretsiz kullanıma açık olduğundan Open Weather API sinin ücretsiz planını kullanır ve bu plana ait limitler aynen ApiPoint içinde geçerlidir. Aşağıdaki limitler uygulanır.

* Calls 10min: 600 
* Calls 1day: 50,000 
* Threshold: 7,200 
* Hourly forecast: 5 
* Daily forecast: 0 


Erdem Avni SELÇUK
eravse@gmail.com
