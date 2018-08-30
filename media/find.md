# Find media

**URL** : `/media/find`

**URL DEVICE** : `/device/media/find`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device

**Description :**
Find a media

If the filter is not specified, the research will be done on the medias linked to the user / device.


Informations to provide :

```json
{
  "purpose": "[string]",
  "circle_id | device_id | user_id": "[integer] (optional)"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "media_list": [
    {
        "id": "[integer]",
        "filename": ["string"],
        "extension": "[string]",
        "identifier": "[string]",
        "uploaded": "[string]"
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