# Checking email availability

Checking email availability.

**URL** : `/account/create/available`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "email": "string(128)"
    
}
```

## Success Response

**Condition** : If email is available.

**Code** : `200 OK`

**Content example**

```json
{
    "success": True
}
```

### OR

**Condition** : If email is unavailable.

**Code** : `200 OK`

**Content example**

```json
{
    "success": False
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