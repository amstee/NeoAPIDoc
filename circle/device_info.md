# Circle informations (as Device)
**[HOME](../README.md)**

**URL** : `/device/circle/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "device_token": "[JWT token]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content": {
        "id": "[integer]",
        "name": "[string(120)]",
        "updated": "[string(datetime)]",
        "conversations": [
            {
                "circle_id": "[integer]",
                "created": "[string(datetime)]",
                "device_access": "[boolean]",
                "id": "[integer]",
                "name": "[string(120)]",
                "updated": "[string(datetime)]"
            }
        ],
        "created": "[string(datetime)]",
        "device": {
            "activated": "[boolean]",
            "circle_id": "[integer]",
            "created": "[string(datetime)]",
            "id": "[integer]",
            "is_online": "[boolean]",
            "name": "[string(120)]",
            "updated": "[string(datetime)]",
            "username": "[string(120)]"
        },
        "invites": [
            {
                "id": "[integer]",
                "updated": "[string(datetime)]",
                "created": "[string(datetime)]",
                "user": "[integer]",
                "circle": {
                        "id": "[integer]",
                        "circle_id": "[integer]",
                        "user_id": "[integer]",
                        "created": "[string(datetime)]",
                        "updated": "[string(datetime)]"
                }
            }
        ],
        "medias": [
            {
                "id": "[integer]",
                "user": {
                    "id": "[integer]",
                    "email": "[string(120)]",
                    "first_name": "[string(50)]",
                    "last_name": "[string(50)]",
                    "birthday": "[string(datetime)]",
                    "created": "[string(datetime)]",
                    "updated": "[string(datetime)]",
                    "isOnline": "[boolean]",
                    "type": "[string(10)]",
                },
                "media": {
                    "id": "[integer]",
                    "filename": "[string(120)]",
                    "extension": "[string(10)]",
                    "identifier": "[string(10)]",
                    "uploaded": "[string]"
                },
                "upload_time": "[string(datetime)]",
                "purpose": "[string(16)]"
            }

        ],
        "users": [
            {
                "circle": 1,
                "created": "Thu, 30 Aug 2018 02:46:45 GMT",
                "id": 1,
                "privilege": "ADMIN",
                "updated": "Thu, 30 Aug 2018 02:46:45 GMT",
                "user": {
                    "birthday": "Thu, 05 Sep 2019 00:00:00 GMT",
                    "created": "Thu, 30 Aug 2018 02:46:45 GMT",
                    "email": "user1.beta@test.com",
                    "first_name": "user1",
                    "id": 2,
                    "isOnline": false,
                    "last_name": "beta",
                    "type": "DEFAULT",
                    "updated": "Thu, 30 Aug 2018 02:46:45 GMT"
                }
            }
        ]
    },
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```