# Modify Device Password
**[HOME](../README.md)**


**URL** : `/device/modify/password`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "device_username": "[string]",
    "previous_password": "[string]",
    "new_password": "[string]"
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