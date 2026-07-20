<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Bharathraj — Portfolio</title>
<style>
body{
  font-family:Arial, sans-serif;
  background:#0f1724;
  color:#00ff00;
  margin:0;
  padding:0;
  overflow-x:hidden;
}

/* Smooth scroll */
html {
  scroll-behavior: smooth;
}

/* Matrix background */
.matrix-bg{
  position:fixed;
  top:0; left:0;
  width:100%; height:100%;
  background:transparent;
  z-index:1;
  overflow:hidden;
  pointer-events:none;
  color:#00ff00;
  font-family:monospace;
  font-size:14px;
  line-height:16px;
  white-space:pre;
}

/* Profile Section */
header{
  display:flex;
  flex-wrap:wrap;
  align-items:center;
  justify-content:flex-start;
  padding:20px 20px;
  max-width:1200px;
  margin:20px auto;
  position:relative;
  z-index:2;
  background:rgba(0,0,0,0.6);
  box-shadow:0 0 20px #00ff00;
  border-radius:12px;
}
header img{
  width:200px;
  height:200px;
  border-radius:50%;
  margin-right:40px;
  object-fit:cover;
  border:4px solid #00ff00;
  box-shadow:0 0 15px #00ff00;
}
.profile-info{
  border:2px solid #00ff00;
  padding:20px;
  border-radius:12px;
  background:rgba(0,0,0,0.6);
  flex:1;
  min-width:250px;
}
.profile-info h1{margin:0;text-shadow:0 0 8px #00ff00}
.profile-info p{color:#00ff00;margin:8px 0 0;text-shadow:0 0 5px #00ff00}
.profile-info p span{display:block; font-size:0.9rem; color:#00ff66}

/* Dashboard */
.dashboard{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
  gap:20px;
  max-width:1200px;
  margin:30px auto;
  text-align:center;
  background:rgba(0,0,0,0.4);
  padding:20px;
  border-radius:12px;
  border:2px solid #00ff00;
  box-shadow:0 0 15px #00ff00;
  z-index:2;
  position:relative;
}
.dash-card{
  background:rgba(0,0,0,0.5);
  padding:20px;
  border-radius:12px;
  border:1px solid #00ff00;
  box-shadow:0 0 10px #00ff00;
  transition:0.3s;
  text-align:center;
  text-decoration:none;
  color:#00ff00;
  display:block;
}
.dash-card:hover{
  box-shadow:0 0 20px #00ff00;
  transform:translateY(-5px);
}
.dash-card img{
  width:40px;
  margin-bottom:10px;
}
.dash-card h3{margin:0 0 10px;text-shadow:0 0 5px #00ff00;font-size:1.3rem}
.dash-card p{margin:0;text-shadow:0 0 4px #00ff66;font-size:0.85rem}

/* Neon glow for icons */
.glow-logo {
  animation: neon-flicker 1.5s infinite alternate;
  filter: drop-shadow(0 0 5px #00ff00) drop-shadow(0 0 10px #00ff00);
}
@keyframes neon-flicker {
  0%   { filter: drop-shadow(0 0 2px #00ff00) drop-shadow(0 0 5px #00ff00); opacity: 0.8; }
  25%  { filter: drop-shadow(0 0 5px #00ff66) drop-shadow(0 0 10px #00ff66); opacity: 1; }
  50%  { filter: drop-shadow(0 0 10px #00ff00) drop-shadow(0 0 15px #00ff00); opacity: 0.9; }
  75%  { filter: drop-shadow(0 0 8px #00ff66) drop-shadow(0 0 12px #00ff66); opacity: 1; }
  100% { filter: drop-shadow(0 0 5px #00ff00) drop-shadow(0 0 10px #00ff00); opacity: 0.85; }
}

/* Sections */
section{
  padding:40px 20px;
  max-width:1200px;
  margin:20px auto;
  position:relative;
  z-index:2;
  background:rgba(0,0,0,0.6);
  border:2px solid #00ff00;
  border-radius:12px;
  box-shadow:0 0 20px #00ff00;
}
h2{
  margin-bottom:16px;
  border-bottom:2px solid #00ff00;
  padding-bottom:6px;
  text-shadow:0 0 5px #00ff00;
  text-align:center;
}
.skills,.experience,.projects,.contact{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
  gap:16px;
  justify-items:center;
  text-align:center;
}
.card{
  background:rgba(0,0,0,0.5);
  padding:16px;
  border-radius:10px;
  border:1px solid #00ff00;
  color:#00ff00;
  box-shadow:0 0 10px #00ff00;
  transition:0.3s;
  text-align:center;
  text-decoration:none;
}
.card:hover{box-shadow:0 0 20px #00ff00;}
.card h3{text-shadow:0 0 5px #00ff00;margin-top:0}
.muted{color:#00ff66;font-size:0.9rem}
/* Message Form */
.message-form {
  margin-top: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 12px;
}
.message-form input,
.message-form textarea {
  width: 90%;
  max-width: 500px;
  background: rgba(0, 0, 0, 0.6);
  border: 1px solid #00ff00;
  border-radius: 8px;
  color: #00ff00;
  padding: 10px;
  font-size: 1rem;
  box-shadow: 0 0 10px #00ff00;
}
.message-form textarea {
  height: 100px;
  resize: none;
}
.message-form button {
  background: #00ff00;
  color: #0f1724;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 0 15px #00ff00;
  transition: 0.3s;
}
.message-form button:hover {
  background: #00ff66;
  box-shadow: 0 0 25px #00ff00;
}
footer{
  text-align:center;
  padding:20px;
  background:rgba(0,0,0,0.6);
  color:#00ff00;
  margin-top:30px;
  position:relative;
  z-index:2;
  border-top:2px solid #00ff00;
  box-shadow:0 0 15px #00ff00;
}
.contact {
  display: flex;
  flex-direction: column; /* Stack vertically */
  align-items: center;    /* Center horizontally */
  gap: 20px;              /* Space between cards */
}
/* Responsive */
@media(max-width:768px){
  header{flex-direction:column;align-items:center;text-align:center;}
  header img{margin-right:0;margin-bottom:20px;width:150px;height:150px;}
  .profile-info{width:100%;}
  .dash-card img{width:35px;}
  .dash-card h3{font-size:1.1rem;}
  .dash-card p{font-size:0.8rem;}
  .skills,.experience,.projects{grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:12px;}
}
</style>
</head>
<body>
<div class="matrix-bg" id="matrix"></div>

<!-- Profile Section -->
<header id="home">
  <img src="bharath.jpg" alt="profile">
  <div class="profile-info">
    <h1>Bharath Raj</h1>
    <p><span>Full-stack Developer</span></p>
    <p><span>Student</span></p>
    <p><span>Email: bharathraj88700@gmail.com</span></p>
    <p><span>Location: Dharmapuri,Tamilnadu, India</span></p>
  </div>
</header>

<!-- Dashboard Navigation -->
<nav>
<div class="dashboard">
  <a href="#home" class="dash-card">
    <img src="https://img.icons8.com/ios-filled/50/00ff00/home.png" class="glow-logo" alt="Home">
    <h3>Home</h3>
    <p>Welcome Page</p>
  </a>
  <a href="#projects" class="dash-card">
    <img src="https://img.icons8.com/ios-filled/50/00ff00/laptop-coding.png" class="glow-logo" alt="Projects">
    <h3>Projects</h3>
    <p>My Work</p>
  </a>
  <a href="#skills" class="dash-card">
     <img src="https://img.icons8.com/ios-filled/50/00ff00/lightning-bolt.png" class="glow-logo" alt="Skills">
    <h3>Skills</h3>
    <p>Technologies</p>
  </a>
  <a href="#contact" class="dash-card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/contacts.png" class="glow-logo" alt="Contact">
      <h3>Contact</h3>
      <p>Get in Touch</p>
  </a>
</div>
</nav>

<!-- Skills Section -->
<section id="skills">
  <h2>Skills</h2>
  <div class="skills">
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/html-5.png" class="glow-logo"><h3>HTML</h3></div>
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/css3.png" class="glow-logo"><h3>CSS</h3></div>
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/javascript.png" class="glow-logo"><h3>JavaScript</h3></div>
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/react-native.png" class="glow-logo"><h3>React</h3></div>
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/nodejs.png" class="glow-logo"><h3>Node.js</h3></div>
    <div class="card"><img src="https://img.icons8.com/color/48/00ff00/python.png" class="glow-logo"><h3>Python</h3></div>
  </div>
</section>

<!-- Projects Section -->
<section id="projects">
  <h2>Projects</h2>
  <div class="projects">
    <a href="https://github.com/bharath934477/website-" target="_blank" class="card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/restaurant.png" class="glow-logo">
      <h3>Food Website</h3>
      <p class="muted">HTML + CSS + JS</p>
      <p>Delicious restaurant website with online ordering.</p>
    </a>
    <a href="https://github.com/bharath934477/One-Stop-Personalized-Career-Education-Advisor.git" target="_blank" class="card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/graduation-cap.png" class="glow-logo">
      <h3>Student Career Advisor</h3>
      <p class="muted">Python + Node.js</p>
      <p>AI-powered career guidance system for students.</p>
    </a>
  </div>
</section>

<!-- Contact Section -->
<section id="contact">
  <h2>Contact Me</h2>
  <div class="contact">
    <div class="card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/new-post.png" class="glow-logo" alt="Email">
      <h3>Email</h3>
      <p class="muted">bharathraj88700@gmail.com</p>
    </div>
    <div class="card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/phone.png" class="glow-logo" alt="Phone">
      <h3>Phone</h3>
      <p class="muted">+91 93447 70265 </p>
    </div>
    <div class="card">
      <img src="https://img.icons8.com/ios-filled/50/00ff00/worldwide-location.png" class="glow-logo" alt="Location">
      <h3>Location</h3>
      <p class="muted">Dharmapuri, Tamilnadu, India</p>
    </div>
    <!-- Added Social Media Links -->
      <div class="card">
        <img src="https://img.icons8.com/ios-filled/50/00ff00/github.png" class="glow-logo" alt="GitHub">
        <h3>GitHub</h3>
        <a href="https://github.com/bharath934477/My-portfolio.git" target="_blank" class="muted">github.com/bharath934477</a>
      </div>

      <div class="card">
        <img src="https://img.icons8.com/ios-filled/50/00ff00/linkedin.png" class="glow-logo" alt="LinkedIn">
        <h3>LinkedIn</h3>
        <a href="https://www.linkedin.com/in/bharath-raj-887oo" target="_blank" class="muted">bharath-raj-887oo</a>
      </div>

      <div class="card">
        <img src="https://img.icons8.com/ios-filled/50/00ff00/instagram-new.png" class="glow-logo" alt="Instagram">
        <h3>Instagram</h3>
        <a href="https://instagram.com/mr__r15__bharath" target="_blank" class="muted">mr__r15__bharath</a>
      </div>

   </div>
</section>
  <section>
      <!-- Send Message Form -->
  <form class="message-form" onsubmit="sendMessage(event)">
    <input type="text" id="name" placeholder="Your Name" required>
    <input type="email" id="email" placeholder="Your Email" required>
    <textarea id="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
  </form>
  </section>


<footer>
  © <span id="year"></span> Bharath Raj
</footer>

<script>
document.getElementById('year').textContent=new Date().getFullYear();

// Matrix effect
const canvas=document.createElement('canvas');
const ctx=canvas.getContext('2d');
document.getElementById('matrix').appendChild(canvas);
canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

const letters='01';
const fontSize=14;
const columns=Math.floor(canvas.width/fontSize);
const drops=Array(columns).fill(1);

function draw(){
  ctx.fillStyle='rgba(0,0,0,0.05)';
  ctx.fillRect(0,0,canvas.width,canvas.height);
  ctx.fillStyle='#00ff00';
  ctx.font=fontSize+'px monospace';
  for(let i=0;i<drops.length;i++){
    const text=letters[Math.floor(Math.random()*letters.length)];
    ctx.fillText(text,i*fontSize,drops[i]*fontSize);
    if(drops[i]*fontSize>canvas.height && Math.random()>0.975) drops[i]=0;
    drops[i]++;
  }
}
setInterval(draw,35);

window.addEventListener('resize',()=>{
  canvas.width=window.innerWidth;
  canvas.height=window.innerHeight;
});
</script>
</body>
</html>
