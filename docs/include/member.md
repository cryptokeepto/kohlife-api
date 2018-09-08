# Group Member

## List [/member]

### List [GET]
+ Response 200
    + Headers

        Content-Type: application/json


    + Body
        {
            "status": true,
            "message": [
                {
                    "auth_id": 18,
                    "auth_username": "jane",
                    "auth_email": "jane@gmail.com",
                    "auth_roles": "member",
                    "auth_created": "2018-07-28 13:52:12",
                    "auth_updated": "-",
                    "auth_partner_id": "9"
                },
                {
                    "auth_id": 21,
                    "auth_username": "dear",
                    "auth_email": "dear@gmail.com",
                    "auth_roles": "member",
                    "auth_created": "2018-08-05 23:10:18",
                    "auth_updated": "-",
                    "auth_partner_id": "9"
                }
            ]
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "List member fail: ${error}"
        }

## FindByMemberId [/member/:memberId]

### FindByMemberId [GET]

+ Parameters

    + memberId: `23` (required, number)


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": {
                "auth_id": 23,
                "auth_username": "jackson",
                "auth_email": "jackson@gmail.com",
                "auth_roles": "member",
                "auth_created": "2018-08-05 23:11:01",
                "auth_updated": "-",
                "auth_partner_id": "9"
            }
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Not have member in system. Please check again."
        }



## Create [/member]

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
            "message": "Member created."
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Create member fail: ${error}"
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Send Email fail: ${error}"
        }

## Update [/member/:memberId]

### Update [PUT]

+ Parameters

    + memberId: `23` (required, number)
    + auth_password: `new123456` (required, string)


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": "Member updated."
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Update member fail: ${error}"
        }

## Delete [/member/:memberId]

### Delete [DELETE]

+ Parameters

    + memberId: `23` (required, number)


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": "Member deleted."
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Delete member fail: ${error}"
        }

