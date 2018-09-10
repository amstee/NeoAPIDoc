# Username Availability
**[HOME](../README.md)**

**URL** : `/device/username/available/<username>`

**Method** : `GET`

**Authentication required** : NO

**Permissions required** : None


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

**Condition** : Username not available.

**Code** : `400`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```