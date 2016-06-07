# Calculator
<!DOCTYPE html>
<html>
    <head>
<meta charset="UTF-8">
<link rel = "stylesheet" type = "text/css" href= "design.css">
    <title>Calculator</title>
	</head>
<body>
		  <div id = "calculator">
		      <form>
			       <input type="text" id="display"><br /><br />
				   
				   <input type="button" value="<--" id="keys"  onclick="backspace()">
		           <input type="button" value="X^3" id="keys"  onclick="power(3)">
				   <input type="button" value="C" id="keys" onclick="addtoscreen('c')"><br />
				   
				   <input type="button" value="9" id="keys" onclick="addtoscreen('9')">
				   <input type="button" value="8" id="keys" onclick="addtoscreen('8')">
				   <input type="button" value="7" id="keys" onclick="addtoscreen('7')"><br />
				   
				   <input type="button" value="6" id="keys" onclick="addtoscreen('6')">
				   <input type="button" value="5" id="keys" onclick="addtoscreen('5')">
				   <input type="button" value="4" id="keys" onclick="addtoscreen('4')"><br />
				   				   
		           <input type="button" value="3" id="keys" onclick="addtoscreen('3')">
				   <input type="button" value="2" id="keys" onclick="addtoscreen('2')">
				   <input type="button" value="1" id="keys" onclick="addtoscreen('1')"><br />
				 
				   <input type="button" value="0" id="keys" onclick="addtoscreen('0')">	
				   <input type="button" value="/" id="keys" onclick="addtoscreen('/')">
				   <input type="button" value="*" id="keys" onclick="addtoscreen('*')"><br />
				   
				   <input type="button" value="-" id="keys" onclick="addtoscreen('-')">
				   <input type="button" value="+" id="keys" onclick="addtoscreen('+')">
				   <input type="button" value="." id="keys" onclick="addtoscreen('.')"><br />
				   <input type="button" value="=" id="keys" onclick="answer()">
				   				   
				   </form>

</div>
<script type="text/javascript" src="logic.js"></script>
</body>

</html>


#calculator
{
	width: 250px;
	height: 450px;
	border: 1px solid purple;
	text-align: center;
	background: lightblue;
	margin: 150px auto;
	box-shadow: 0px 0px 30px gray;
	
	
}

#display
{
    margin-top: 30px;
    margin-bottom: 20px;
    width: 220px;
    height: 20px;
    border: 1 px solid red;
    box-shadow: 0px 0px 30px red;
    text-align: right;
    font: 20px bold;
    color: black;
}
#keys
{
	width: 40px;
	height: 30px;
	margin-left: 10px;
	margin-bottom: 20px;
	box-shadow: 0px 0px 20px lightpink;
	cursor: pointer;
	
}

#keys:hover
{
	background: yellow;
	font-weight: bold;
}

	
	
	var box=document.getElementById('display');

function addtoscreen(x)
{
	box.value +=x;

	if(x=='c')
	{
		box.value='';
	}
}
function answer()
{
	x=box.value;
	x=eval(x);
	box.value=x;
}

function backspace()
{
	var number=box.value;
	var len=number.length-1;
	var newnumber=number.substring(0,len);
	box.value=newnumber;
	
}
function power(y)
{
	x=box.value;
	x=Math.pow(x,y);
	box.value=x;
}
