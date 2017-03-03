# MyCiti

## Get MyCiti routes

```javascript
GET: "http://proserver.gometro.co.za/api/v1/myciti/routes"
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "10:1101",
    "shortName": "D01",
    "longName": "Khayelitsha East - Civic Centre",
    "mode": "TRAM",
    "color": "f0648b",
    "agencyName": "MyCiti"
  },
  {
    "id": "10:1103",
    "shortName": "D03",
    "longName": "Mitchells Plain East - Civic Centre",
    "mode": "TRAM",
    "color": "74c599",
    "agencyName": "MyCiti"
  },
  {
    "id": "10:2001",
    "shortName": "A01",
    "longName": "Airport - Civic Centre",
    "mode": "TRAM",
    "color": "899AA5",
    "agencyName": "MyCiti"
  }
]
```

This endpoint retrieves MyCiti routes.


### HTTP Request

`GET <BASEURL>/myciti/routes/`

### URL Parameters

There are no query parameters for this endpoint.

## Get MyCiti stops by route

```javascript
GET: "http://proserver.gometro.co.za/api/v1/myciti/routes/10:1101/stops"
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "10:348",
    "name": "Lindela",
    "lat": -34.056993,
    "lon": 18.69717033
  },
  {
    "id": "10:29",
    "name": "Civic Centre",
    "lat": -33.92082723,
    "lon": 18.42985692
  },
  {
    "id": "10:347",
    "name": "Kuyasa",
    "lat": -34.0553875,
    "lon": 18.691905
  },
  {
    "id": "10:355",
    "name": "Vuyani",
    "lat": -34.03724,
    "lon": 18.68092267
  }
]
```

This endpoint retrieves our Cape Town taxi stops by route.


### HTTP Request

`GET <BASEURL>/myciti/routes/<routeId>/stops`


### URL Parameters

Parameter | Description
--------- | -----------
routeId | The ID of the route to retrieve stops for

## Get MyCiti stop details

```javascript
GET: "http://proserver.gometro.co.za/api/v1/myciti/stop/10:348"
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": "10:348",
  "name": "Lindela",
  "lat": -34.056993,
  "lon": 18.69717033,
  "locationType": 0,
  "wheelchairBoarding": 0,
  "vehicleType": -999,
  "vehicleTypeSet": false
}
```
This endpoint retrieves info for a specific MyCiti stop.



### HTTP Request

`GET <BASEURL>/myciti/stop/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for
