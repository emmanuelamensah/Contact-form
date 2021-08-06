# Contact-form
contact form in php

<html>
<head>
</head>
<body>
<h4>Contact Forms</h4>
<form method="post"action="sendmail.php">
Name :<input
type="text"name="uname"><br>
Phone Number.:<input
type="text"name="phone"><br>
Email ID: <input
type="text"name="email"><br>
Message: <textarea
name="message">
</textarea><br>
<input type="submit" value="Submit">
</form>
</body>
</html>

<php
$uname=$_POST['uname'];
$phone=$_POST['phone'];
$email=$_POST['email'];
$message=$_POST['message'];

$to = "yawadumensah@gmail.com";
$subject= "Contact";
$message=$message."\n Name:
".$uname."\n Phone:".$phone."\n Email: $email;
if(mail($to,$subject,$message))
{
	echo "Received";
	}
{else
	echo "again";
}
?>
