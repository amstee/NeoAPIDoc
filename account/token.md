# Checking JWT validity
**[HOME](../README.md)**

**URL** : `/token/verify`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : None


Informations to provide :

```json
{
    "token": "[JWT token]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "message": "Le token json est valide",
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