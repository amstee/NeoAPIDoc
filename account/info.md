# Create User's Account
**[HOME](../README.md)**

Retrieving account informations.

**URL** : `/account/info`

**Method** : `POST`

**Authentication required** : YES (token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content": {
        "birthday": "[string(datetime)]",
        "circles": [
            {
                "circle": {
                    "created": "[string(datetime)]",
                    "device": "[integer]",
                    "id": "[integer]",
                    "name": "[string(120)]",
                    "updated": "[string(datetime)]"
                },
                "created": "[string(datetime)]",
                "id": "[integer]",
                "privilege": "[string(10)]",
                "updated": "[string(datetime)]",
                "user": "[integer]"
            }
        ],
        "conversations": [
            {
                "circle_id": "[integer]",
                "conversation_id": "[integer]",
                "created": "[string(datetime)]",
                "id": "[integer]",
                "privilege": "[string(10)]",
                "updated": "[string(datetime)]",
                "user_id": "[integer]"
            }
        ],
        "created": "[string(datetime)]",
        "email": "[string(120)]",
        "facebook": "[boolean]",
        "first_name": "[string(50)]",
        "hangout": "[boolean]",
        "id": "[integer]",
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
        "isOnline": "[boolean]",
        "last_name": "[string(50)]",
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
        "type": "[string(10)]",
        "updated": "[string(datetime)]"
    },
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```