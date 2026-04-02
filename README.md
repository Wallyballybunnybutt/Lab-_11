# Lab 11 - Puppet LAMP Stack & User Management

## Overview
This project uses Puppet to:
- Create users and groups
- Deploy a LAMP stack (Apache, PHP, MariaDB)
- Test configuration with a simple file

---

## Files

### server_users_groups.pp
Creates users and groups with:
- SHA-512 hashed passwords
- Home directories (`managehome => true`)
- Group assignments

Users:
- user04 -> group01  
- user05 -> group02  
- user06 -> group01, group02  
- user07 -> default group

---

### lamp_stack_server.pp
Installs and configures:
- Apache (`apache2`)
- PHP (`php`, `libapache2-mod-php`, `php-cli`, `php-mysql`)
- MariaDB (`mariadb-server`)
- Deploys `phpinfo.php` to test PHP
- Apache is also set to run and restart when changes are made

---

### phpinfo.php
Simple PHP test file:
```php
<?php
phpinfo()
?>
```
---

### testing_puppet.pp
- test file created
