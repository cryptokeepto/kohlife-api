# Group Contracts
support partner and admin only

## ListContractsPartner [/contracts]

### listContractsPartner [GET]

+ Request
    + Headers
            Content-Type: application/json
            x-access-token: <token>


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": [
                {
                    "contracts_id": 31,
                    "booking_code": "s-34468-t-1535535727125",
                    "contracts_travelers_amount": 3,
                    "contracts_price": 4200,
                    "contracts_status": "pending",
                    "contracts_created": "2018-08-29 16:42:39",
                    "contracts_updated": "-",
                    "schedules": {
                        "schedules_name": "Bangkok - Butterworth",
                        "schedules_travel_time": 1330,
                        "schedules_departure_time": 885,
                        "schedules_arrival_time": 775,
                        "schedules_departure_datetime": "Wed Jun 28 2017 07:45:00 GMT+0700 (Indochina Time)",
                        "schedules_arrival_datetime": "Thu Jun 29 2017 05:55:00 GMT+0700 (Indochina Time)",
                        "schedules_price": "1400.0",
                        "schedules_suggest_price": "1120.0",
                        "schedules_net_price": "1120.0"
                    },
                    "partner": {
                        "partner_username": "mickey",
                        "partner_email": "mickey@gmail.com",
                        "partner_role": "partner"
                    },
                    "contact": {
                        "contact_title": "mr",
                        "contact_firstname": "sittikiat",
                        "contact_lastname": "sujitranon",
                        "contact_birthday": "1995/03/09",
                        "contact_nationality": "th",
                        "contact_passport_number": "1102800050052",
                        "contact_phone": "0992828286",
                        "contact_email": "miikeoho@gmail.com"
                    },
                    "travelers": [
                        {
                            "travelers_id": 93,
                            "travelers_title": "mr",
                            "travelers_firstname": "sittikiat",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        },
                        {
                            "travelers_id": 94,
                            "travelers_title": "mr",
                            "travelers_firstname": "jack",
                            "travelers_lastname": "mar",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        },
                        {
                            "travelers_id": 95,
                            "travelers_title": "mr",
                            "travelers_firstname": "somchai",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        }
                    ]
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Authorization fail, You are not partner or admin but you are ${decoded.user.roles}."
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "No token provided"
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Invalid signature"
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List contract partner fail: ${error}"
        }

## ListContractsAdmin [/contracts]

### listContractsAdmin [GET]

+ Request
    + Headers
            Content-Type: application/json
            x-access-token: <token>

+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": [
                {
                    "contracts_id": 28,
                    "booking_code": "s-35608-t-1535018529329",
                    "contracts_travelers_amount": 3,
                    "contracts_price": 2430,
                    "contracts_status": "pending",
                    "contracts_created": "2018-08-23 17:05:34",
                    "contracts_updated": "-",
                    "schedules": {
                        "schedules_name": "Bangkok - Khao Lak",
                        "schedules_travel_time": 990,
                        "schedules_departure_time": 1170,
                        "schedules_arrival_time": 720,
                        "schedules_departure_datetime": "Wed Jun 28 2017 12:30:00 GMT+0700 (Indochina Time)",
                        "schedules_arrival_datetime": "Thu Jun 29 2017 05:00:00 GMT+0700 (Indochina Time)",
                        "schedules_price": "810.0",
                        "schedules_suggest_price": "748.0",
                        "schedules_net_price": "648.0"
                    },
                    "partner": {
                        "partner_username": "jame",
                        "partner_email": "jame@gmail.com",
                        "partner_role": "partner"
                    },
                    "contact": {
                        "contact_title": "mr",
                        "contact_firstname": "sittikiat",
                        "contact_lastname": "sujitranon",
                        "contact_birthday": "1995/03/09",
                        "contact_nationality": "th",
                        "contact_passport_number": "1102800050052",
                        "contact_phone": "0992828286",
                        "contact_email": "miikeoho@gmail.com"
                    },
                    "travelers": [
                        {
                            "travelers_id": 84,
                            "travelers_title": "mr",
                            "travelers_firstname": "somchai",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:05:34",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535018529329"
                        },
                        {
                            "travelers_id": 85,
                            "travelers_title": "mr",
                            "travelers_firstname": "sittikiat",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:05:34",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535018529329"
                        },
                        {
                            "travelers_id": 86,
                            "travelers_title": "mr",
                            "travelers_firstname": "jack",
                            "travelers_lastname": "mar",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:05:34",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535018529329"
                        }
                    ]
                },
                {
                    "contracts_id": 29,
                    "booking_code": "s-35608-t-1535019921965",
                    "contracts_travelers_amount": 3,
                    "contracts_price": 2430,
                    "contracts_status": "pending",
                    "contracts_created": "2018-08-23 17:25:54",
                    "contracts_updated": "-",
                    "schedules": {
                        "schedules_name": "Bangkok - Khao Lak",
                        "schedules_travel_time": 990,
                        "schedules_departure_time": 1170,
                        "schedules_arrival_time": 720,
                        "schedules_departure_datetime": "Wed Jun 28 2017 12:30:00 GMT+0700 (Indochina Time)",
                        "schedules_arrival_datetime": "Thu Jun 29 2017 05:00:00 GMT+0700 (Indochina Time)",
                        "schedules_price": "810.0",
                        "schedules_suggest_price": "748.0",
                        "schedules_net_price": "648.0"
                    },
                    "partner": {
                        "partner_username": "jame",
                        "partner_email": "jame@gmail.com",
                        "partner_role": "partner"
                    },
                    "contact": {
                        "contact_title": "mr",
                        "contact_firstname": "sittikiat",
                        "contact_lastname": "sujitranon",
                        "contact_birthday": "1995/03/09",
                        "contact_nationality": "th",
                        "contact_passport_number": "1102800050052",
                        "contact_phone": "0992828286",
                        "contact_email": "miikeoho@gmail.com"
                    },
                    "travelers": [
                        {
                            "travelers_id": 87,
                            "travelers_title": "mr",
                            "travelers_firstname": "sittikiat",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:25:54",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535019921965"
                        },
                        {
                            "travelers_id": 88,
                            "travelers_title": "mr",
                            "travelers_firstname": "somchai",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:25:54",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535019921965"
                        },
                        {
                            "travelers_id": 89,
                            "travelers_title": "mr",
                            "travelers_firstname": "jack",
                            "travelers_lastname": "mar",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:25:54",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535019921965"
                        }
                    ]
                },
                {
                    "contracts_id": 30,
                    "booking_code": "s-35608-t-1535020798723",
                    "contracts_travelers_amount": 3,
                    "contracts_price": 2430,
                    "contracts_status": "pending",
                    "contracts_created": "2018-08-23 17:40:22",
                    "contracts_updated": "-",
                    "schedules": {
                        "schedules_name": "Bangkok - Khao Lak",
                        "schedules_travel_time": 990,
                        "schedules_departure_time": 1170,
                        "schedules_arrival_time": 720,
                        "schedules_departure_datetime": "Wed Jun 28 2017 12:30:00 GMT+0700 (Indochina Time)",
                        "schedules_arrival_datetime": "Thu Jun 29 2017 05:00:00 GMT+0700 (Indochina Time)",
                        "schedules_price": "810.0",
                        "schedules_suggest_price": "748.0",
                        "schedules_net_price": "648.0"
                    },
                    "partner": {
                        "partner_username": "jame",
                        "partner_email": "jame@gmail.com",
                        "partner_role": "partner"
                    },
                    "contact": {
                        "contact_title": "mr",
                        "contact_firstname": "sittikiat",
                        "contact_lastname": "sujitranon",
                        "contact_birthday": "1995/03/09",
                        "contact_nationality": "th",
                        "contact_passport_number": "1102800050052",
                        "contact_phone": "0992828286",
                        "contact_email": "miikeoho@gmail.com"
                    },
                    "travelers": [
                        {
                            "travelers_id": 90,
                            "travelers_title": "mr",
                            "travelers_firstname": "jack",
                            "travelers_lastname": "mar",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:40:22",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535020798723"
                        },
                        {
                            "travelers_id": 91,
                            "travelers_title": "mr",
                            "travelers_firstname": "somchai",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:40:22",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535020798723"
                        },
                        {
                            "travelers_id": 92,
                            "travelers_title": "mr",
                            "travelers_firstname": "sittikiat",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-23 17:40:22",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-35608-t-1535020798723"
                        }
                    ]
                },
                {
                    "contracts_id": 31,
                    "booking_code": "s-34468-t-1535535727125",
                    "contracts_travelers_amount": 3,
                    "contracts_price": 4200,
                    "contracts_status": "pending",
                    "contracts_created": "2018-08-29 16:42:39",
                    "contracts_updated": "-",
                    "schedules": {
                        "schedules_name": "Bangkok - Butterworth",
                        "schedules_travel_time": 1330,
                        "schedules_departure_time": 885,
                        "schedules_arrival_time": 775,
                        "schedules_departure_datetime": "Wed Jun 28 2017 07:45:00 GMT+0700 (Indochina Time)",
                        "schedules_arrival_datetime": "Thu Jun 29 2017 05:55:00 GMT+0700 (Indochina Time)",
                        "schedules_price": "1400.0",
                        "schedules_suggest_price": "1120.0",
                        "schedules_net_price": "1120.0"
                    },
                    "partner": {
                        "partner_username": "mickey",
                        "partner_email": "mickey@gmail.com",
                        "partner_role": "partner"
                    },
                    "contact": {
                        "contact_title": "mr",
                        "contact_firstname": "sittikiat",
                        "contact_lastname": "sujitranon",
                        "contact_birthday": "1995/03/09",
                        "contact_nationality": "th",
                        "contact_passport_number": "1102800050052",
                        "contact_phone": "0992828286",
                        "contact_email": "miikeoho@gmail.com"
                    },
                    "travelers": [
                        {
                            "travelers_id": 93,
                            "travelers_title": "mr",
                            "travelers_firstname": "sittikiat",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        },
                        {
                            "travelers_id": 94,
                            "travelers_title": "mr",
                            "travelers_firstname": "jack",
                            "travelers_lastname": "mar",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        },
                        {
                            "travelers_id": 95,
                            "travelers_title": "mr",
                            "travelers_firstname": "somchai",
                            "travelers_lastname": "sujitranon",
                            "travelers_birthday": "1995/03/09",
                            "travelers_nationality": "th",
                            "travelers_created": "2018-08-29 16:42:39",
                            "travelers_updated": "-",
                            "travelers_passport_number": "1102800050052",
                            "booking_code": "s-34468-t-1535535727125"
                        }
                    ]
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Authorization fail, You are not partner or admin but you are ${decoded.user.roles}."
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "No token provided"
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Invalid signature"
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List contract admin fail: ${error}"
        }

## CreateContract [/contracts]

### CreateContract [POST]

+ Request
    + Headers
        Content-Type: application/json
        x-access-token: <token>

    + Body
        {
            "booking_code": "s-34468-t-1535535727125",
            "contracts_contact_title": "mr",
            "contracts_contact_firstname": "sittikiat",
            "contracts_contact_lastname": "sujitranon",
            "contracts_contact_birthday": "1995/03/09",
            "contracts_contact_nationality": "th",
            "contracts_contact_passport_number": "1102800050052",
            "contracts_contact_phone": "0992828286",
            "contracts_contact_email": "miikeoho@gmail.com",
            "travelers": [
                {
                    "travelers_title": "mr",
                    "travelers_firstname": "sittikiat",
                    "travelers_lastname": "sujitranon",
                    "travelers_birthday": "1995/03/09",
                    "travelers_nationality": "th",
                    "travelers_passport_number": "1102800050052"
                },
                {
                    "travelers_title": "mr",
                    "travelers_firstname": "somchai",
                    "travelers_lastname": "sujitranon",
                    "travelers_birthday": "1995/03/09",
                    "travelers_nationality": "th",
                    "travelers_passport_number": "1102800050052"
                },
                {
                    "travelers_title": "mr",
                    "travelers_firstname": "jack",
                    "travelers_lastname": "mar",
                    "travelers_birthday": "1995/03/09",
                    "travelers_nationality": "th",
                    "travelers_passport_number": "1102800050052"
                }
            ]
        }


+ Response 201
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": "Your booking code is ${BOOKING_CODE}"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Authorization fail, You are not partner but you are ${decoded.user.roles}."
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "No token provided"
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Invalid signature"
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Create contract fail: ${error}"
        }
