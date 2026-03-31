---
title: SM3 Security Overview
source: madcap.md
version: '1.0'
last_updated: '2026-02-19'
short_description: SM3 Security Overview
long_description: Help documentation for SM3 Security Overview in the 4GL system.
---

# SM3 Security Overview

### Client Types

* Traditional Windows MFC client\
  Client is an application installed on a user’s PC. Connection to the Linux server can be setup as either telnet or SSH.
* Open Client (web-based client)\
  User connects through their web browser. Connection can be either http or https-based. For https connection, an SSL certificate can be installed. See also [Using the Browser Version](https://4glsol.com/sm3-helpdocs/Content/Welcome/open_client_tips.htm).

### Login Types

Anytime a user logs into SM3, a login to the Linux server takes place first (transparently) before the user logs into SM3.

When using the Windows client, a user will have a PIV file (connection file) saved on their computer that they will use to launch the SM3 session. The PIV file will contain the Linux username and password (encrypted) that will be used to log the user into Linux, after which the user will be presented with the SM3 login screen, where they will enter their SM3 username and password. Users can be set up with a number of allowable retries — if they reach their limit, they will be notified and an administrator will need to unlock their account.

SM3 also has the concept of single sign on where a user can have their Windows username stored against their SM3 user profile. A reserved Linux/SM3 user will be set up and if the PIV file has been set up to login as that user, after logging into Linux SM3 will find the SM3 user that has been set up with that computer’s Windows username and automatically log them into SM3 as that user. If it is unable to find a user with that Windows username, the user will be prompted to provide their SM3 username and password to login, like the paragraph above.

When using the Open Client, all users will log into Linux as the same user. The concept of logging into SM3 by either providing their SM3 username and password or via single sign on (Windows username) still apply as above.

### Roles

SM3 has the concept of security profiles, which define which menu items a user can access. For example, users in a Sales profile would have access to menu items under the ‘Order Entry’ menu (and sub-menus) but may not have access to items under the ‘Accounts Payable’ menu (and sub-menus) and may have access to some, but not all, menu items under the ‘Inventory’ (and sub-menus) menu.

[![](https://4glsol.com/sm3-helpdocs/Content/Resources/Images/ADM_sec_profiles.png)](https://4glsol.com/sm3-helpdocs/Content/Resources/Images/ADM_sec_profiles.png)

### User Security/Options

Just because two users belong to the same security profile it doesn’t necessarily mean they are equal. Additional security settings can be controlled at the user level. For example, user A and user B both belong to the ‘Sales’ profile. User ‘A’ could be allowed to override the current exchange rate when entering a sales order, whereas user ‘B’ could be not allowed to do this. On the other hand, user ‘B’ could be allowed to change the payment terms on an order, while user ‘A’ may not be allowed to do this.

[![](https://4glsol.com/sm3-helpdocs/Content/Resources/Images/ADM_op_OE_security.png)](https://4glsol.com/sm3-helpdocs/Content/Resources/Images/ADM_op_OE_security.png)
