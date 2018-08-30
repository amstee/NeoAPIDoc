# Invite user to circle
**[HOME](../README.md)**

**URL** : `/circle/invite`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "circle_id": "[integer]",
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

**Condition** : User is not part of your circle and connot be invited.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "Utilisateur n'appartient pas au cercle spécifié",
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