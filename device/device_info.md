# Device Info
**[HOME](../README.md)**

Device info.

**URL** : `/device/info/<device_id>`

**Method** : `GET`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

HEADER --> Authorization
```json
{
    "device_token": "[string]"
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

**Condition** : Error occured.

**Code** : `400 An error occured`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```