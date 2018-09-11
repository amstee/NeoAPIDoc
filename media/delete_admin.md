# Admin delete media
**[HOME](../README.md)**

**URL** : `/admin/media/delete`

**Method** : `DELETE`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin

**Description :**
Delete any media


Informations to provide :

```json
{
  "token": "[string]",
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