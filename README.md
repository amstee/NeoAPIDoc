# NEO API documentation

This is the api documentation which will detail the available route, how to access them, their parameters and answers.

### Account related

Endpoints for viewing, manipulating and creating accounts.

* [Create account](account/create.md) : `POST /account/create`
* [Log in account](account/login.md) : `POST /account/login`
* [Log out account](account/logout.md) : `POST /account/logout`
* [Account informations](account/info.md) : `POST /account/info`
* [Modify account informations](account/modify.md) : `POST /account/modify`
* [Check email availability](account/create_available.md) : `POST /account/create/available`
* [Modify account password](account/modify_password.md) : `POST /account/modify/password`
* [Verify account token validity](account/token.md) : `POST /token/verify`
* [Promote account (as Admin)](account/promote.md) : `POST /admin/account/promote`
* [Account information (as Device)](account/device_info.md) : `POST /device/account/info`

### Circle related

Endpoints for viewing, manipulating and creating circles.

* [Invite user to circle](circle/invite.md): `POST /circle/invite`
* [Join a circle](circle/join.md): `POST /circle/join`
* [Reject cirle invitation](circle/reject.md): `POST /circle/reject`
* [Quit circle](circle/quit.md): `POST /circle/quit`
* [Kick user from circle](circle/kick.md): `POST /circle/kick`
* [Create circle](circle/create.md): `POST /circle/create`
* [Update cirle](circle/update.md): `POST /circle/update`
* [Delete circle (as Admin)](circle/delete.md): `POST /admin/circle/delete`
* [Circle informations](circle/info.md): `POST /circle/info`
* [List circles](circle/list.md): `POST /circle/list`
* [Circle informations (as Device)](circle/device_info.md): `POST /device/circle/info`

### Conversation related

Endpoint for viewing, manipulating and creating conversations.

* [Create conversation (as Admin)](conversation/create.md): `POST /admin/conversation/create`
* [Delete conversation (as Admin)](conversation/delete.md): `POST /admin/conversation/delete`
* [Conversation informations (as Device)](conversation/device_info.md): `POST /device/conversation/info`
* [Conversation information](conversation/info): `POST /conversation/info`
* [Update conversation informations](conversation/update.md): `POST /conversation/update`
* [List conversation](conversation/list.md): `POST /conversation/list`
* [List conversation (as Device)](conversation/device_list.md): `POST /device/conversation/list`
* [Invite user to conversation](conversation/invite.md): `POST /conversation/invite`
* [Kick user from conversation](conversation/kick.md): `POST /conversation/kick`
* [Quit conversation](conversation/quit.md): `POST /conversation/quit`
* [Remove device from conversation](conversation/remove.md): `POST /conversation/device/remove`
* [Promote user in conversation](conversation/promote.md): `POST /conversation/promote`
* [Add device in conversation](conversation/device_add.md): `POST /conversation/device/add`