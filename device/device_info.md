# Device Info
**[HOME](../README.md)**

Device info.

**URL** : `/device/info/<device_id>`

**URL POST** : `/device/info`

**Method** : `GET` OR `POST`

**Authentication required** : YES

**Permissions required** : USER or DEVICE


Informations to provide for GET :

HEADER --> Authorization
```json
{
    "device_token | token": "[string]"
}
```

```json
{
    "token": "[JWT token]",
    "(Only for users) device_id": "[int]",
    "success": true
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "success": true,
    "content": {
        "id": "[integer]",
        "name": "[string]",
        "created": "[date]",
        "updated": "[date]",
        "activated": "[boolean]",
        "username": "[string]",
        "circle": "[list]",
        "messages": "[list]",
        "medias": "[list]",
        "is_online": "boolean"
    }
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `400 An error occured`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```