Oracle database driver for Laravel
==================================

This is an Oracle PDO_OCI database driver for the Laravel PHP framework.

## Installation ##

1. Move `oracle.php` into `application/libraries/`.
2. Edit `application/config/database.php` and add a new item to the connections array:
    
        'my_oracle_connection' => array(
            'driver'   => 'oracle',
            'host'     => '[HOST]',
            'database' => '[DATABASE]',
            'port'     => '[PORT]',
            'username' => '[USERNAME]',
            'password' => '[PASSWORD]',
            'charset'  => 'UTF-8',
            'prefix'   => '',
        ),
        
3. Still editing `application/config/database.php`, change the "Default Database Connection" to match the custom connection key (in this case, `my_oracle_connection`).

## Notes ##

Oracle supports use of a `tnsnames.ora` configuration file that defines database connection parameters. If such a file resides on your system, you can omit the "host" and "port" configuration settings in step 2 of the Installation instructions.

Oh yeah, also: **this is totally untested and probably doesn't work** (yet). Improvements and fixes are very welcome!