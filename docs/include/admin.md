# Group Admin

## List [/admin]

### List [GET]
+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": [
                {
                    "auth_id": 25,
                    "auth_username": "admin",
                    "auth_email": "admin@me.com",
                    "auth_roles": "admin",
                    "auth_created": "2018-08-09 16:50:45",
                    "auth_updated": "-",
                    "auth_partner_id": "-"
                },
                {
                    "auth_id": 39,
                    "auth_username": "admin2",
                    "auth_email": "admin2@gmail.com",
                    "auth_roles": "admin",
                    "auth_created": "2018-09-07 15:52:16",
                    "auth_updated": "-",
                    "auth_partner_id": "-"
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List admin fail: ${error}"
        }

## Create [/admin]

### Create [POST]

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
            "message": "Admin created."
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Create admin fail: ${error}"
        }
