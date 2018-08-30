# Delete media
**[HOME](../README.md)**

**URL** : `/media/delete`

**URL DEVICE** : `/device/media/delete`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Being owner of the media

**Description :**
Delete a media


Informations to provide :

```json
{
  "media_id": "[integer]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
   "success": true
}
```

## Error Responses

**Condition** : An error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```