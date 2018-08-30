# Promote user in conversation
**[HOME](../README.md)**

**URL** : `/conversation/promote`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "conversation_id": "[integer]",
    "email": "[string(120)]"
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

**Condition** : Insufficient right for request.

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