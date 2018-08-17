# Modify account informations

Modifying account informations.

**URL** : `/account/modify`

**Method** : `POST`

**Authentication required** : YES (token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "email"(not mandatory): "[string(128)]",
    "first_name"(not mandatory): "[string(64)]",
    "last_name"(not mandatory): "[string(64)]",
    "birthday"(not mandatory): "[string]"
    
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