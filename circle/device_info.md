# Circle informations (as Device)

**URL** : `/device/circle/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


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
    "content": {
                "id": "[integer]",
                "name": "[string(120)]",
                "created": "[datetime]",
                "updated": "[datetime]",
                "users": [link.get_content(False) for link in self.user_link],
                "device": self.device.get_simple_content() if self.device is not None else {},
                "invites": [invite.get_content(False) for invite in self.circle_invite],
                "conversations": [conv.get_simple_content() for conv in self.conversations],
                "medias": [link.get_content() for link in self.media_links]
               },
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