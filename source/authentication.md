Authentication
--------------

### Supported Browsers
* Current and recent Firefox, IE, Safari, Seamonkey, Opera an Chrome versions all supported
* Requires browser to have Javascript enabled. The CORAL interface relies heavily on AJAX, JQuery and JQuery plugins

### Server-Side Requirements and Setup

**Database**

The recommended name for the auth database is `coral_auth_prod`. If you have created a “coral” user
for your other modules, it should have select, insert, update and delete privileges to the
`coral_auth_prod`. If you are using different users for your other CORAL installs, you will need to make
sure that all of your other users have select access to the new authentication database.

### Installation

Installation can occur in one of two ways – either through the web installation script or manually. Web
installation will provide advantages over manual because will check MySQL privileges and PHP version.
Installation is recommended in the /coral/auth/ directory. It is also recommended that you check out
the CORAL Main Landing page and place it into the /coral/ directory. This contains an HTML file and
graphics for each module, similar to the landing page on the CORAL demo website.

#### Web Installation

Visit `http://.../coral/auth/install/` and follow instructions on the screen

_Be sure to remove the `/install/` directory once installation is complete_

#### Manual Installation

Install database tables

1. Create new database schema (recommended name is `coral_auth_prod`)
3. Run SQL file

Update `/admin/configuration.ini`

_**Important:**_ First rename `/admin/configuration_sample.ini` to `/admin/configuration.ini`

1. Under [settings]
     1. timeout=  
length of time (in seconds) the user remains logged in
1. Under [database]
     1. type=mysql  
currently only MySQL is supported but other database types could be supported if modifications to the generic database classes are made
     1. host=  
MySQL server - could be localhost as well
     1. name=  
database name (for example, `coral_resources_prod`)
     1. username=  
recommended to have a single user with select, update, insert, delete access to all coral modules
     1. password=  
password for above mentioned user
1. For security reasons, remove the `/install/` directory once the installation is complete

### Setting up and using Authentication module for the first time

After installation a single default user will be set up with the username _coral_ and password _admin_. In
your browser, visit the page `/coral/auth/admin.php` to add your username/password and set yourself
(or anyone else) as ‘admin’. The ‘admin’ users will be able to add, edit and delete users in
Authentication. Once you have another ‘admin’ user set up you can delete the original coral/admin
user.

_**Important:**_ Your usernames should always match the usernames in other CORAL modules for proper privileges. Note that after the CORAL Authentication install the only user set up is ‘coral’. Be sure to add all other users from other modules on the CORAL Authentication Admin page – link is at the bottom of
the login page.

### Using Authentication with other CORAL Modules

CORAL Authentication should be installed before this point, and all of your users from the other CORAL
Modules should be added to CORAL Authentication. If you already have other CORAL modules installed and wish to switch to CORAL Authentication, you will need to add the following to each config file - `/coral/module_name/admin/configuration.ini` under [settings]

```
authModule=Y
authDatabaseName=coral_auth_prod
```

You can leave the `remoteAuthVariableName` alone.

Users will still need to be set up in each module separately because of varying permissions for each. In
Organizations and Resources any users in CORAL Authentication will be set up as view only users if they
are not already set up. In Usage and Licensing users must be set up explicitly for access. The username
in the CORAL module and CORAL Authentication need to match.

You also will probably want to add a ‘logout’ link to your modules pages. You can either download the
new `/coral/modulename/templates/header.php` or you can make the following manual change:

Around line 85, replace the following line:

`<br /><span style='color:red;font-size:90%;'>&nbsp;</span>`

With the following line:

`<br /><?php if($config->settings->authModule == 'Y'){ echo "<a href='" . $coralURL .
"auth/?logout'>logout</a>"; } ?>`

If you find yourself with mismatching users (i.e. only the ‘coral’ user in auth but only other users in the remaining modules), you should go into CORAL Authentication as your ‘admin’ user (coral/admin by default), go into the Admin page, and add the usernames to match the other modules.