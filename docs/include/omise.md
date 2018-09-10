# Group Omise

## omiseBooking [/omiseBooking]

### omiseBooking [POST]

+ Request
    + Headers
        Content-Type: application/json
        x-access-token: <token>

    + Body
        {
            "card_name": "sittikiat",
            "card_number": "5454545454545454",
            "card_city": "Bangkok",
            "card_postal_code": "10150",
            "card_expiration_month": "8",
            "card_expiration_year": "2022",
            "card_security_code": "154",
            "charges_amount": "1566.0",
            "booking_id": "3"
        }


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": "Paymented"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Payment fail: ${error}"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Create card fail: ${error}"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Charge card fail: ${error}"
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
