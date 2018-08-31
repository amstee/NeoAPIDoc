# Update message
**[HOME](../README.md)**

**URL** : `/device/message/update`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : device


Informations to provide :

```json
{
    "device_token": "[JWT token]",
    "message_id": "[integer]",
    "text_content": "[string(8192)]"
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

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```