# Group Authentication

## Register [/register]

### Register [POST]

+ Parameters

    + auth_username: `john` (required, string)
    + auth_email: `john@domain.com` (required, string)
    + auth_password: `123456` (required, string)


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

+ Parameters

    + auth_email: `john@domain.com` (required, string)
    + auth_password: `123456` (required, string)


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
