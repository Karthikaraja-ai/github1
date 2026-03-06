<!DOCTYPE html>
<html>
<head>
<title>Medicine Reminder</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<h1>Medicine Reminder for Elderly</h1>

<div class="container">
<label>Medicine Name:</label>
<input type="text" id="medicineName">

<label>Reminder Time:</label>
<input type="time" id="reminderTime">

<button onclick="setReminder()">Set Reminder</button>

<h3 id="status"></h3>
</div>

<script src="script.js"></script>

</body>
</html>
body{
font-family: Arial;
text-align:center;
background-color:#f2f2f2;
}

.container{
background:white;
padding:20px;
width:300px;
margin:auto;
margin-top:100px;
border-radius:10px;
box-shadow:0 0 10px gray;
}

input{
width:90%;
padding:8px;
margin:10px;
}

button{
padding:10px;
background:green;
color:white;
border:none;
border-radius:5px;
cursor:pointer;
}
function setReminder(){

let medicine = document.getElementById("medicineName").value;
let time = document.getElementById("reminderTime").value;

document.getElementById("status").innerText =
"Reminder set for " + medicine + " at " + time;

setInterval(function(){

let now = new Date();
let currentTime = now.getHours() + ":" + now.getMinutes();

if(currentTime == time){

alert("Time to take your medicine: " + medicine);

}

},60000);

}