# Remove device from conversation
**[HOME](../README.md)**

**URL** : `/conversation/device/remove`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "conversation_id": "[integer]"
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