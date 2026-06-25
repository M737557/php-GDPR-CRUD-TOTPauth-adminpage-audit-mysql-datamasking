# php-GDPR-CRUD-TOTPauth-adminpage-audit-mysql-datamasking

1.7 release contains bug
 Fatal error: Uncaught PDOException: SQLSTATE[HY000] [1049] Unknown database 'contact_manager_release170prd' 
all releases
pagination working. Fixed in release1.8
 
**25 june 2026 07:45**


Features to expect to **launch soon**
- Stay cool.

 **Features release 2.3**
- config.php:

define('COLUMN_MAX_LENGTH', serialize([

    'a' => 12,
    
    'b' => 12,
    
    'c' => 12,
    
    'd' => 15,  //bigger max length limit
    
    'e' => 12,
    
    // etc.
    
]));
 
  
  config.php re-label database with line 98 till line 131

  
   'a' => 'Field A',
  
   'b' => 'Field B',

For bigger data columns this is cool new feature. No Multilines anymore. 


 **Features release 2.2**
- Caution, this database schema is different from before, you cannot upgrade this release working. Without beginning again.
- abcdefghijklmnopqrstuvwxyz database with re-label function
- mysql queries are now for different schema, therefor I didn't include them in this release.


   
  
Enjoy.

config.php re-label this line 89 till line 123.
// ID Column
    'id' => 'ID',
    // Custom Fields A-Z
    'a' => 'Field A',
    'b' => 'Field B',
    'c' => 'Field C',

  
**Features release 1.9**
- bug fix pagination working


**Features release 1.8**
- audit_viewer.php filter based on USER.
- audit_viewer.php filter Record ID.

**Features release 1.7**
- Audit_viewer.php with fixed bug, record id lookup and search through.
- added new mysql query, join two databases rot47.
- do not use this version: contains bug
 Fatal error: Uncaught PDOException: SQLSTATE[HY000] [1049] Unknown database 'contact_manager_release170prd' 
  

**Features release 1.6**

- double click table record to edit
- config.php in a secure bubble (not able to edit config.enc file).
- PRO: enc file creation.7z (Hook require-once (read.php) in index.php to launch bubble configuration as *.enc file.)

Enjoy this release.
  



**Release of 'mysql queries rot47.txt' and Release1.5**

- configure routine tasks first, then launch the queries.
- Addes CSRF protection to admin.php
- joined query of two (crud) databases
-   Enjoy.


22 june 2026: 

**Release 1.4**
Released on 22 june 2026 20:09
- authRequireLogin(); added to index.php (guest access was possible in 1.3)



**Release 1.3**
Released on 22 june 2026 19:18
- re(label) columns in config.php line 73-100.
- forced password login + TOTP (is required now). See config.php.
  

**Release 1.2**
- forced password login + TOTP (is required now). See config.php.


**release1.1.1.1**

- audit_viewer.php: Forbidden 403 (totp_auth.php) non-admin users are redirected to login as admin.
- Redirect to logout.php instead of login.php



**Quick Manual:**

1. first launch
   - point browser to website/directory
   - lookup in files directory (admin_setup_info.txt created). Logon with included parameters(username/password/totp)
   - setup totp on smartphone, from appstore or playstore authenticator apps like microsoft authenticator or go to:
   https://totp.danhersam.com/
https://support.microsoft.com/nl-NL/authenticator/download-microsoft-authenticator


3. Configure columns in config.php line 73 till 100 (re-label database fields/columns):
    
    'relation_number'   => 'Relation Number X',
    
    'passport_number'   => 'Passport Number X',
    
  etc..
  

2. start with admin.php
   - create admin with password, configure softtoken/multifactor One-Time Password.
   - after setting up password uncomment line 8 //authRequireAdmin(); to authRequireAdmin();
    
3. config.php
   - configure database settings
   - configure datamasking settings
  
4. run index.php
   - create data
  
5. check audit_viewer.php
   - audit/undo newdata old data (restore)
  
Enjoy.

Got questions or feature request, contact me.
matijn@gmail.com

+++++++

Known bug(s)/ fixed list:

audit_viewer.php (search record id) fixed in release 1.8



