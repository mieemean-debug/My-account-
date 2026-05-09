
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mini System</title>

<style>
body{
    font-family: Arial;
    background:#0f172a;
    color:white;
    margin:0;
    padding:20px;
}

.container{max-width:650px;margin:auto;}

.card{
    background:#1e293b;
    padding:15px;
    border-radius:10px;
    margin-bottom:15px;
}

input, button{
    width:100%;
    padding:10px;
    margin-top:10px;
    border:none;
    border-radius:5px;
}

button{
    background:#4f46e5;
    color:white;
    cursor:pointer;
}

button:hover{background:#4338ca;}

.balance{
    font-size:20px;
    color:lime;
}

.modal{
    display:none;
    position:fixed;
    top:0;left:0;
    width:100%;height:100%;
    background:rgba(0,0,0,0.6);
    justify-content:center;
    align-items:center;
}

.box{
    background:#1e293b;
    padding:20px;
    border-radius:10px;
    width:300px;
}
</style>
</head>

<body>

<div class="container">

<!-- TOP BUTTONS -->
<div class="card">
    <button onclick="openProfile()">👤 Profile</button>
    <button onclick="openWithdraw()">💸 Withdraw</button>
</div>

<!-- USER -->
<div class="card">
    <h3>👤 User</h3>
    <input type="text" id="username" placeholder="আপনার নাম">
    <p>💰 Balance: <span id="balance" class="balance">0</span> টাকা</p>
</div>

<!-- FILE SUBMIT -->
<div class="card">
    <h3>📁 File Submit</h3>
    <input type="file" id="fileInput">
    <button onclick="uploadFile()">Submit</button>
    <p id="msg"></p>
</div>

</div>

<!-- PROFILE -->
<div id="profileBox" class="modal">
  <div class="box">
    <h3>👤 Profile</h3>
    <p>Name: <span id="pname"></span></p>
    <p>Balance: <span id="pbalance"></span> TK</p>
    <button onclick="closeProfile()">Close</button>
  </div>
</div>

<!-- WITHDRAW -->
<div id="withdrawBox" class="modal">
  <div class="box">
    <h3>💸 bKash Withdraw</h3>

    <input type="text" id="bkash" placeholder="bKash Number">
    <input 
