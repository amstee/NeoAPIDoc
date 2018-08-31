# Message informations
**[HOME](../README.md)**

**URL** : `/device/message/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "device_token": "[JWT token]",
    "message_id": "[integer]"
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
        "device": {
            "id": "[integer]",
            "name": "[string(120)]",
            "created": "[string(datetime)]",
            "updated": "[string(datetime)]",
            "circle_id": "[integer]",
            "activated": "[boolean]",
            "username": "[string(120)]",
            "is_online": "[boolean]"
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
    "success": True
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