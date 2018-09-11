# Invite user to conversation
**[HOME](../README.md)**

**URL** : `/conversation/invite`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being member of the conversation


Informations to provide :

```json
{
    "token | device_token": "[string]",
    "email": "[string(120)]",
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

**Condition** : Missing necessary user right for this request.

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