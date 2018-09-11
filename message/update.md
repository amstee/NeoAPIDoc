# Update message
**[HOME](../README.md)**

**URL** : `/message/update`

**Method** : `PUT`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being owner of the message


Informations to provide :

```json
{
    "token | device_token": "[string]",
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