# php-GDPR-CRUD-TOTPauth-adminpage-audit-mysql-datamasking

22 june 2026: 

1. working on forced TOTP Login with password.
2. setup.php page to edit columns for specific database needs and configuration of database table/columns.

20 june 2026.

1. start with admin.php
   - create admin with password, configure softtoken/multifactor One-Time Password.
    
2. config.php
   - configure database settings
   - configure datamasking settings
  
3. run index.php
   - create data
  
4. check audit_viewer.php
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
