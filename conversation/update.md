# Update conversation informations
**[HOME](../README.md)**

**URL** : `/conversation/update`

**Method** : `PUT`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being member of the conversation


Informations to provide :

```json
{
    "token | device_token": "[string]",
    "conversation_id": "[integer]",
    "conversation_name": "[string(120)]",
    "device_access": "[boolean]"
}
```

* *Not mandatory

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