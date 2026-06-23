# php-GDPR-CRUD-TOTPauth-adminpage-audit-mysql-datamasking

22 june 2026: 

**Release 1.4**
Released on 22 june 2026 20:09
- authRequireLogin(); added to index.php (guest access was possible in 1.3)



**Release 1.3**
Released on 22 june 2026 19:18
- re(label) columns in config.php line 73-100.
- forced password login + TOTP (is required now). See config.php.
- 

**Release 1.2**
- forced password login + TOTP (is required now). See config.php.





**Quick Manual:**

1. Configure columns in config.php line 73 till 100 (re-label database fields/columns):
    
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

Known bug(s)

audit_viewer.php (search record id).

Release information

**release1.1.1.1.7z**

audit_viewer.php: Forbidden 403 (totp_auth.php) non-admin users are redirected to login as admin.
Redirect to logout.php instead of login.php
cleaned config.php file lean code.
