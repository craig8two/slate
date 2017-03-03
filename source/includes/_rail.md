# Metrorail


## Get Metrorail routes by region

```javascript
GET "http://pro.gometro.co.za:9090/otp/routers/prasa-gauteng/index/routes/"
```

```ruby
Ruby examples coming soon
```

```python
Python examples coming soon
```

```shell
Shell examples coming soon
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "1:25230",
    "shortName": "Mabopane-Pretoria",
    "longName": "Mabopane-Pretoria",
    "mode": "RAIL",
    "color": "00BAF1",
    "agencyName": "Metro rail Gauteng"
  },
  {
    "id": "1:25231",
    "shortName": "Pienaarspoort-Pretoria",
    "longName": "Pienaarspoort-Pretoria",
    "mode": "RAIL",
    "color": "0072BC",
    "agencyName": "Metro rail Gauteng"
  }
]
```

This endpoint retrieves our Metrorail routes data.

### HTTP Request

`GET <BASEURL>/otp/routers/<REGION>/index/routes/`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
REGION | false | You need to specify a region, see below for available options

### Region options:

Region | Description
---------- | -------
prasa-westerncape | Metrorail Western Cape
prasa-gauteng | Metrorail Gauteng


## Get line announcements by route

```javascript
GET: "http://gometroapp.com/?transit_api+announcements+routes+90000128+2"
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
      "event_id": "8730289",
      "create_date": "2017-03-02 15:31:03",
      "creator_id": "2191264",
      "type_id": "126",
      "message_id": "8730288",
      "receiver": "routes",
      "receiver_id": "90000160",
      "portal_id": "",
      "target_id": "90000160",
      "target2_id": "",
      "use_grouping": "0",
      "title": "Minor Delays",
      "message": "Cancellations due to sets out of service and maintenance: Train no 0557 the 16:22 train from Cape Town to Heathfield, train no 0558 the 17:08 train from Heathfield to Cape Town, train no 0571 the 17:56 train from Cape Town to Heathfield and train no 0572 the 18:41 train from Heathfield to Cape Town. Trains on the Cape Flats line are delayed between 15-20 minutes due to ongoing technical problem at Pinelands.",
      "user_name": "Western Cape Metrorail"
    },
    {
      "event_id": "8730247",
      "create_date": "2017-03-02 15:21:05",
      "creator_id": "2191264",
      "type_id": "126",
      "message_id": "8730246",
      "receiver": "routes",
      "receiver_id": "90000160",
      "portal_id": "",
      "target_id": "90000160",
      "target2_id": "",
      "use_grouping": "0",
      "title": "Other Announcement",
      "message": "Cancellations due to sets out of service and maintenance: Train no 0557 the 16:22 train from Cape Town to Heathfield, train no 0558 the 17:08 train from Heathfield to Cape Town, train no 0571 the 17:56 train from Cape Town to Heathfield and train no 0572 the 18:41 train from Heathfield to Cape Town.",
      "user_name": "Western Cape Metrorail"
    }
  ]
}
```

This endpoint retrieves line announcements by route


### HTTP Request

`GET <BASEURL>/?transit_api+announcements+routes+<ID>+<COUNT>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the route to retrieve
COUNT | How many entries you want returned

### Available route ID's

Parameter | Description
--------- | -----------
90000160 | 
90000164 | 
90000163 | 
90000175 | 
90000128 | 