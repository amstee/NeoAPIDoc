# Media list

**URL** : `/media/list`

**URL DEVICE** : `/device/media/list`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device

**Description :**
List all medias for a given message

Informations to provide :

```json
{
  "message_id": "[integer]"
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