# Create User's Account
**[HOME](../README.md)**

Retrieving account informations.

**URL** : `/account/info`

**Method** : `POST`

**Authentication required** : YES (token)

**Permissions required** : User


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
                "email": "[string(128)]",
                "first_name": "[string(64)]",
                "last_name": "[string(64)]",
                "birthday": "[datetime]",
                "created": "[datetime]",
                "updated": "[datetime]",
                "isOnline": "[boolean]",
                "type": "[string(16)]",
                "hangout": "[boolean]",
                "facebook": "[boolean]",
                "circles": {
                            "id": "[integer]",
                            "name": "[string(128)]",
                            "created": "[datetime]",
                            "updated": "[datetime]",
                            "users": {
                                        "id": "[integer]",
                                        "created": "",
                                        "updated": self.updated,
                                        "privilege": self.privilege,
                                        "user_id": self.user.get_simple_content(),
                                        "conversation_id": self.conversation.get_simple_content(),
                                        "messages": [message.get_simple_content() for message in self.messages]
                                     },
                            "device": self.device.get_simple_content() if self.device is not None else {},
                            "invites": [invite.get_content(False) for invite in self.circle_invite],
                            "conversations": [conv.get_simple_content() for conv in self.conversations],
                            "medias": [link.get_content() for link in self.media_links]
                           },
                "invites": [invite.get_content() for invite in self.circle_invite],
                "conversations": [link.get_simple_content() for link in self.conversation_links],
                "medias": [link.get_content() for link in self.media_links]
               },
    "success": True
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```