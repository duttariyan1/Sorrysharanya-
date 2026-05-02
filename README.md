<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry Sharanya 💗</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
font-family:Arial, sans-serif;
background:linear-gradient(135deg,#ff9eb5,#ffe4ec);
overflow:hidden;
}

/* Floating Hearts */
.heart{
position:absolute;
color:#ff4d88;
font-size:20px;
animation:float 6s linear infinite;
}

@keyframes float{
0%{transform:translateY(100vh) scale(0);}
100%{transform:translateY(-10vh) scale(1.5);}
}

/* Card */
.card{
background:white;
padding:40px;
border-radius:25px;
box-shadow:0 10px 30px rgba(0,0,0,0.15);
text-align:center;
max-width:500px;
z-index:2;
animation:pop 1s ease;
}

@keyframes pop{
from{transform:scale(0.7);opacity:0;}
to{transform:scale(1);opacity:1;}
}

h1{
color:#ff2e63;
font-size:36px;
margin-bottom:15px;
}

p{
font-size:19px;
color:#444;
line-height:1.7;
min-height:90px;
}

button{
margin-top:20px;
padding:12px 25px;
border:none;
background:#ff2e63;
color:white;
font-size:18px;
border-radius:30px;
cursor:pointer;
transition:0.3s;
}

button:hover{
background:#e6004c;
transform:scale(1.05);
}

.hidden{
display:none;
margin-top:15px;
font-size:22px;
color:#ff2e63;
font-weight:bold;
}
</style>
</head>

<body>

<div class="card">
<h1>Sorry Sharanya 💗</h1>

<p id="text"></p>

<button onclick="forgive()">Please Forgive Me</button>

<div class="hidden" id="msg">You Mean A Lot To Me 💖</div>
</div>

<script>
/* Typing Text */
let message = "I know I made a mistake... and I'm truly sorry. Please forgive me. You matter to me more than you know.";
let i = 0;

function type(){
if(i < message.length){
document.getElementById("text").innerHTML += message.charAt(i);
i++;
setTimeout(type,50);
}
}
type();

/* Forgive Button */
function forgive(){
document.getElementById("msg").style.display="block";
}

/* Floating Hearts */
function createHeart(){
let heart = document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="💗";
heart.style.left=Math.random()*100+"vw";
heart.style.fontSize=(Math.random()*20+15)+"px";
heart.style.animationDuration=(Math.random()*3+3)+"s";
document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},6000);
}

setInterval(createHeart,300);
</script>

</body>
</html>