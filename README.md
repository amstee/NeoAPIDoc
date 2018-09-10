# NEO API documentation

This is the api documentation which will detail the available routes, how to access them, their parameters and answers.

### Web Sockets

[Menu](sockets/menu.md) : Description of the web sockets handlers

### Account

Resources for viewing, manipulating and creating accounts.

* [Create account](account/create.md) : `POST /account/create`
* [Log in account](account/login.md) : `POST /account/login`
* [Log out account](account/logout.md) : `POST /account/logout`
* [Account informations](account/info.md) : `POST /account/info`
* [Modify account informations](account/modify.md) : `PUT /account/modify`
* [Check email availability](account/create_available.md) : `GET /email/available/<email>`
* [Modify account password](account/modify_password.md) : `PUT /account/modify/password`
* [Verify account token validity](account/token.md) : `POST /token/verify`
* [Account information](account/device_info.md) : `GET /account/info/<user_id>`

### Device

Resources for viewing, manipulating devices.

* [Update device](device/update.md) : `POST /device/update`
* [Log in device](device/device_info.md) : `POST /device/authenticate`
* [Log out device](device/login.md) : `POST /device/logout`
* [Device informations](device/logout.md) : `POST /device/info/<device_id>`
* [Check username availability](device/available.md) : `GET /device/username/available/<username>`
* [Modify device password](device/modify_password.md) : `PUT /device/modify/password`
* [Verify device token validity](device/token.md) : `POST /device/token/verify`

### Circle

Endpoints for viewing, manipulating and creating circles.

* [Invite user to circle](circle/invite.md): `POST /circle/invite`
* [Join a circle](circle/join.md): `POST /circle/join`
* [Reject cirle invitation](circle/reject.md): `POST /circle/reject`
* [Quit circle](circle/quit.md): `POST /circle/quit`
* [Kick user from circle](circle/kick.md): `POST /circle/kick`
* [Create circle](circle/create.md): `POST /circle/create`
* [Update cirle](circle/update.md): `PUT /circle/update`
* [Circle informations](circle/info.md): `GET /circle/info/<circle_id>`
* [List circles](circle/list.md): `GET /user/circle/list`

### Conversation

Resources for viewing, manipulating and creating conversations.

* [Conversation information](conversation/info.md): `GET /conversation/info/<conversation_id>`
* [Update conversation informations](conversation/update.md): `PUT /conversation/update`
* [List conversation](conversation/list.md): `GET /conversation/list/<circle_id>`
* [Invite user to conversation](conversation/invite.md): `POST /conversation/invite`
* [Kick user from conversation](conversation/kick.md): `POST /conversation/kick`
* [Quit conversation](conversation/quit.md): `POST /conversation/quit`
* [Add/Remove device from conversation](conversation/remove.md): `PUT /conversation/device/set`
* [Promote user in conversation](conversation/promote.md): `PUT /conversation/promote`

### Message

Resources for viewing, manipulating and creating messages.

* [Delete message](message/delete.md): `DELETE /message/delete`
* [Message informations](message/info.md): `GET /message/info/<message_id>`
* [Update message](message/update.md): `PUT /message/update`
* [List messages in conversation](message/list.md): `GET /message/list/<conversation_id>/<quantity>`
* [Send first message](message/first_message.md): `POST /message/first-message`
* [Send message](message/send.md): `POST /message/send`
* [Send first message to device](message/first-message_to_device.md): `POST /message/device/first-message`
* [First message (as Device)](message/device_first_message.md): `POST /device/message/first-message`
* [Send message (as Device)](message/device_send.md): `POST /device/message/send`

### Media

Resources for creating, uploading and retrieving medias.

* [Delete media](media/delete.md): `DELETE /media/delete`
* [Media informations](media/info.md): `GET /media/info/<media_id>`
* [List medias (for a message)](media/media_list.md): `GET /message/media/list/<message_id>`
* [Media informations (as admin)](media/info_admin.md): `POST /admin/media/info`
* [Create media](media/create.md): `POST /media/create`
* [Find media](media/find.md): `POST /media/find`
* [upload media](media/upload.md): `POST /media/upload/<media_id>`
* [retrieve media](media/request.md): `GET /media/retrieve/<media_id>`


### Admin

Resources available for Admin users

* [Media delete](media/delete_admin.md): `DELETE /admin/media/delete`
* [Media update](media/update_admin.md): `PUT /admin/media/update`
* [Create conversation](conversation/create.md): `POST /admin/conversation/create`
* [Delete conversation](conversation/delete.md): `DELETE /admin/conversation/delete`
* [Delete circle](circle/delete.md): `DELETE /admin/circle/delete`
* [Promote account](account/promote.md) : `POST /admin/account/promote`
* [Create Device](device/admin_create.md) : `POST /admin/device/create`
* [Delete Device](device/admin_delete.md) : `POST /admin/device/delete`
* [Activate Device](device/admin_activate.md) : `POST /admin/device/activate`
* [Device Credentials](device/admin_credentials.md) : `POST /admin/device/credentials`

