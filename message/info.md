# Message informations
**[HOME](../README.md)**

**URL** : `/message/info/<message_id>`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Have access to the message

Informations to provide in header :

```json
{
    "Authorization": "[string]"
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
        "sent": "[boolean]",
        "read": "[boolean]",
        "content": "[string(8192)]",
        "link": {
                    "id": "[integer]",
                    "created": "[datetime]",
                    "updated": "[datetime]",
                    "privilege": "[string(10)]",
                    "user_id": "[integer]",
                    "conversation_id": "[integer]",
                    "circle_id": "[integer]"
        },
        "medias": [
            {
                "id": "[integer]",
                "upload_time": "[string(datetime)]",
                "message": {
                    "id": "[integer]",
                    "link_id": "[integer]",
                    "sent": "[string(datetime)]",
                    "read": "[string(datetime)]",
                    "content": "[string(8192)]",
                    "medias": "[integer]"
                },
                "media": {
                    "id": "[integer]",
                    "filename": "[string(120)]",
                    "extension": "[sting(10)]",
                    "identifier": "[string(10)]",
                    "uploaded": "[string(boolean)]"
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
    "success": false
}
```