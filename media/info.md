# Media info

**URL** : `/media/info`

**URL DEVICE** : `/device/media/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Access to the media

**Description :**
Get a media informations

Informations to provide :

```json
{
  "media_id": "[integer}"
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
        "filename": ["string"],
        "extension": "[string]",
        "identifier": "[string]",
        "uploaded": "[string]"
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