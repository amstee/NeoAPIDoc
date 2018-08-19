# Create User's Account

Log in account (receiving JWT token).

**URL** : `/account/login`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "email": "[string(120)]",
    "password": "[string(50)]",
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

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```