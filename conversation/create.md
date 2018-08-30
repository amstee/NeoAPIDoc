# Create conversation
**[HOME](../README.md)**

**URL** : `/admin/conversation/create`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin


Informations to provide :

```json
{
    "token": "[JWT token]",
    "conversation_name": "[string(120)]",
    "circle_id": "[integer]"
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