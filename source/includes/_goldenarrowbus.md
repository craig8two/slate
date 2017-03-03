# Golden Arrow Bus

## Get Golden Arrow bus routes

```javascript
GET: "http://proserver.gometro.co.za/api/v1/ga/routes"
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
    "id": "6:2311",
    "shortName": "147_A",
    "longName": "MFULENILWANDLEMALIBU",
    "mode": "BUS",
    "agencyName": "Golden Arrow"
  },
  {
    "id": "6:2795",
    "shortName": "091_F",
    "longName": "WESPOORTKILLARNEY GARDENSNEW EISLEBEN",
    "mode": "BUS",
    "agencyName": "Golden Arrow"
  },
  {
    "id": "6:2310",
    "shortName": "146_B",
    "longName": "PRESTIGE COLLEGEBELLVILLEMIKE PIENAAR",
    "mode": "BUS",
    "agencyName": "Golden Arrow"
  },
  {
    "id": "6:2794",
    "shortName": "091_E",
    "longName": "KAPTEINSKLIPKILLARNEY GARDENSMERRYDALE",
    "mode": "BUS",
    "agencyName": "Golden Arrow"
  }
 ]
```

This endpoint retrieves Golden Arrow bus routes.


### HTTP Request

`GET <BASEURL>/ga/routes/`

### URL Parameters

There are no query parameters for this endpoint.

## Get Golden Arrow bus stops by route

```javascript
GET: "http://proserver.gometro.co.za/api/v1/ga/routes/6:2311/stops"
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
    "id": "6:S5132",
    "code": "42",
    "name": "BUS 5132",
    "lat": -33.999829,
    "lon": 18.725962
  },
  {
    "id": "6:S5056",
    "code": "4508",
    "name": "BUS 5056",
    "lat": -33.996338,
    "lon": 18.701745
  },
  {
    "id": "6:S5111",
    "code": "1985",
    "name": "BUS 5111",
    "lat": -33.988815,
    "lon": 18.718762
  },
  {
    "id": "6:S5672",
    "code": "3789",
    "name": "BUS 5672",
    "lat": -34.120379,
    "lon": 18.865693
  }
 ]
```

This endpoint retrieves Golden Arrow bus stops by route.


### HTTP Request

`GET <BASEURL>/ga/routes/<routeId>/stops`


### URL Parameters

Parameter | Description
--------- | -----------
routeId | The ID of the route to retrieve stops for

## Get Golden Arrow bus stop details

```javascript
GET: "http://proserver.gometro.co.za/api/v1/ga/stop/6:S5132"
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
  "id": "6:S5132",
  "name": "BUS 5132",
  "lat": -33.999829,
  "lon": 18.725962,
  "code": "42",
  "desc": "Bus Stop5132",
  "locationType": 0,
  "wheelchairBoarding": 0,
  "vehicleType": -999,
  "vehicleTypeSet": false
}
```
This endpoint retrieves info for a specific Golden Arrow bus stop.



### HTTP Request

`GET <BASEURL>/ga/stop/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for
