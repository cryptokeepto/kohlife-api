# Group Locations

## List [/locations]

### List [GET]

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
                    "id": 457,
                    "name": "Koh Lanta (Koh Travel) Baanmaiphai Lanta"
                },
                {
                    "id": 42,
                    "name": "Satun"
                },
                {
                    "id": 3,
                    "name": "Bangkok"
                },
                {
                    "id": 9,
                    "name": "Hat Yai"
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List locations fail: ${error}"
        }

## FindByLocationId [/locations/:locationId]

### FindByLocationId [GET]


+ Parameters

    + locationId: `9` (required, number)

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
                "id": 9,
                "name": "Hat Yai",
                "type": "Location::Area",
                "address": null,
                "latitude": "7.0086472",
                "longitude": "100.4746879",
                "created_at": "2017-05-27T10:35:41.472Z",
                "updated_at": "2018-01-04T01:31:12.257Z",
                "parent_location_id": null,
                "map_detail_store": null,
                "seed_key": "hat_yai",
                "parent_pickup_id": null,
                "country": "tha"
            }
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Not have locationId in system. Please check again."
        }



