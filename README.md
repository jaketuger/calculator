<!Doctype><meta charset = "UTF-8">

<html>
<head>
<title>MY Calculator</title>
<STYLE>
h1 {
	text-align:center;
}


</STYLE>
<h1>Need A Calculator</h1>
</head>
<body>
<form>
<input type="text" name="number1" placeholder="Number">
<input type="text" name="number2" placeholder="Number">

<select name="operators">
 <option>None</option>
 <option>Add</option>
 <option>Subtract</option>
 <option>Multiply</option>
 <option>Divide</option>
 </select>
 <br>
 
 <button type="submit" name="submit" value="submit" >Calculate</button>
</form>

<p>The answer is:</p>

<?php

if (isset($_GET['submit'])){
	$result1 = $_GET['number1'];
	$result2 = $_GET['number2'];
	$operators = $_GET['operators'];
	
	switch ($operators) {
		case 'None':
		echo "You need to select a method!";
		break;
		case 'Add':
		echo $result1 + $result2;
		break;
		case 'Subtract':
		echo $result1 - $result2;
		break;
		case 'Multiply':
		echo $result1 * $result2;
		break;
		case 'Divide':
		echo $result1 / $result2;
		break;
		
		
	}

}

?>
</body>
</html>
