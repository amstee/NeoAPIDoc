# Create User's Account
**[HOME](../README.md)**

Create a NEO user account to either use device, web application or smartphone applications.

**URL** : `/account/create`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "email": "[string(120)]",
    "password": "[string(50)]",
    "first_name": "[string(50)]",
    "last_name": "[string(50)]",
    "birthday": "[string(datetime)]"
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this User.

**Code** : `201 CREATED`

**Content example**

```json
{
    "success": True
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `409 CONFLICT`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```