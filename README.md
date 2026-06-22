# php-GDPR-CRUD-TOTPauth-adminpage-audit-mysql-datamasking

22 june 2026: 

Future features release 1.3

- preconfigured personal database in executable change columns.
Expect it to be released in 2 days from today.
released 22 june 2026


Release 1.2
- forced password login + TOTP (is required now). See config.php.

Enjoy.

0. Configure columns in database line 73 till 100 in config.php (re-label database fields/columns):

define('FIELD_LABELS', serialize([

    // Personal Information
    
    'relation_number'   => 'Relation Number X',
    
    'passport_number'   => 'Passport Number X',
    
  etc..
  

2. start with admin.php
   - create admin with password, configure softtoken/multifactor One-Time Password.
    
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

Known bug(s)

audit_viewer.php (search record id).

Release information

**release1.1.1.1.7z**

audit_viewer.php: Forbidden 403 (totp_auth.php) non-admin users are redirected to login as admin.
Redirect to logout.php instead of login.php
cleaned config.php file lean code.
