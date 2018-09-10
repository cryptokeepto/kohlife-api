# Group Tickets

## Create [/tickets]

### Create [POST]

+ Request
    + Headers
        Content-Type: application/json
        x-access-token: <token>

    + Body
        {
            "booking_code": "s-34468-t-1535535727125"
        }

+ Response 201
    + Headers

        Content-Type: application/json


    + Body
       {
            "status": true,
            "message": "ticket created"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Authorization fail. you are ${decoded.user.roles}."
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
            "message": "Create ticket fail: ${error}"
        }

## Download [/tickets?booking_code=<booking_code>]

### Download [GET]

+ Parameters

    + booking_code: `s-34468-t-1535535727125` (required, string)

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
            "message": "created success"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Can not generate ticket"
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Authorization fail. you are ${decoded.user.roles}."
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
            "message": "Create ticket fail: ${error}"
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Send Email fail: ${error}"
        }
