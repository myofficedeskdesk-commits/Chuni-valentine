<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>For Chuni 💘</title>  
  
<style>  
body {  
  margin: 0;  
  height: 100vh;  
  background: linear-gradient(135deg, #ff758c, #ff7eb3);  
  display: flex;  
  justify-content: center;  
  align-items: center;  
  font-family: 'Poppins', sans-serif;  
  overflow: hidden;  
  color: white;  
  text-align: center;  
}  
  
.card {  
  background: rgba(255,255,255,0.15);  
  padding: 40px;  
  border-radius: 25px;  
  backdrop-filter: blur(10px);  
  box-shadow: 0 20px 40px rgba(0,0,0,0.25);  
  max-width: 420px;  
  width: 90%;  
  z-index: 2;  
}  
  
h1 {  
  font-size: 2.3em;  
}  
  
p {  
  font-size: 1.2em;  
}  
  
button {  
  padding: 14px 28px;  
  font-size: 1.1em;  
  border: none;  
  border-radius: 30px;  
  cursor: pointer;  
  margin: 10px;  
  transition: transform 0.2s;  
}  
  
button:hover {  
  transform: scale(1.1);  
}  
  
.yes {  
  background: #ff3d68;  
  color: white;  
}  
  
.no {  
  background: white;  
  color: #ff3d68;  
}  
  
#message {  
  margin-top: 20px;  
  font-size: 1.4em;  
  display: none;  
}  
  
/* Floating hearts */  
.heart {  
  position: absolute;  
  bottom: -20px;  
  font-size: 20px;  
  animation: floatUp 6s linear infinite;  
  opacity: 0.7;  
}  
  
@keyframes floatUp {  
  0% {  
    transform: translateY(0) scale(1);  
    opacity: 0.8;  
  }  
  100% {  
    transform: translateY(-110vh) scale(1.5);  
    opacity: 0;  
  }  
}  
</style>  
</head>  
  
<body>  
  
<div class="card">  
  <h1>Hey Chuni 💕</h1>  
  <p>  
    You make my ordinary days special<br>  
    just by being you 🌸  
  </p>  
  
  <h2>Will you be my Valentine? 💘</h2>  
  
  <button class="yes" onclick="sayYes()">Yes 💖</button>  
  <button class="no" onclick="moveNo()">No 🙈</button>  
  
  <div id="message"></div>  
</div>  
  
<script>  
function sayYes() {  
  const msg = document.getElementById("message");  
  msg.style.display = "block";  
  msg.innerHTML = "You just made my heart so happy 💞<br>I love you, Chuni 🌹";  
}  
  
function moveNo() {  
  const btn = event.target;  
  btn.style.position = "absolute";  
  btn.style.left = Math.random() * 80 + "%";  
  btn.style.top = Math.random() * 80 + "%";  
}  
  
// hearts generator  
setInterval(() => {  
  const heart = document.createElement("div");  
  heart.className = "heart";  
  heart.innerHTML = "💖";  
  heart.style.left = Math.random() * 100 + "vw";  
  heart.style.fontSize = (20 + Math.random() * 20) + "px";  
  document.body.appendChild(heart);  
  
  setTimeout(() => heart.remove(), 6000);  
}, 400);  
</script>  
  
</body>  
</html>  
