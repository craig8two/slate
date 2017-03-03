# Accessibility Score

Quantify all public transport available within 800m of a single point including Minibus Taxi Routes.

For any point in Cities that we support, GoMetro is able to provide a complete inventory of public transport routes and stops within 800m of a given point. This includes train, BRT, bus and minibus taxi routes that are continuously collected and updated by commuters themselves. Our Access Score is a benchmark of transport availability and can be used to compare different points around the world as to transport availability.

Our Accessibility Score currently is only supported in Cape Town. Other cities to follow shortly.

## Get accessibility

```javascript
GET "http://proserver.gometro.co.za/api/v1/accessibility/-33.903490/18.420468/150/"
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
{
  "stops": [
    {
      "id": "10:19",
      "name": "Breakwater",
      "lat": -33.9030545,
      "lon": 18.4192915,
      "dist": 118,
      "modes": "BRT",
      "routeCount": 2
    }
  ],
  "stopCount": 1,
  "routeCount": 2,
  "longestRoutes": [
    {
      "id": "10:104",
      "shortName": "104",
      "longName": "Sea Point - Waterfront - Civic Centre",
      "mode": "BRT",
      "color": "FFDD00",
      "agencyName": "MyCiti",
      "routerId": "South_Africa",
      "distance": 10.23
    },
    {
      "id": "10:P104",
      "shortName": "104",
      "longName": "Sea Point - Waterfront - Civic Centre",
      "mode": "BRT",
      "color": "FFDD00",
      "agencyName": "MyCiti",
      "routerId": "South_Africa",
      "distance": 9.97
    }
  ],
  "routesDistance": 20.2,
  "accessibilityScore": 0
}
```

This endpoint retrieves the accessibility score for an area

### HTTP Request

`GET <BASEURL>/accessibility/<lat>/<lng>/<rad>/`

### Query Parameters

Parameter | Description
--------- | -----------
lat | Latitude
lng | Longitude 
rad | Radius

