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
```PHP
<?php 
// SETUP for smartDB
define('DB_HOST', 'localhost');			// Hostname of database
define('DB_NAME', 'sampleDB');			// Name of database
define('DB_USER', 'root');				// Username of database
define('DB_PASSWORD', 'root');			// User password of database

// Including class
require_once 'class.SmartDB.php';
```

###INSERT
```PHP
$db = new SmartDB;

// Insert single row
// Prepare columns and values
$data = array();
$data['column1'] = 'mix value 1';
$data['column2'] = 'mix value 2';

// Insert into dummy_table
$db->insert('dummy_table', $data);
```

###SELECT
```PHP
$db = new SmartDB;

// SELECT * FROM dummy_table
$num_rows = 10; // Optional
$db->get('dummy_table', $num_rows);
```

###DELETE
```PHP
$db = new SmartDB;

// SELECT FROM dummy_table limit 10
$num_rows = 10; // Optional
$db->delete('dummy_table', $num_rows);
```

###UPDATE
```PHP
$db = new SmartDB;

// update
// Prepare columns and values
$data = array();
$data['column1'] = 'new mix value 1';
$data['column2'] = 'new mix value 2';

// Insert into dummy_table
$db->update('dummy_table', $data);
```

###RESULT - ALL RESULTS - LOOP
- Assign single row to $result
```PHP
$result = $db->result();
print_r($result);
```
- Assign all rows to $results
```PHP
$results = $db->all_results();
print_r($results);
```
- Loop through row
```PHP
while($result = $db->result()){

	print_r($result);
	echo '<br>';
}
```

###ROW COUNT - Effected rows
- Display the total counts after GET or effect rows count after DELETE or UPDATE
```PHP
echo $db->row_count();
```

###LAST INSERT ID
- Returns the ID of the last inserted row or sequence value
```PHP
echo $db->last_id();
```

###SELECT COLUMNS
```PHP
// SELECT id FROM dummy_table
$columns = array();
$columns[] = 'id';

$db->select($columns);
$num_rows = 10; // Optional
$db->get('dummy_table', $num_rows);
```

###Using WHERE
- @param = column name
- @param = value
- @pram = condition
```PHP
$db->where('id', 2, '=');
$db->get('dummy_table') or $db->delete('dummy_table');
```

###CUSTOM QUERY

###BIND

###JOIN

###_DATE

##Licensing
Free for personal use only, If you want to use this class for commercial please contact me

##Help & Feedback
Have you made something cool with SmartDB? Let me know on thehanif@msn.com
