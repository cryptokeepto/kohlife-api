# Group Authentication

## Register [/register]

### Register [POST]

+ Request
    + Headers
        Content-Type: application/json
    + Body
        {
            "auth_username": "john",
            "auth_email": "john@domain.com",
            "auth_password": "123456"
        }

+ Response 201
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": "Signup is success."
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Signup fail: ${error}"
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Send Email fail: ${error}"
        }

## Login [/login]

### Login [POST]

+ Request
    + Headers
        Content-Type: application/json
    + Body
        {
            "auth_email": "john@domain.com",
            "auth_password": "123456"
        }

+ Response 200
    + Headers

        Content-Type: application/json

    + Body
        {
            "status": true,
            "message": <token>
        }

+ Response 401

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Email or password invalid."
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Login fail: ${error}"
        }
