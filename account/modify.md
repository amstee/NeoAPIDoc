# Modify account informations
**[HOME](../README.md)**

Modifying account informations.

**URL** : `/account/modify`

**Method** : `PUT`

**Authentication required** : YES (token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "email(not mandatory)": "[string(120)]",
    "first_name(not mandatory)": "[string(50)]",
    "last_name(not mandatory)": "[string(50)]",
    "birthday(not mandatory)": "[string(datetime)]"
    
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