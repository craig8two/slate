# Metrorail

Currently only the Western Cape region is supported

## Get rail routes

```javascript
GET: "http://proserver.gometro.co.za/api/v1/rail/routes"
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
    "id": "13:90000160",
    "longName": "CapeFlats",
    "mode": "RAIL",
    "color": "905846",
    "agencyName": "Metrorail Western Cape"
  },
  {
    "id": "13:90000164",
    "longName": "Malmesbury",
    "mode": "RAIL",
    "color": "00A651",
    "agencyName": "Metrorail Western Cape"
  },
  {
    "id": "13:90000163",
    "longName": "Central",
    "mode": "RAIL",
    "color": "00BAF2",
    "agencyName": "Metrorail Western Cape"
  },
  {
    "id": "13:90000175",
    "longName": "Southern",
    "mode": "RAIL",
    "color": "ED1C24",
    "agencyName": "Metrorail Western Cape"
  },
  {
    "id": "13:90000128",
    "longName": "Northen",
    "mode": "RAIL",
    "color": "3C763D",
    "agencyName": "Metrorail Western Cape"
  }
]
```

This endpoint retrieves all rail routes.


### HTTP Request

`GET <BASEURL>/rail/routes/`

### URL Parameters

There are no query parameters for this endpoint.

## Get rail stops by route

```javascript
GET: "http://proserver.gometro.co.za/api/v1/rail/routes/13:90000160/stops"
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
    "id": "13:f12",
    "code": "f12",
    "name": "Athlone",
    "lat": -33.962688,
    "lon": 18.502
  },
  {
    "id": "13:f16",
    "code": "f16",
    "name": "Ottery",
    "lat": -34.013376,
    "lon": 18.495
  },
  {
    "id": "13:f15",
    "code": "f15",
    "name": "Wetton",
    "lat": -34.001818,
    "lon": 18.501
  },
  {
    "id": "13:f1",
    "code": "f1",
    "name": "Salt Rivier",
    "lat": -33.926709,
    "lon": 18.465
  }
]
```

This endpoint retrieves rail stops by route.


### HTTP Request

`GET <BASEURL>/rail/routes/<routeId>/stops`


### URL Parameters

Parameter | Description
--------- | -----------
routeId | The ID of the route to retrieve stops for

## Get rail stop details

```javascript
GET: "http://proserver.gometro.co.za/api/v1/rail/stop/13:f12"
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
  "id": "13:f12",
  "name": "Athlone",
  "lat": -33.962688,
  "lon": 18.502,
  "code": "f12",
  "zoneId": "2",
  "locationType": 0,
  "wheelchairBoarding": 0,
  "vehicleType": -999,
  "vehicleTypeSet": false
}
```
This endpoint retrieves info for a specific stop in our rail data.



### HTTP Request

`GET <BASEURL>/rail/stop/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for

## Get rail line updates

```javascript
GET: "http://proserver.gometro.co.za/api/v1/rail/lineupdates"
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
  "routes_announcements": [
    {
      "event_id": "8733293",
      "create_date": "2017-03-03 06:23:54",
      "creator_id": "2191264",
      "type_id": "126",
      "message_id": "8733292",
      "receiver": "routes",
      "receiver_id": "90000160",
      "portal_id": "",
      "target_id": "90000160",
      "target2_id": "",
      "use_grouping": "0",
      "title": "Other Announcement",
      "message": "Trains cancelled due to sets out of service: Train no 0505 the 05:34 train from cape Town to Heathfield, Train no 0508 the 06:23 train from Heathfield to Cape Town, Train no 0513 the 06:21 train from Cape Town to Heathfield, Train no 0514 the 07:08 train from Heathfield to Cape Town, Train no 0519 the 07:10 train from Cape Town to Heathfield, Train no 0520 the 07:57 train from Heathfield to Cape Town.",
      "user_name": "Western Cape Metrorail"
    },
    {
      "event_id": "8733098",
      "create_date": "2017-03-03 05:41:01",
      "creator_id": "2191264",
      "type_id": "126",
      "message_id": "8733097",
      "receiver": "routes",
      "receiver_id": "90000160",
      "portal_id": "",
      "target_id": "90000160",
      "target2_id": "",
      "use_grouping": "0",
      "title": "Other Announcement",
      "message": "Trains cancelled due to sets out of service: Train no 0505 the 05:34 train from cape Town to Heathfield, Train no 0508 the 06:23 train from Heathfield to Cape Town, Train no 0513 the 06:21 train from Cape Town to Heathfield, Train no 0514 the 07:08 train from Heathfield to Cape Town, Train no 0519 the 07:10 train from Cape Town to Heathfield, Train no 0520 the 07:57 train from Heathfield to Cape Town.",
      "user_name": "Western Cape Metrorail"
    }
  ]
}
```
This endpoint retrieves lineupdates for Western Cape.



### HTTP Request

`GET <BASEURL>/rail/lineupdates/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for
