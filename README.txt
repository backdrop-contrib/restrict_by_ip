$Id$

DESCRIPTION
===========
Each user can be individually assigned an IP Addresses and/or IP Address ranges from which they are allowed to login from.

If they are not at a valid allowed ip address they cannot login.

This module is designed to work with Drupal 6.x.

Installation
=====
1. Copy this directory to a suitable modules directory, such as 
     sites/all/modules
2. Enable the module at: Administer > Site building > Modules
3. Set the error page at: Administer > Site configuration > Restrict by IP

USAGE
=====
1. When adding or modifying a user account a Restrict by IP settings fieldset will be a new option.
2. Type in the IP Address in the Restricted IP Address field and click submit
3. The next time the user tries to login their current IP will be checked against this one and will be redirected to the error page if they are at the wrong IP Address.
4. Simply delete the value, and submit to remove the restriciton.

AUTHOR
======
Matt Rice (mrice [at] mattrice.org)
