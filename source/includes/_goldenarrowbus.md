# Golden Arrow Bus

## Get Golden Arrow bus routes

```javascript
GET: "pro.gometro.co.za/api/v1/ga/routes"
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

This endpoint retrieves Golden Arrow bus routes.


### HTTP Request

`GET <BASEURL>/ga/routes/`

### URL Parameters

There are no query parameters for this endpoint.

## Get Golden Arrow bus stops by route

```javascript
GET: "pro.gometro.co.za/api/v1/ga/routes/234544/stops"
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

This endpoint retrieves Golden Arrow bus stops by route.


### HTTP Request

`GET <BASEURL>/ga/routes/<routeId>/stops`


### URL Parameters

Parameter | Description
--------- | -----------
routeId | The ID of the route to retrieve stops for

## Get Golden Arrow bus stop details

```javascript
GET: "pro.gometro.co.za/api/v1/ga/stops/1234"
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
This endpoint retrieves info for a specific Golden Arrow bus stop.



### HTTP Request

`GET <BASEURL>/ga/stop/<stopId>`

### URL Parameters

Parameter | Description
--------- | -----------
stopId | The ID of the stop to retrieve data for
