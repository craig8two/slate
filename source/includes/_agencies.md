# Agencies


## Get all agencies

```javascript
GET "pro.gometro.co.za/api/v1/agencies/"
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

This endpoint retrieves all transport agencies in our database.

### HTTP Request

`GET <BASEURL>/agencies/`

### Query Parameters

There are no query parameters for this endpoint.

