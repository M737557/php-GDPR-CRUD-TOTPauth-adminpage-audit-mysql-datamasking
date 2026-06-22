# php-GDPR-CRUD-TOTPauth-adminpage-audit-mysql-datamasking

22 june 2026: 

Release 1.2
- forced password login + TOTP (is required now). See config.php.

Enjoy.

0. Configure columns in database, from line 542 in index.php:
   - replace 'relation_number', 'passport_number' etcetera for own needs. Allow to REPLACE FOR ALL in current notepad/notepad++

   `id`                 INT(11)   NOT NULL AUTO_INCREMENT,
        `relation_number`    TEXT      NOT NULL,
        `passport_number`    TEXT      DEFAULT NULL,
        `gender`             TEXT      DEFAULT NULL,
        `initials`           TEXT      DEFAULT NULL,
        `first_name`         TEXT      NOT NULL,
        `nickname`           TEXT      DEFAULT NULL,
        `name_prefix`        TEXT      DEFAULT NULL,
        `last_name`          TEXT      NOT NULL,
        `postal_code`        TEXT      DEFAULT NULL,
        `house_number`       TEXT      DEFAULT NULL,
        `street`             TEXT      DEFAULT NULL,
        `city`               TEXT      DEFAULT NULL,
        `language`           TEXT      DEFAULT NULL,
        `relationship_group` TEXT      DEFAULT NULL,

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
