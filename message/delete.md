# Delete message
**[HOME](../README.md)**

Delete a given message.

**URL** : `/message/delete`

**Method** : `DELETE`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being owner of the message


Informations to provide :

```json
{
    "token | device_token": "[string]",
    "message_id": "[integer]"
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

**Condition** : Cannot delete this message.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```

### OR

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```