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
