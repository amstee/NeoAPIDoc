# Create media
**[HOME](../README.md)**

**URL** : `/media/create`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device

**Description :**

Send a json list with the name of the medias you want to create.<br/>
If you want to upload medias for a circle you need to add the circle_id as a parameter.<br/>
As a user you can also upload medias for a device by adding the parameter device_id.<br/>
There is also a field "purpose", this field which is a VARCHAR(32) allows you to add a role to the media.<br/>
*Be careful the field "purpose" is not unique*


Informations to provide :

```json
{
  "token | device_token": "[string]",
  "medias": [
    {
       "purpose": "[string] Ex: profile_picture",
       "name": "[string] Ex: profile.jpg"
    }, 
    {
      "purpose": "[string] Ex: circle_picture",
      "name": "[string] Ex: circle_profile.png",
      "circle_id": "[integer]"
    },
    {
       "purpose": "[string] Ex: profile_picture",
       "name": "[string] Ex: device_profile.png",
       "device_id": "[integer]"
    }
  ]
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "media_list": [
    {
        "id": "[integer]",
        "filename": ["string"],
        "extension": "[string]",
        "identifier": "[string]",
        "uploaded": "[string]"
   }
   ],
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