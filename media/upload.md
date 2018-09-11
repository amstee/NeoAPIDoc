# Upload media
**[HOME](../README.md)**

**URL** : `/media/upload/<media_id>`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Be owner of the media

**Description :**

The file must be found under the key "file".<br/>
A media accept only one file.

Informations to provide :

```
Headers : {
    "Authorization": "JsonWebToken",
    "content-type": "multipart/form-data"
}
```

```
Body : {"file": file content}
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

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```