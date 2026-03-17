<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>سِـيـلـفـر 𝐒𝐋𝐕</title>

<style>

*{
box-sizing:border-box;
font-family:system-ui;
transition:.3s;
}

body{
margin:0;
min-height:100vh;

background:
linear-gradient(rgba(0,0,0,.8),rgba(0,0,0,.8)),
url("background.jpg") center/cover fixed;

color:#fff;
}

.container{
max-width:520px;
margin:auto;
padding:24px;
}

.card{

background:rgba(20,20,25,.85);
border-radius:20px;
padding:22px;

box-shadow:0 25px 70px rgba(0,0,0,.7);

backdrop-filter:blur(10px);
}

.header{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:10px;
}

h1{
font-size:20px;
margin:0;
}

.icon-btn{
background:none;
border:none;
font-size:16px;
color:white;
cursor:pointer;
padding:6px 10px;
border-radius:12px;
}

.icon-btn:hover{
background:rgba(255,255,255,.1);
}

label{
font-size:13px;
opacity:.8;
}

input,textarea{

width:100%;
margin:6px 0 14px;

padding:12px 14px;

border-radius:14px;

border:1px solid rgba(255,255,255,.15);

background:rgba(10,10,14,.6);

color:#fff;

}

textarea{
min-height:120px;
}

button.main{

width:100%;
padding:15px;

border-radius:16px;

border:none;

background:linear-gradient(135deg,#ff2a2a,#ff6b6b);

font-weight:800;

cursor:pointer;

}

button.main:hover{

transform:scale(1.03);

box-shadow:0 0 15px white;

}

.actions{

display:flex;

gap:10px;

margin-top:10px;

}

.actions button{

flex:1;

padding:10px;

border-radius:12px;

border:none;

cursor:pointer;

background:rgba(255,255,255,.1);

color:#fff;

}

.actions button:hover{

background:rgba(255,255,255,.2);

}

.counter{

margin-top:10px;

font-size:13px;

text-align:center;

opacity:.9;

}

.counter b{

background:white;

padding:2px 8px;

border-radius:12px;

margin-left:6px;

}

.footer{

display:flex;

justify-content:space-between;

align-items:center;

margin-top:16px;

font-size:12px;

opacity:.85;

}

.footer a{

color:#fff;

text-decoration:none;

}

.footer a:hover{

color:#FFFFFF;

}

</style>

</head>

<body>

<div class="container">

<div class="card">

<div class="header">

<h1>سِـيـلـفـر 𝐒𝐋𝐕</h1>

</div>

<label>بريد الدعم</label>

<input id="email" placeholder="abuse@telegram.org">

<label>الموضوع</label>

<input id="subject">

<label>كليشة البلاغ</label>

<textarea id="body"></textarea>

<button class="main" id="send">
 ✓ إرسال البلاغ
</button>

<div class="actions">

<button id="reuse">
↺ استخدام آخر كليشة بلاغ
</button>

<button id="reset">
 تصفير عداد البلاغات
</button>

</div>

<div class="counter">

عدد البلاغات المرسلة:
<b id="count">0</b>

</div>

<div class="footer">

<span>سِـيـلـفـر 𝐒𝐋𝐕</span>

<a href="https://t.me/IsSilver1" target="_blank">

تواصل مع المطور

</a>

</div>

</div>

</div>

<script>

let count=0;

let lastText="";

document.getElementById("send").onclick=function(){

let email=document.getElementById("email").value;

let subject=document.getElementById("subject").value;

let body=document.getElementById("body").value;

if(!email){

alert("اكتب بريد الدعم");

return;

}

let link="mailto:"+email+

"?subject="+encodeURIComponent(subject)+

"&body="+encodeURIComponent(body);

window.location.href=link;

count++;

document.getElementById("count").innerText=count;

lastText=body;

};

document.getElementById("reuse").onclick=function(){

if(lastText){

document.getElementById("body").value=lastText;

}

};

document.getElementById("reset").onclick=function(){

count=0;

document.getElementById("count").innerText=0;

};

</script>

</body>

</html>
