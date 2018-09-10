# Group Transportations

## RoutesMatch [/transportations/routesMatch]

### RoutesMatch [GET]
+ Request
    + Headers
        Content-Type: application/json

+ Response 200
    + Headers

        Content-Type: application/json


    + Body
       {
            "status": true,
            "message": {
                "1": [
                    3,
                    9,
                    12,
                    13,
                    18,
                    20,
                    21,
                    23,
                    24,
                    26,
                    33,
                    38,
                    40,
                    47
                ],
                "2": [
                    6
                ]
            }
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List routesMatch fail: ${error}"
        }

## FromToDate [/transportations/:fromId/:toId/:date]

### FromToDate [GET]

+ Parameters

    + fromId: `3` (required, number)
    + toId: `5` (required, number)
    + date: `2017-06-28` (required, string)

+ Request
    + Headers
        Content-Type: application/json


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": [
                {
                    "booking_code": "s-34468-t-1536303143171",
                    "transport_schedules_id": 34468,
                    "status": "scheduled",
                    "route_name": "Bangkok - Butterworth",
                    "departure_datetime": "Wed Jun 28 2017 07:45:00 GMT+0700 (Indochina Time)",
                    "arrival_datetime": "Thu Jun 29 2017 05:55:00 GMT+0700 (Indochina Time)",
                    "operator_name": "songserm",
                    "operator_image": "http://res.cloudinary.com/chinnatip-store/image/upload/v1511087029/logo_songserm_llf6ar.png",
                    "departure_terminal": {
                        "id": 3,
                        "name": "Bangkok",
                        "type": "Location::Area",
                        "address": null,
                        "latitude": "13.7563309",
                        "longitude": "100.5017651",
                        "created_at": "2017-05-27T10:35:41.440Z",
                        "updated_at": "2018-01-04T01:31:12.127Z",
                        "parent_location_id": null,
                        "map_detail_store": null,
                        "seed_key": "bangkok",
                        "parent_pickup_id": null,
                        "country": "tha"
                    },
                    "arrival_terminal": {
                        "id": 5,
                        "name": "Butterworth",
                        "type": "Location::Area",
                        "address": null,
                        "latitude": "5.4380309",
                        "longitude": "100.388192",
                        "created_at": "2017-05-27T10:35:41.452Z",
                        "updated_at": "2018-01-04T01:31:12.166Z",
                        "parent_location_id": null,
                        "map_detail_store": null,
                        "seed_key": "butterworth",
                        "parent_pickup_id": null,
                        "country": "mal"
                    },
                    "duration": "22:10",
                    "net_price": "1120.0",
                    "suggest_price": "1120.0",
                    "price": "1400.0"
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "fromToDate fail: ${error}"
        }



