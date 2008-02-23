$Id$

DESCRIPTION
===========
Each user can be individually assigned an IP Address which they are allowed to 
login from. If they are not at that address they cannot login.

This module is designed to work with Drupal 5.x.

Installation
=====
1. Copy this directory to a suitable modules directory, such as 
    sites/all/modules
2. Enable the module at: Administer > Site building > Modules
3. Set the error page at: Administer > Site configuration > Restrict by IP

USAGE
=====
1. When modifying a user account a Restrict by IP settings fieldset will be a new option.
2. Type in the IP Address in the Restricted IP Address field and click submit
3. The next time the user tries to login their current IP will be checked against this one.
4. Simply delete the value, and submit to remove the restriciton.

AUTHOR
======
Matt Rice (mrice [at] mattrice.org)