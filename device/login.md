# Login Device
**[HOME](../README.md)**

Log in device (receiving JWT token).

**URL** : `/device/authenticate`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "device_username": "[string]",
    "device_password": "[string]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "token": "[JWT token]",
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```