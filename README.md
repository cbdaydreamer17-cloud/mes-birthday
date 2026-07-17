<!DOCTYPE html>
<html>
<head>

<title>Happy Birthday Abelaye 🎂</title>

<style>

body {
  margin:0;
  text-align:center;
  font-family:Georgia, serif;
  background:linear-gradient(135deg,#0f4c81,#dbe9f4,#8fb8d8);
  min-height:100vh;
  padding-top:40px;
  overflow:hidden;
}


/* Countdown */
#countdown {
  color:white;
  font-size:35px;
  margin-top:150px;
}


/* Birthday Question */
#question {
  display:none;
  background:white;
  width:85%;
  max-width:420px;
  margin:auto;
  padding:30px;
  border-radius:25px;
  box-shadow:0 0 25px gray;
}


button {
  padding:15px 30px;
  margin:15px;
  border:none;
  border-radius:30px;
  font-size:20px;
  cursor:pointer;
}


.yes {
  background:#0f4c81;
  color:white;
}


.no {
  background:#ddd;
}


/* Birthday Card */
#card {
  display:none;
  background:white;
  width:85%;
  max-width:500px;
  margin:auto;
  padding:25px;
  border-radius:25px;
  box-shadow:0 0 25px gray;
  animation:show 2s;
}


@keyframes show {

from {
 opacity:0;
 transform:scale(.5);
}

to {
 opacity:1;
 transform:scale(1);
}

}


img {
  width:250px;
  height:250px;
  object-fit:cover;
  border-radius:50%;
  border:8px solid silver;
  box-shadow:0 0 25px #0f4c81;
}


h1 {
  color:black;
  font-size:40px;
  text-shadow:none;
}


p {
  font-size:20px;
  line-height:1.5;
}
</style>

</head>

<body>


<!-- Countdown -->

<div id="countdown">

A special surprise is waiting for you... 🎁

<br><br>

<span id="number">3</span>

</div>



<!-- Question -->

<div id="question">

<h1>🎂 Is it Abelaye's Birthday?</h1>


<button class="yes" onclick="celebrate()">
YES 💙
</button>


<button class="no">
NO 😄
</button>

</div>




<!-- Floating balloons -->

<div class="balloon b1">🎈</div>

<div class="balloon b2">🎈</div>

<div class="balloon b3">🎈</div>




<!-- Money rain -->

<div class="money" style="left:10%;">💵</div>

<div class="money" style="left:30%;animation-delay:1s;">💰</div>

<div class="money" style="left:50%;animation-delay:2s;">💵</div>

<div class="money" style="left:70%;animation-delay:3s;">💰</div>

<div class="money" style="left:90%;animation-delay:1.5s;">💵</div>




<!-- Birthday Card -->

<div id="card">


<img src="IMG_20260717_081636_454">


<h1>
🎉 Happy Birthday, Abelaye! 🎂❤️
</h1>



<p>
mess the real one... yene tsede sew! 🌼❤️<br>
Enkuan teweledk! 🥳
</p>



<p>
Wishing you the happiest birthday ever, mess! 🎊🎉
</p>



<p>
Thank you for being such an amazing friend.<br>
May this year bring you endless happiness, success, laughter and unforgettable memories. ✨
</p>



<p>
Stay awesome, keep smiling, and never change.<br>
You're one of a kind! 😄💙
</p>




<p>
💙 From Bettisha 💙
</p>



<button onclick="showSecret()">
💌 Open Secret Message
</button>



<p id="secret" style="display:none;color:red;">

😁 Yasebkew misakabet amet yargleh ye bereha guade😂,<br>

bet bet tsede buna,weta stlu bira metatatah gra gon ysteh✊🤣

<br><br>

🫵🫶❤️

</p>



</div>
<script>


// Countdown

let count = 3;

let timer = setInterval(function(){

count--;

document.getElementById("number").innerHTML = count;


if(count == 0){

clearInterval(timer);

document.getElementById("countdown").style.display="none";

document.getElementById("question").style.display="block";

}

},1000);





// YES button magic

function celebrate(){

document.getElementById("question").style.display="none";


// Balloon explosion

for(let i=0; i<25; i++){

let balloon = document.createElement("div");

balloon.innerHTML="🎈";

balloon.style.position="fixed";

balloon.style.left="50%";

balloon.style.top="50%";

balloon.style.fontSize="45px";

balloon.style.setProperty("--x",
(Math.random()*500-250)+"px");

balloon.style.setProperty("--y",
(Math.random()*500-250)+"px");


balloon.style.animation="explode 2s forwards";


document.body.appendChild(balloon);

}



// Show card

setTimeout(function(){

document.getElementById("card").style.display="block";

},1500);


}




// Secret message

function showSecret(){

document.getElementById("secret").style.display="block";

}


</script>




<style>


/* Floating balloons */

.balloon {

position:fixed;

font-size:60px;

animation:float 7s infinite linear;

}


.b1 {
left:10%;
animation-duration:6s;
}


.b2 {
left:50%;
animation-duration:8s;
}


.b3 {
left:85%;
animation-duration:5s;
}



@keyframes float {

from {
transform:translateY(100vh);
}

to {
transform:translateY(-120vh);
}

}




/* Balloon explosion */

@keyframes explode {

from {

transform:translate(0,0);

opacity:1;

}


to {

transform:translate(var(--x),var(--y));

opacity:0;

}

}





/* Money falling */

.money {

position:fixed;

top:-50px;

font-size:35px;

animation:fall 5s linear infinite;

}



@keyframes fall {

from {

transform:translateY(-50px) rotate(0deg);

}


to {

transform:translateY(110vh) rotate(360deg);

}

}


</style>



</body>

</html>
