# Add / Remove device to conversation
**[HOME](../README.md)**

The device is able to call this route but only to remove himself from the conversation

**URL** : `/conversation/device/set`

**Method** : `PUT`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being member of the conversation


Informations to provide :

```json
{
    "token | device_token": "[string]",
    "conversation_id": "[integer]"
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

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```