$Id$

DESCRIPTION
===========
Each user can be individually assigned an IP Addresses ranges from which they are allowed to login from.

If they are not at a valid allowed ip address they cannot login.

Each time a user successfully logs in,  the roles are assigned according to their ip restriction placed on each role. So if a role is not allowed from a specific ip address, they will not have that role for their entire time logged in. This role based ip restriction only applies to roles that are NOT "annonymous user" or "authenticated user"

This module is designed to work with Drupal 6.x.

Installation
=====
1. Copy this directory to a suitable modules directory, such as 
     sites/all/modules
2. Enable the module at: Administer > Site building > Modules
3. Set the error page at: Administer > Site configuration > Restrict by IP
   This is for Login restriction only, and does not apply to the role restriction.
4. You then must change your settings.php file to add the following line
   towards the end of the file:

   $conf['session_inc'] = './sites/all/modules/restrict_by_ip/session_restrict_by_ip.inc';

   Adjust the above to point to where you installed the module, e.g. 
   './sites/all/modules/restrict_by_ip/session_restrict_by_ip.inc' if that 
   is where you installed it.
   
USAGE
=====
1.)	a.) When adding or modifying a user account a Restrict by IP settings fieldset will be a new option.
	b.) When modifying a individual role other than "annonymous user" or "Authenticated User", Restrict by IP settings fieldset will be a new option at the bottom of the page.
2. Type in the IP Address in the Restricted IP Address field and click submit
3. The next time the user tries to login their current IP will be checked against this one and will be redirected to the error page if they are at the wrong IP Address.
	If the user is restricted by an restricted-ip based role restriction, the users roles will be removed for the duration of the session if it's range is not within the range specified on the roles admin page.
4. Simply delete the value, and submit to remove the restriciton.

AUTHOR
======
Matt Rice (mrice [at] mattrice.org) 
Bobby Kramer (panthar1 [at] gmail.com)
