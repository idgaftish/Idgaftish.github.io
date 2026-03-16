<!DOCTYPE html>
<html>
<head>
<title>Birthday Surprise</title>

<style>

body{
background: linear-gradient(135deg,#ff9a9e,#fad0c4);
font-family: Arial;
text-align:center;
padding-top:100px;
overflow:hidden;
}

h1{
font-size:60px;
color:white;
}

p{
font-size:22px;
color:white;
}

button{
padding:15px 30px;
font-size:18px;
border:none;
border-radius:25px;
background:white;
cursor:pointer;
margin-top:20px;
}

button:hover{
background:#ffe6ea;
}

img{
width:250px;
border-radius:20px;
margin-top:20px;
}

.heart{
position:fixed;
top:-10px;
color:white;
font-size:24px;
animation:fall 5s linear infinite;
}

@keyframes fall{
0%{transform:translateY(-10vh);}
100%{transform:translateY(110vh);}
}

</style>
</head>

<body>

<h1>🎂 Happy Birthday!</h1>

<p>
I wanted to make something special instead of just sending a text.
So I made this little website just for you.
Hope your birthday is amazing ❤️
</p>

<img src="https://i.imgur.com/3ZQ3Z4K.jpeg">

<br>

<button onclick="showMessage()">
Open Your Surprise 🎁
</button>

<p id="secret" style="display:none;">
You mean a lot to me and I'm really lucky to have you in my life.
Hope this year brings you happiness and everything you wish for ❤️
</p>

<audio autoplay loop>
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<script>

function showMessage(){
document.getElementById("secret").style.display="block";
}

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"vw";
heart.style.animationDuration=(Math.random()*3+2)+"s";
document.body.appendChild(heart);

setTimeout(()=>{
heart.remove();
},5000);
}

setInterval(createHeart,300);

</script>

</body>
</html>
