# Media retrieve
**[HOME](../README.md)**

**URL** : `/media/retrieve`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Access to the media

**Description :**
Retrieve a given media

Informations to provide in body :

```json
{
  "token | device_token": "[string]",
  "media_id": "[integer]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content**

```
Media content
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