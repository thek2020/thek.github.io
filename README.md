<!DOCTYPE html>
<html>
<body>
<center>
<h2>Link Generator</h2>

<p>Please input a number between 1 and 3811:</p>

<input id="numb">

<button style="color:Violet;" type="button" onclick="myFunction()">Submit</button>

<p id="demo"></p>
<br>
<p id="demo2"></p>
</center>
<script>
function myFunction() {
  var x, text, text2;
  var link1 = '<a href=http://catchup.zeeone.de/vod/ZON';
  var link1a = 'http://catchup.zeeone.de/vod/ZON';
  var u10 ="000";
  var u100 ="00";
  var u1000 = "0";
  var link3 = '.mp4/master-v1-a1.m3u8 target="_blank">';
  var link4 = '</a>'; 
  var link3a = '.mp4/master-v1-a1.m3u8';
  // Get the value of the input field with id="numb"
  x = document.getElementById("numb").value;

  // If x is Not a Number or less than one or greater than 3811
  if (isNaN(x)) {
    text = "Input not valid";
  } else if (x > 0 && x < 10) {
    text2 = link1a + u10 + x + link3a;
	text = link1 + u10 + x + link3 + text2 + link4;
  } else if (x > 9 && x < 100) {
    text2 = link1a + u100 + x + link3a;
	text = link1 + u100 + x + link3 + text2 + link4;
   } else if (x > 99 && x < 1000) {
    text2 = link1a + u1000 + x + link3a;
	text = link1 + u1000 + x + link3 + text2 + link4;
  } else if (x > 999 && x < 3812) {
   text2 = link1a + x + link3a;   
   text = link1 + x + link3 + text2 + link4;
  } else {
    text = "Falsche Zahl";
  }
  document.getElementById("demo").innerHTML = text;
  
}
</script>

</body>
</html> 
