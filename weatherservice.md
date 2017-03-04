
#Weather Service
Weather Servis API üzerinden bulunduğunuz il yada coordinatların hava durumunu Open Weather Servisini kullanarak size döndürür.

Weather Api çağırım adresi https://apipoint.sharepoint-tr.com/weather/getWeather . 

### Parametreler 
* RequestType: 0 <b> (  ByCityName = 0,        ByCoordinates = 1,        ByCityId = 2 )</b>
* Format : 0  <b>(jSon = 0,        Xml = 1,        Html = 2,) // Servis şu anda sadece json olarak dönüş yapmaktadır.</b>
* UnitType: 1 <b>(Imperial = 0,        Metrics = 1) </b>
* Q: "Çanakkale" <b>(şehir ismi Request Type'a göre değer alır.)</b>
* Lat: "sample string 2" <b>(Request Type ByCoordinates seçilirse kullanılır)</b>
* Lon: "sample string 3" <b>(Request Type ByCoordinates seçilirse kullanılır)</b>


### Sample Request  
> Requestler sadece POST olarak çalışır.

```javascript
{
"RequestType": 0,
"Format": 0,
"UnitType": 1,
"Q": "Çanakkale",
"Lat": "sample string 2",
"Lon": "sample string 3"
}
```

### Sample Output 

```javascript
{
  "coord": {
    "lon": 29.08,
    "lat": 40.17
  },
  "weather": [
    {
      "id": 800,
      "main": "Clear",
      "description": "clear sky",
      "icon": "01n"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 5,
    "pressure": 1022,
    "humidity": 60,
    "temp_min": 5,
    "temp_max": 5
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.5,
    "deg": 70
  },
  "clouds": {
    "all": 0
  },
  "dt": 1488653400,
  "sys": {
    "type": 1,
    "id": 6057,
    "message": 0.0021,
    "country": "TR",
    "sunrise": 1488601883,
    "sunset": 1488643174
  },
  "id": 750268,
  "name": "Bursa",
  "cod": 200
}
```

### Weather Service Limits
Servis ücretsiz kullanıma açık olduğundan Open Weather API sinin ücretsiz planını kullanır ve bu plana ait limitler aynen ApiPoint içinde geçerlidir. Aşağıdaki limitler uygulanır.

* Calls 10min: 600 
* Calls 1day: 50,000 
* Threshold: 7,200 
* Hourly forecast: 5 
* Daily forecast: 0 
