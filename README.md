<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday Mes 👑</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{

background:#050505;

font-family:Georgia,serif;

color:white;

overflow-x:hidden;

text-align:center;

}


/* GOLD STARS */

.star{

position:fixed;

color:gold;

font-size:18px;

animation:twinkle 3s infinite alternate;

opacity:.8;

}


@keyframes twinkle{

from{

opacity:.2;
transform:scale(.8);

}

to{

opacity:1;
transform:scale(1.4);

}

}



/* INTRO */

#intro{

height:100vh;

display:flex;

flex-direction:column;

justify-content:center;

align-items:center;

}


.intro1{

font-size:28px;

letter-spacing:4px;

color:gold;

animation:fade 2s;

}


.intro2{

font-size:22px;

margin-top:25px;

color:white;

animation:fade 3s;

}


#count{

margin-top:40px;

font-size:60px;

color:gold;
.profile{

width:260px;

height:260px;

border-radius:50%;

object-fit:cover;

border:8px solid gold;

box-shadow:
0 0 20px gold,
0 0 40px goldenrod;

margin-top:25px;

}


.title{

margin-top:25px;

font-size:45px;

color:gold;

text-shadow:
0 0 12px gold,
0 0 25px goldenrod;

}


.message{

margin:30px auto;

max-width:700px;

font-size:22px;

line-height:1.8;

color:#f8f8f8;

}


.gallery{

display:flex;

justify-content:center;

flex-wrap:wrap;

gap:20px;

margin-top:35px;

}


.gallery img{

width:260px;

border-radius:20px;

border:5px solid gold;

box-shadow:
0 0 15px gold;

transition:.4s;

}


.gallery img:hover{

transform:scale(1.05);

}


.secretBtn{

margin-top:35px;

padding:15px 35px;

font-size:20px;

background:gold;

color:black;

border:none;

border-radius:30px;

cursor:pointer;

font-weight:bold;

}


#secret{

display:none;

margin-top:25px;

font-size:22px;

color:red;

font-weight:bold;

line-height:1.8;

}


.signature{

margin-top:40px;

font-size:26px;

color:gold;

}

</style>

</head>

<body>


<div id="intro">

<h1 class="intro1">
🎬 BETTISHA PRESENTS
</h1>

<h2 class="intro2">
A Birthday Surprise ✨
</h2>

<div id="count">3</div>

</div>



<div id="starring">

<h2>⭐ STARRING ⭐</h2>

<div id="mes">
👑 MES 👑
</div>

</div>



<div id="main">

<img
class="profile"
src="IMG_20260717_081636_454.jpg">

<h1 class="title">

🎉 Happy Birthday Mes 🎂

</h1>


<div class="message">

Happy Birthday, Mes! 🎂💛<br><br>

Today is all about celebrating an amazing person.
May your life always be filled with happiness, success, good health, unforgettable memories and endless smiles the real one❣️.

Keep shining and keep being the wonderful person you are.ye bereha guade😅 ✨

</div>


<div class="gallery">

<img src="IMG_20260717_081648_216.jpg">

</div>


<button
class="secretBtn"
onclick="showSecret()">

💌 Open Secret Message

</button>


<div id="secret">

😁 Yasebkew misakabet amet yargleh Mes,<br>

genzeb bekelalu mnagegnbet amet yhunlennn,,buna mtafelaleh migegnbet year yargew😅 ✊🤣

<br><br>

🫵🫶❤️

</div>


<div class="signature">

💛 Crafted with love,<br>

— Bettisha ✨

</div>

</div>
<style>

/* Floating Gold Stars */

.star1{
left:8%;
top:10%;
animation-delay:0s;
}

.star2{
left:22%;
top:30%;
animation-delay:1s;
}

.star3{
left:40%;
top:18%;
animation-delay:2s;
}

.star4{
left:60%;
top:42%;
animation-delay:1.5s;
}

.star5{
left:78%;
top:15%;
animation-delay:2.5s;
}

.star6{
left:92%;
top:35%;
animation-delay:3s;
}


/* Gold Balloons */

.balloon{

position:fixed;

bottom:-120px;

font-size:55px;

animation:floatUp 8s linear infinite;

}

.b1{left:10%;animation-delay:0s;}
.b2{left:30%;animation-delay:2s;}
.b3{left:50%;animation-delay:4s;}
.b4{left:70%;animation-delay:1s;}
.b5{left:90%;animation-delay:3s;}

@keyframes floatUp{

from{

transform:translateY(0);

}

to{

transform:translateY(-130vh);

}

}

</style>



<!-- Floating Stars -->

<div class="star star1">✨</div>
<div class="star star2">✨</div>
<div class="star star3">✨</div>
<div class="star star4">✨</div>
<div class="star star5">✨</div>
<div class="star star6">✨</div>



<!-- Gold Balloons -->

<div class="balloon b1">🎈</div>

<div class="balloon b2">🎈</div>

<div class="balloon b3">🎈</div>

<div class="balloon b4">🎈</div>

<div class="balloon b5">🎈</div>
<script>

// Countdown
let count = 3;

let counter = setInterval(function(){

document.getElementById("count").innerHTML = count;

count--;

if(count < 0){

clearInterval(counter);

// Hide intro
document.getElementById("intro").style.display="none";

// Show STARRING
document.getElementById("starring").style.display="flex";

// After 3 seconds, show main page
setTimeout(function(){

document.getElementById("starring").style.display="none";

document.getElementById("main").style.display="block";

},3000);

}

},1000);




// Secret Message

function showSecret(){

document.getElementById("secret").style.display="block";

}

</script>
<script>

// Smooth scroll to top when the page appears
window.onload = function () {
    window.scrollTo(0, 0);
};

// Optional: reveal the secret message with a small fade effect
function showSecret() {
    let secret = document.getElementById("secret");
    secret.style.display = "block";
    secret.style.opacity = "0";

    let opacity = 0;
    let fade = setInterval(function () {
        opacity += 0.05;
        secret.style.opacity = opacity;

        if (opacity >= 1) {
            clearInterval(fade);
        }
    }, 30);
}

</script>

</body>
</html>
