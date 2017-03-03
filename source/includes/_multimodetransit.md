# Multimodal Routing

The GoMetro Routing API responds to journey planning requests with itineraries in a JSON or XML representation. Plan multi-modal walking, wheelchair, bicycle and transit trips. Take travel time, road type, safety, and elevation into account, and allow users to customize the weighting of these three factors:

Imports data from GTFS, OpenStreetMap, and digital elevation models – we are a completely open data warehouse and can connect any data type to any other data type in the transport operating environment.
Supports one-to-many and many-to-many searches for planning, alternatives analysis, and accessibility research purposes.
Typically provides multiple itineraries in a fraction of a second even in large metropolitan networks – our response times are very efficient.

## Get multimodal routing

```javascript
GET "http://proserver.gometro.co.za/api/v1/trips/Artscape%20Theatre%20Centre/10%20church%20street,%20durbanville/2017-03-03/10:00/RAIL,BUS,FERRY,TRAM,GONDOLA,WALK"
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
  "date": 1488528000000,
  "from": {
    "name": "BUS 807",
    "lon": 18.430152,
    "lat": -33.920658,
    "orig": "",
    "vertexType": "NORMAL"
  },
  "to": {
    "name": "BUS 3943",
    "lon": 18.648731,
    "lat": -33.834074,
    "orig": "",
    "vertexType": "NORMAL"
  },
  "itineraries": [
    {
      "duration": 3558,
      "startTime": 1488528190000,
      "endTime": 1488531748000,
      "walkTime": 0,
      "transitTime": 3304,
      "waitingTime": 254,
      "walkDistance": 0,
      "walkLimitExceeded": false,
      "elevationLost": 0,
      "elevationGained": 0,
      "transfers": 1,
      "legs": [
        {
          "startTime": 1488528190000,
          "endTime": 1488531467000,
          "departureDelay": 0,
          "arrivalDelay": 0,
          "realTime": false,
          "distance": 25190.738939604,
          "pathway": false,
          "mode": "BUS",
          "route": "015_A",
          "agencyName": "Golden Arrow",
          "agencyUrl": "http://www.cccta.org",
          "agencyTimeZoneOffset": 7200000,
          "routeType": 3,
          "routeId": "6:713",
          "interlineWithPreviousLeg": false,
          "tripShortName": "Golden Arrow Trips",
          "headsign": "Bus Stop54194",
          "agencyId": "6000",
          "tripId": "6:713",
          "serviceDate": "20170303",
          "from": {
            "name": "BUS 807",
            "stopId": "6:S807",
            "stopCode": "2435",
            "lon": 18.430152,
            "lat": -33.920658,
            "departure": 1488528190000,
            "orig": "",
            "stopIndex": 2,
            "stopSequence": 54184,
            "vertexType": "TRANSIT"
          },
          "to": {
            "name": "BUS 3938",
            "stopId": "6:S3938",
            "stopCode": "720",
            "lon": 18.647079,
            "lat": -33.832471,
            "arrival": 1488531467000,
            "departure": 1488531721000,
            "stopIndex": 13,
            "stopSequence": 54195,
            "vertexType": "TRANSIT"
          },
          "legGeometry": {
            "points": "pc`nE_snoB\\g@xH_JiS}RtHuOzB{KBye@n@yIA{Hy@wIi@{_@NaRoCmh@mPclAcEkNMgDfAmOsBkSmDiQ_IuUcGgLmF}HesC}`DkDwFmDcJeCwNe@{Nd@_KbAsHjCwJvS{f@`BuFhBqLb@wMa@mKke@kaFYuJRiHvAcKlCgIhR_d@vB_MZ{HqGkkC]cH_Fw[_C_HiIo@_HaAyj@}H_Cy@kBqAiFuDmZkEoJuAiIkAkRoCeY_KqHgBoKwAuw@mE_DcAgGaFaDgCgCaBsEuCgFgBSGiI_BKAmEUaAGkRfCwG|G",
            "length": 74
          },
          "routeShortName": "015_A",
          "routeLongName": "CITYDURBANVILLEN1 FREEWAY",
          "rentedBike": false,
          "transitLeg": true,
          "duration": 3277,
          "intermediateStops": [
            {
              "name": "BUS 3981",
              "stopId": "6:S3981",
              "stopCode": "4492",
              "lon": 18.634704,
              "lat": -33.883158,
              "arrival": 1488530755000,
              "departure": 1488530755000,
              "stopIndex": 3,
              "stopSequence": 54185,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3921",
              "stopId": "6:S3921",
              "stopCode": "4493",
              "lon": 18.637036,
              "lat": -33.874942,
              "arrival": 1488530867000,
              "departure": 1488530867000,
              "stopIndex": 4,
              "stopSequence": 54186,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3929",
              "stopId": "6:S3929",
              "stopCode": "192",
              "lon": 18.638968,
              "lat": -33.869408,
              "arrival": 1488530951000,
              "departure": 1488530951000,
              "stopIndex": 5,
              "stopSequence": 54187,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3927",
              "stopId": "6:S3927",
              "stopCode": "209",
              "lon": 18.639688,
              "lat": -33.867614,
              "arrival": 1488530974000,
              "departure": 1488530974000,
              "stopIndex": 6,
              "stopSequence": 54188,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3926",
              "stopId": "6:S3926",
              "stopCode": "2207",
              "lon": 18.639788,
              "lat": -33.865918,
              "arrival": 1488530999000,
              "departure": 1488530999000,
              "stopIndex": 7,
              "stopSequence": 54189,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3950",
              "stopId": "6:S3950",
              "stopCode": "200",
              "lon": 18.645823,
              "lat": -33.843843,
              "arrival": 1488531299000,
              "departure": 1488531299000,
              "stopIndex": 8,
              "stopSequence": 54190,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3953",
              "stopId": "6:S3953",
              "stopCode": "2205",
              "lon": 18.647169,
              "lat": -33.842452,
              "arrival": 1488531324000,
              "departure": 1488531324000,
              "stopIndex": 9,
              "stopSequence": 54191,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3947",
              "stopId": "6:S3947",
              "stopCode": "2204",
              "lon": 18.648381,
              "lat": -33.840209,
              "arrival": 1488531356000,
              "departure": 1488531356000,
              "stopIndex": 10,
              "stopSequence": 54192,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3946",
              "stopId": "6:S3946",
              "stopCode": "201",
              "lon": 18.648798,
              "lat": -33.838438,
              "arrival": 1488531382000,
              "departure": 1488531382000,
              "stopIndex": 11,
              "stopSequence": 54193,
              "vertexType": "TRANSIT"
            },
            {
              "name": "BUS 3945",
              "stopId": "6:S3945",
              "stopCode": "2203",
              "lon": 18.648904,
              "lat": -33.837362,
              "arrival": 1488531399000,
              "departure": 1488531399000,
              "stopIndex": 12,
              "stopSequence": 54194,
              "vertexType": "TRANSIT"
            }
          ],
          "steps": []
        }
}
}
}
```

Plan multi-modal walking, wheelchair, bicycle and transit trips. 


### HTTP Request

`GET <BASEURL>/trips/<from>/<to>/<date>/<time>/<modes>`

### Query Parameters

Parameter | Description
--------- | -----------
from | Starting Point
to | Destination 
date | The date
time | The time
modes | Mode options - RAIL,BUS,FERRY,TRAM,GONDOLA,WALK

