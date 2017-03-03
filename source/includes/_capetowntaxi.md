# Cape Town Taxis

<aside class="success">
Remember — Our API uses FERRY mode for taxi's 
</aside>

## Get taxi routes

```javascript
GET: "http://proserver.gometro.co.za/api/v1/taxi/routes"
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
    "id": "11:8806774",
    "shortName": "CAPETX27",
    "longName": "BaysideToDunoon",
    "mode": "FERRY",
    "agencyName": "Cape Town Taxis"
  },
  {
    "id": "11:6943042",
    "shortName": "CAPETX142",
    "longName": "GugulethuToNyanga",
    "mode": "FERRY",
    "agencyName": "Cape Town Taxis"
  },
  {
    "id": "11:6853105",
    "shortName": "CAPETX371",
    "longName": "MitchellsPlainToMowbry",
    "mode": "FERRY",
    "agencyName": "Cape Town Taxis"
  }
 ]
```

This endpoint retrieves our Cape Town taxi routes.


### HTTP Request

`GET <BASEURL>/taxi/routes/`

### URL Parameters

There are no query parameters for this endpoint.

## Get taxi stops by route

```javascript
GET: "http://proserver.gometro.co.za/api/v1/taxi/routes/11:8806774/stops"
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
    "id": "11:8806781",
    "code": "8806774",
    "name": "Taxi Stop300",
    "lat": -33.83123,
    "lon": 18.51384
  },
  {
    "id": "11:8806785",
    "code": "8806774",
    "name": "Taxi Stop298",
    "lat": -33.83306,
    "lon": 18.526136
  },
  {
    "id": "11:8806775",
    "code": "8806774",
    "name": "Taxi Stop303",
    "lat": -33.82508,
    "lon": 18.49072
  },
  {
    "id": "11:8806783",
    "code": "8806774",
    "name": "Taxi Stop299",
    "lat": -33.831665,
    "lon": 18.515657
  },
  {
    "id": "11:8806779",
    "code": "8806774",
    "name": "Taxi Stop301",
    "lat": -33.829384,
    "lon": 18.507118
  },
  {
    "id": "11:8806777",
    "code": "8806774",
    "name": "Taxi Stop302",
    "lat": -33.826954,
    "lon": 18.497896
  }
]
```

This endpoint retrieves our Cape Town taxi stops by route.


### HTTP Request

`GET <BASEURL>/taxi/routes/<routeId>/stops`


### URL Parameters

Parameter | Description
--------- | -----------
routeId | The ID of the route to retrieve stops for

## Get taxi stop details

```javascript
GET: "http://proserver.gometro.co.za/api/v1/taxi/stop/11:8806781"
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
  "id": "11:8806781",
  "name": "Taxi Stop300",
  "lat": -33.83123,
  "lon": 18.51384,
  "code": "8806774",
  "desc": "Cape town road300",
  "locationType": 0,
  "wheelchairBoarding": 0,
  "vehicleType": -999,
  "vehicleTypeSet": false
}
```
This endpoint retrieves info for a specific stop in our Cape Town taxi data.



### HTTP Request

`GET <BASEURL>/taxi/stop/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for
