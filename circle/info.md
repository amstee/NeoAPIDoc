# Circle informations

**URL** : `/circle/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "circle_id": "[integer]"
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
                "name": "[string(128)]",
                "created": "[datetime]",
                "updated": "[datetime]",
                "users": {
                            "id": "[integer]",
                            "user": {
                                    "id": "[integer]",
                                    "email": "[string(128)]",
                                    "first_name": "[string(64)]",
                                    "last_name": "[string(64)]",
                                    "birthday": "[datetime]",
                                    "created": "[datetime]",
                                    "updated": "[datetime]",
                                    "isOnline": "[boolean]",
                                    "type": "[string(16)]",
                                    },
                            "circle": "[integer]",
                            "created": "[datetime]",
                            "updated": "[datetime]",
                            "privilege": "[string(16)]"
                         },
                "device": {
                            "id": "[integer]",
                            "name": "[string(128)]",
                            "created": "[datetime]",
                            "updated": "[datetime]",
                            "circle_id": "[integer]",
                            "activated": "[boolean]",
                            "username": "[string(128)]",
                            "is_online": "[boolean]"
                          },
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