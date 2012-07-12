Php-code
========

php extra code

<?php

$hostname = 'localhost';        // Your MySQL hostname. Usualy named as 'localhost', so you're NOT necessary to change this even this script has already online on the internet.
$dbname   = 'phpmysimplelogin'; // Your database name.
$username = 'root';             // Your database username.
$password = '';                 // Your database password. If your database has no password, leave it empty.

// Let's connect to host
mysql_connect($hostname, $username, $password) or DIE('Connection to host is failed, perhaps the service is down!');
// Select the database
mysql_select_db($dbname) or DIE('Database name is not available!');

?>

Next step, save document below and name it as ‘index.php’:

<?php

// Inialize session
session_start();

// Check, if user is already login, then jump to secured page
if (isset($_SESSION['username'])) {
header('Location: securedpage.php');
}

?>
<html>

<head>
<title>PHPMySimpleLogin 0.3</title>
</head>

<body>

<h3>User Login</h3>

<table border="0">
<form method="POST" action="loginproc.php">
<tr><td>Username</td><td>:</td><td><input type="text" name="username" size="20"></td></tr>
<tr><td>Password</td><td>:</td><td><input type="password" name="password" size="20"></td></tr>
<tr><td>&nbsp;</td><td>&nbsp;</td><td><input type="submit" value="Login"></td></tr>
</form>
</table>

</body>

</html>

<!DOCTYPE html> 
<html>  
  <head>
    <title>Golf score keeper</title>
    <script src="http://www.google.com/jsapi"></script>
    <script>
      google.load("jquery", "1.4.1");
    </script>
  </head>
  <body>
    <form action="upload.html" method="get">
      <div>
        <label for="1">Hole 1</label>
        <input type="number" min="1" value="4" name="1" size="2" step="1" />
      </div>
      <div>
        <label for="2">Hole 2</label>
        <input type="number" min="1" value="4" name="2" size="2" step="1" />
      </div>
      <div>
        <input type="email" placeholder="Enter your email address" size="40"/>
      </div>
      <div>
        <input type="text" id="lat_field" name="latitude" />
        <input type="text" id="long_field" name="longitude" />
      </div>
      <script>
        navigator.geolocation.getCurrentPosition(
          function(pos) {
            $("#lat_field").val(pos.coords.latitude);
            $("#long_field").val(pos.coords.longitude);
          }
        );
      </script>
      <div>
        <input type="submit" value="Upload Score" />
      </div>
    </form>
  </body>
</html> 

