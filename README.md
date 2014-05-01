SmartDB
=======
- Smart Database Class that proccess most posible PDO Queries in smart way.
- This class provides various methods to handle query as eazy as posible.
- Class contains CRUD method includind various JOIN functionalities
- Class also provides column and fiels selection mehods
- You can also find biding methors for custom queries or special JOINs.
- A extra _date method is available for customizing dates or get current date customized.


##Tutorial

###SETUP
- Add this code at top of your php applications or use a seperate file for setup
```
<?php 
// SETUP for smartDB
define('DB_HOST', 'localhost');			// Hostname of database
define('DB_NAME', 'sampleDB');			// Name of database
define('DB_USER', 'root');				// Username of database
define('DB_PASSWORD', 'root');			// User password of database

// Including class
require_once 'class.SmartDB.php';

$db = new SmartDB;
```

###INSERT

###SELECT

###DELETE

###UPDATE

###RESULT - ALL RESULTS - LOOP

###ROW COUNT - Effected rows

###LAST INSERT ID

###SELECT COLUMNS

###Using WHERE

###CUSTOM QUERY

###BIND

###JOIN

###_DATE

##Licensing
Free for personal use only, If you want to use this class for commercial please contact me

##Help & Feedback
Have you made something cool with SmartDB? Let me know on thehanif@msn.com
