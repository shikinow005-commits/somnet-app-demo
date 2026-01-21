# somnet-app-demo
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Somnet Customer Assistant</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
    margin:0;
    height:100vh;
    background:#1b1b1b;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:Arial, sans-serif;
}

/* PHONE FRAME */
.phone{
    width:380px;
    height:760px;
    background:#000;
    border-radius:36px;
    padding:12px;
    box-shadow:0 25px 60px rgba(0,0,0,.8);
}

/* SCREEN */
.screen{
    width:100%;
    height:100%;
    background:linear-gradient(#0f5fa8,#8fd0ff);
    border-radius:28px;
    overflow:hidden;
    position:relative;
}

/* HEADER */
.header{
    background:#0f5fa8;
    color:#fff;
    padding:16px;
}

.header-top{
    display:flex;
    align-items:center;
    gap:10px;
    font-size:16px;
}

.profile{
    width:40px;
    height:40px;
    border-radius:50%;
    background:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#0f5fa8;
    font-size:20px;
    font-weight:bold;
}

.welcome{
    margin-top:18px;
    font-size:18px;
}

/* GRID */
.grid{
    padding:16px;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:14px;
}

/* CARD */
.card{
    background:#fff;
    border-radius:16px;
    padding:16px 10px;
    text-align:center;
    box-shadow:0 6px 12px rgba(0,0,0,.15);
    font-size:14px;
    font-weight:bold;
    cursor:pointer;
}

.icon{
    width:48px;
    height:48px;
    border-radius:12px;
    margin:0 auto 8px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:22px;
    color:#fff;
}

.orange{background:#ff9f43;}
.red{background:#ff4d4d;}
.gold{background:#f5b400;}
.green{background:#4cd964;}
.purple{background:#7d5fff;}
.teal{background:#1abc9c;}

/* OUTPUT AREA */
#contentBox{
    margin:16px;
    background:#fff;
    border-radius:16px;
    padding:16px;
    font-size:14px;
    box-shadow:0 6px 12px rgba(0,0,0,.15);
}

/* BOTTOM NAV */
.bottom-nav{
    position:absolute;
    bottom:0;
    left:0;
    width:100%;
    background:#fff;
    display:flex;
    justify-content:space-around;
    padding:10px 0;
}

.nav-item{
    font-size:20px;
    color:#888;
}

.nav-item.active{
    color:#0f5fa8;
}
</style>
</head>

<body>

<div class="phone">
    <div class="screen">

        <!-- HEADER -->
        <div class="header">
            <div class="header-top">
                <div class="profile">👤</div>
                <div>Somnet Customer Assistant</div>
            </div>
            <div class="welcome">Ku soo dhowow Somnet</div>
        </div>

        <!-- GRID MENU -->
        <div class="grid">

            <div class="card" onclick="showBundles()">
                <div class="icon orange">⚙️</div>
                Data Bundles
            </div>

            <div class="card" onclick="showPUK()">
                <div class="icon red">🧾</div>
                PUK Code
            </div>

            <div class="card" onclick="showVIP()">
                <div class="icon gold">VIP</div>
                VIP Numbers
            </div>

            <div class="card" onclick="showTech()">
                <div class="icon green">📞</div>
                Technical Support
            </div>

            <div class="card" onclick="showBalance()">
                <div class="icon purple">📅</div>
                Balance Check
            </div>

            <div class="card" onclick="showContact()">
                <div class="icon teal">❌</div>
                Contact Support
            </div>

        </div>

        <!-- OUTPUT AREA -->
        <div id="contentBox">
            Ku soo dhowow Somnet 👋<br>
            Dooro adeegga aad rabto.
        </div>

        <!-- BOTTOM NAV -->
        <div class="bottom-nav">
            <div class="nav-item active">🏠</div>
            <div class="nav-item">🔗</div>
            <div class="nav-item">⚙️</div>
        </div>

    </div>
</div>

<script>
// DATA BUNDLES
function showBundles(){
    document.getElementById("contentBox").innerHTML =
    "<b>📦 Data Bundles</b><br><br>" +
    "🔹 <b>Daily</b><br>1GB – $1<br>Activate: *770#<br><br>" +
    "🔹 <b>Weekly</b><br>5GB – $5<br>Activate: *770#<br><br>" +
    "🔹 <b>Monthly</b><br>20GB – $15<br>Activate: *770#";
}

// PUK CODE
function showPUK(){
    document.getElementById("contentBox").innerHTML =
    "<b>🔑 PUK Recovery</b><br>" +
    "For security reasons, verification is required.<br>" +
    "Please contact customer support if SIM is blocked.";
}

// VIP NUMBERS (GOLD)
function showVIP(){
    document.getElementById("contentBox").innerHTML =
    "<b>⭐ VIP Numbers – Gold</b><br><br>" +
    "📞 061 777 0001<br>" +
    "📞 061 777 0022<br>" +
    "📞 061 777 0055<br>" +
    "📞 061 777 0088<br><br>" +
    "<b>Gold Features:</b><br>" +
    "• Easy to remember<br>" +
    "• Business use<br>" +
    "• Priority support<br><br>" +
    "👉 Contact support to request.";
}

// TECHNICAL SUPPORT
function showTech(){
    document.getElementById("contentBox").innerHTML =
    "<b>💬 Technical Support</b><br>📞 Call: 141<br>💬 WhatsApp support<br>🕒 24/7";
}

// BALANCE CHECK
function showBalance(){
    document.getElementById("contentBox").innerHTML =
    "<b>💰 Balance Check</b><br>Dial *123# or check in the app dashboard.";
}

// CONTACT SUPPORT
function showContact(){
    document.getElementById("contentBox").innerHTML =
    "<b>📩 Contact Support</b><br>Email: support@somnet.so<br>Phone: 141<br>WhatsApp support available";
}
</script>

</body>
</html>
