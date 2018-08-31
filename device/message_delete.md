# Delete message
**[HOME](../README.md)**

**URL** : `/device/message/delete`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "device_token": "[JWT token]",
    "message_id": "[integer]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "success": True
}
```

## Error Responses

**Condition** : Cannot delete this message.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```

### OR

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```