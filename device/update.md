# Update Device
**[HOME](../README.md)**

Device update.

**URL** : `/device/update`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "device_token OR token": "[string]",
    "device_id": "[int]"
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