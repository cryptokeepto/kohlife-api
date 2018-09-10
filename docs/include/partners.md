# Group Partners

## List [/partners]

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
                    "auth_id": 9,
                    "auth_username": "mickey",
                    "auth_email": "mickey@gmail.com",
                    "auth_roles": "partner",
                    "auth_created": "2018-07-26 21:49:30",
                    "auth_updated": "-",
                    "auth_partner_id": "-"
                },
                {
                    "auth_id": 27,
                    "auth_username": "jame",
                    "auth_email": "jame@gmail.com",
                    "auth_roles": "partner",
                    "auth_created": "2018-08-15 16:58:50",
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
            "message": "List partners fail: ${error}"
        }

## FindByPartnerId [/partners/:partnerId]

### FindByPartnerId [GET]

+ Parameters

    + partnerId: `9` (required, number)

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
                "auth_id": 9,
                "auth_username": "mickey",
                "auth_email": "mickey@gmail.com",
                "auth_roles": "partner",
                "auth_created": "2018-07-26 21:49:30",
                "auth_updated": "-",
                "auth_partner_id": "-"
            }
        }

+ Response 500

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Not have partner in system. Please check again."
        }



## Create [/partners]

### Create [POST]

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
            "message": "Partner created."
        }

+ Response 409

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Create partner fail: ${error}"
        }

## Update [/partners/:partnerId]

### Update [PUT]

+ Parameters

    + partnerId: `9` (required, number)

+ Request
    + Headers
        Content-Type: application/json

    + Body
        {
            "auth_password": "new123456"
        }


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": "Partner updated."
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Update partner fail: ${error}"
        }

## Delete [/partners/:partnerId]

### Delete [DELETE]

+ Parameters

    + partnerId: `9` (required, number)

+ Request
    + Headers
        Content-Type: application/json


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": "Partner deleted."
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "Delete partner fail: ${error}"
        }


## CreateMemberByPartner [/partners/:partnerId/member]

### CreateMemberByPartner [POST]


+ Parameters
    + partnerId: `9` (required, number)

+ Request
    + Headers
        Content-Type: application/json
        x-access-token: <token>

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
            "message": "Member by partner created."
        }

+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "You are not partner but you are ${decoded.user.roles}."
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
            "message": "Create member by partner fail: ${error}"
        }

## ListMemberOfPartner [/partners/:partnerId/member]

### ListMemberOfPartner [GET]


+ Parameters
    + partnerId: `9` (required, number)

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
                },
                {
                    "auth_id": 22,
                    "auth_username": "mike",
                    "auth_email": "mike@gmail.com",
                    "auth_roles": "member",
                    "auth_created": "2018-08-05 23:10:34",
                    "auth_updated": "-",
                    "auth_partner_id": "9"
                },
                {
                    "auth_id": 24,
                    "auth_username": "jackson",
                    "auth_email": "jackson@gmail.com",
                    "auth_roles": "member",
                    "auth_created": "2018-08-05 23:11:01",
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
            "message": "You are not partner but you are ${decoded.user.roles}."
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
            "message": "List member by partner fail: ${error}"
        }

## FindByMemberOfPartner [/partners/:partnerId/member/:memberIdOfPartner]

### FindByMemberOfPartner [GET]

+ Parameters
    + memberIdOfPartner: `18` (required, number)
    + partnerId: `9` (required, number)

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
            "message": {
                "auth_id": 18,
                "auth_username": "jane",
                "auth_email": "jane@gmail.com",
                "auth_roles": "member",
                "auth_created": "2018-07-28 13:52:12",
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
            "message": "Not have memberIdOfPartner in system. Please check again."
        }



## UpdateMemberIdOfPartner [/partners/:partnerId/member/:memberIdOfPartner]

### UpdateMemberIdOfPartner [PUT]

+ Parameters

    + memberIdOfPartner: `18` (required, number)
    + partnerId: `9` (required, number)

+ Request
    + Headers
        Content-Type: application/json
        x-access-token: <token>

    + Body
        {
            "auth_roles": "partner"
        }


+ Response 200
    + Headers

        Content-Type: application/json


    + Body
         {
            "status": true,
            "message": "Member by partner updated."
        }


+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "You are not partner but you are ${decoded.user.roles}."
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
            "message": "Update member by partner fail: ${error}"
        }


## DeleteMemberIdOfPartner [/partners/:partnerId/member/:memberIdOfPartner]

### DeleteMemberIdOfPartner [DELETE]

+ Parameters

    + memberIdOfPartner: `18` (required, number)
    + partnerId: `9` (required, number)

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
            "message": "Member by partner deleted."
        }


+ Response 400

    + Headers

        Content-Type: application/json

    + Body
        {
            "status": false,
            "message": "You are not partner but you are ${decoded.user.roles}."
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
            "message": "Delete member by partner fail: ${error}"
        }
