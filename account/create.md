# Create User's Account

Create a NEO user account to either use device, web application or smartphone applications.

**URL** : `/account/create`

**Method** : `POST`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "email": "[unicode 128 chars max]",
    "password": "[unicode 64 chars max]",
    "first_name": "[unicode 64 chars max]",
    "last_name": "[unicode 64 chars max]",
    "birthday": "[datetime chars format]"
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