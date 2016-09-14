# ApiPoint

ApiPoint SharePoint-Tr tarafından geliştirilen ve yayınlanan ücretsiz bir Json ve XML servisleridir. Bu sevisler SharePoint Online ve SharePoint on-prem kullanıcılarının web partları üzerinde kullanabileceği basit ve hızlı entegrasyonlar için arayüzler sağlamayı hedeflemektedir. 

ApiPoint geliştirilme esnasında token olmaksızın hizmete girecek olup, release aşamasında kullanıcıların sharepoint tenant ve gerekli bilgileri girerek secret key ve token oluşturulmaları istenecektir.

ApiPoint base adres olarak https://apipoint.sharepoint-tr.com adresinden çalışmaktadır. Metodların kullanım detayları aşağıda belirtilmiştir. 

Saygılarımızla 

#Weather Service
Weather Servis API üzerinden bulunduğunuz il yada coordinatların hava durumunu Open Weather Servisini kullanarak size döndürür.

Weather Api çağırım adresi https://apipoint.sharepoint-tr.com/apipoint/weather/getWeather dur. 

## Sample Request  
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
