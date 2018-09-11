# Media list
**[HOME](../README.md)**

**URL** : `/message/media/list/<message_id>`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Access to the message

**Description :**
List all medias for a given message

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
    "content": [ 
    {
        "id": "[integer]",
        "message": {
            "id": "[integer]",
            "sent": "[boolean]",
            "read": "[boolean]",
            "content": "[string(8192)]"        
        },
        "media": {
            "id": "[integer]",
            "filename": ["string"],
            "extension": "[string]",
            "identifier": "[string]",
            "uploaded": "[string]"
        },
        "upload_time": "[date]"
    }
    ],
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