
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Love Story ❤️</title>
<style>
body {
  margin: 0;
  font-family: 'Georgia', 'Palatino Linotype', 'Times New Roman', serif;
  background: linear-gradient(to bottom, #ffdde1, #ee9ca7);
  color: rgb(227, 88, 88);
  text-align: center;
}

/* General Card Styling */
.card {
  background: rgba(255,255,255,0.1);
  border-radius: 40px;
  padding: 40px;
  margin: 30px auto;
  max-width: 900px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  text-align: center;
}

/* ROWS */
.row {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  box-sizing: border-box;
  padding: 20px 10px;
}

h1, h2, h3, p, textarea, button {
  font-style: italic;
  line-height: 1.5;
}

img {
  display:;
  max-width: 200px;
  height: auto;
  border-radius: 15px;
  margin: 10px auto;
}

video {
  display:;
  max-width: 200px;
  height: auto;
  border-radius: 15px;
  margin: 10px auto;
}

textarea {
  width: 85%;
  max-width: 400px;
  height: 70px;
  border-radius: 10px;
  border: none;
  padding: 10px;
  margin: 10px auto;
  display: block;
  resize: vertical;
  font-size: 18px;
}

button {
  display: block;
  margin: 10px auto;
  padding: 10px 20px;
  border: none;
  border-radius: 20px;
  background: white;
  color: #e91e63;
  font-size: 18px;
  cursor: pointer;
}

/* Floating Hearts */
.heart {
  position: fixed;
  color: red;
  animation: float 6s linear infinite;
}
@keyframes float { from {transform: translateY(100vh);} to {transform: translateY(-10vh);} }

/* Sending Overlay */
#sendingOverlay {
  position: fixed;
  top:0; left:0;
  width:100%; height:100%;
  background:rgba(0,0,0,0.85);
  display:none;
  justify-content:center;
  align-items:center;
  z-index:9999;
}

.sendingBox{
  background: linear-gradient(to bottom, #ff758c, #ff7eb3);
  padding:30px;
  border-radius:20px;
  width:80%;
  max-width:400px;
  text-align:center;
}

.loader{
  margin:20px auto;
  border:5px solid white;
  border-top:5px solid #e91e63;
  border-radius:50%;
  width:40px;
  height:40px;
  animation:spin 1s linear infinite;
}
@keyframes spin{ to{transform:rotate(360deg);} }

#surpriseMemories, #finalMessage, #loveMessage, #messageDisplay { 
  display: none; 
  margin-top: 15px; 
  text-align: center;
}

/* QUESTION SLIDES */
.slide { display: none; }
.active { display: block; }

@media (max-width: 600px) {
  .row { padding: 15px 5px; }
  textarea { width: 95%; }
}
.floating {
  position: fixed;
  pointer-events: none;
  z-index: 999;
  font-weight: bold;
}

/* Glowing Heart */
.glow {
  text-shadow: 0 0 5px #ff66cc, 0 0 10px #ff66cc, 0 0 15px #ff3388, 0 0 20px #ff66cc;
  animation-name: floatUp;
  animation-timing-function: linear;
  animation-fill-mode: forwards;
}

/* Pink Gradient Heart */
.gradientHeart {
  background: linear-gradient(45deg, #ff9ccf, #ff66cc, #ff3388);
  -webkit-text-fill-color: transparent;
  animation-name: floatUp;
  animation-timing-function: linear;
  animation-fill-mode: forwards;
}

/* Floating Up */
@keyframes floatUp {
  0% {
    transform: translateY(0) translateX(0) scale(1);
    opacity: 1;
  }
  50% {
    transform: translateY(-50vh) translateX(15px) scale(1.2);
  }
  100% {
    transform: translateY(-110vh) translateX(-15px) scale(0.8);
    opacity: 0;
  }
}

/* Floating Down (falling hearts / petals) */
@keyframes floatDown {
  0% {
    transform: translateY(0) translateX(0) rotate(0deg) scale(1);
    opacity: 1;
  }
  50% {
    transform: translateY(50vh) translateX(20px) rotate(180deg) scale(1.2);
  }
  100% {
    transform: translateY(110vh) translateX(-20px) rotate(360deg) scale(0.8);
    opacity: 0;
  }
}

/* Sparkle */
.sparkle {
  color: #fff;
  text-shadow: 0 0 3px #fff, 0 0 6px #ffe0f0, 0 0 10px #ffb3d9;
  animation: sparkleMove linear forwards;
}

@keyframes sparkleMove {
  0% { transform: translateY(0) scale(0.5); opacity: 1; }
  100% { transform: translateY(-100vh) scale(1.2); opacity: 0; }
}
</style>
</head>
<body>

<!-- INTRO SLIDE -->
<div class="row">
  <div class="card">
    <h1>26th❤️ US</h1>
    <p>The day you walked into my life and changed everything.</p>
    <p>
From the very first moment our paths crossed, I felt something extraordinary — a connection so deep, it made ordinary days feel magical and quiet moments feel infinite. Every laugh, every shared glance, every adventure we embarked on together has built the story of us — a story that is uniquely ours, filled with warmth, trust, and a love that grows stronger every single day. Today, as we pause to celebrate our journey and the bond we’ve nurtured, I want you to know how profoundly you mean to me — how every heartbeat whispers your name, and every thought brings a smile when I think of you. This day is special not just because it exists on a calendar, but because it is a reflection of all the moments we’ve cherished, the memories we’ve created, and the love we continue to share. And as a small gesture from me to you, here is this page — a little world of our own, built from my heart, just for you. 💖
    </p>
  </div>
</div>

<!-- ROW 1: QUESTIONS -->
<div class="row">
  <div class="card">
    <h2>From My Heart to Yours ❤️</h2>
    <p>Before we relive our memories, I want to hear your heart. Your feelings matter to me more than anything.</p>
    <div id="slidesContainer"></div>
    <div>
      <button onclick="prevSlide()">Previous</button>
      <button onclick="nextSlide()">Next</button>
    </div>
  </div>
  <button onclick="sendAnswers()">📤 Send Your Answers</button>
</div>

<!-- Sending overlay -->
<div id="sendingOverlay">
  <div class="sendingBox">
    <h2>💌 Sending Our Love...</h2>
    <p>Please wait while your beautiful words travel ❤️</p>
    <div class="loader"></div>
  </div>
</div>

<!-- ROW 2: MEMORIES -->
<div class="row">
  <div class="card">
    <h2>Our Beautiful Memories 🌸</h2>
    <p>Every memory here is a piece of my heart - moments that made me realize how deeply I feel for you.</p>

    <button onclick="showMemorySurprise()">Click for a Surprise ❤️</button>
    <button onclick="showLoveMessage()">Write a Message ✍️</button>

    <div id="surpriseMemories" class="card"></div>

    <div id="loveMessage" class="card">
      <p>My Love,</p>
      <p>I want you to know that you are my everything — the smile in my morning, the peace in my evening, and the reason my heart feels alive. Every moment with you is a treasure I cherish forever. You are more than my partner; you are my soul, my joy, and my home.</p>
      <p>Even our simple memories holding hands, laughing together, silent moments, little surprises they all mean the world to me because of you. You make me better, you make me happier, and you make love feel infinite.</p>
      <p>Thank you for being you. Thank you for letting me love you. And thank you for making me fall in love with you again, every single day.</p>
      <p><b>With all my heart ❤️,</b><br>Aalu</p>
      <textarea id="personalMessage" placeholder="Write your personal love message here..."></textarea>
      <button onclick="saveMessage()">💌 Save Message</button>
      <div id="messageDisplay" class="card"></div>
    </div>
  </div>
</div>

<!-- ROW 3: FINAL -->
<div class="row">
  <div class="card">
    <h2>One Last Surprise 🎁</h2>
    <p>If you’ve reached here, it means you’ve walked through our journey once more… and my heart is still standing right beside yours.</p>
    <button onclick="showFinal()">Open My Heart</button>
    <div id="finalMessage" class="card">
      <p>
        तिमी मेरो कथा होइनौ, तिमी मेरो जीवनको सबैभन्दा सुन्दर अध्याय हौ।❤️🧿<br> 
        You are not just part of my story — you are the most beautiful chapter of my life.
      </p>
      <p>
        We created memories from simple moments —  
        holding hands, sharing hugs, stealing kisses,  
        risking everything just to see each other,  
        and finding peace in each other's presence.❤️😭
      </p>
      <p>
        You taught me that love is not in grand gestures,  
        but in quiet moments, soft touches, and the comfort of being understood.💗
      </p>
      <p>
        Thank you for every smile, every hug, every memory.  
        You made my world softer, warmer, and more meaningful.💗😭
      </p>
      <p><b>Will you seal this day with a warm hug and a soft kiss… just for us? 💗💋</b></p>
    </div>
  </div>
</div>

<script>
  setInterval(() => {
  const container = document.body;
  const item = document.createElement("div");
  item.classList.add("floating");

  const types = ["glow", "gradientHeart", "fallingHeart", "petal", "sparkle"];
  const chosen = types[Math.floor(Math.random() * types.length)];

  if (chosen === "glow") {
    item.classList.add("glow");
    item.innerHTML = "💖";
    item.style.animationDuration = (Math.random() * 3 + 4) + "s";
  } else if (chosen === "gradientHeart") {
    item.classList.add("gradientHeart");
    item.innerHTML = "💕";
    item.style.animationDuration = (Math.random() * 3 + 4) + "s";
  } else if (chosen === "fallingHeart") {
    item.classList.add("glow");
    item.innerHTML = "💘";
    item.style.animationName = "floatDown";
    item.style.animationDuration = (Math.random() * 3 + 4) + "s";
  } else if (chosen === "petal") {
    item.innerHTML = "🌸";
    item.style.animationName = "floatDown";
    item.style.animationDuration = (Math.random() * 4 + 3) + "s";
  } else if (chosen === "sparkle") {
    item.classList.add("sparkle");
    item.innerHTML = "✨";
    item.style.animationDuration = (Math.random() * 3 + 3) + "s";
  }

  item.style.left = Math.random() * 100 + "vw";
  const size = Math.random() * 20 + 15;
  item.style.fontSize = size + "px";

  container.appendChild(item);
  const duration = parseFloat(item.style.animationDuration) * 1000;
  setTimeout(() => item.remove(), duration);
}, 200);
// ---------------- QUESTIONS ----------------
let currentSlide = 0;

const memories = [
  { title:"Our First Smile😭❤️", text:"The moment we first connected still feels magical to me. That first smile we shared carried something unspoken, something warm and exciting. It was the beginning of a story I didn’t even know I was waiting for.", question:"Do you remember how you felt when we first started talking?", media: ["photo1.jpeg"] },
  { title:"The Day We Held Hands❤️", text:"The warmth of your hand in mine felt so natural, like it was always meant to be there. In that simple touch, I felt comfort, reassurance, and a quiet promise of togetherness.", question:"Did you feel the same comfort when we held hands?", media: ["photo2.jpeg"] },
  { title:"Our Secret Meetups😭", text:"Every risk we took just to see each other made my heart beat faster. Those secret moments were filled with excitement, longing, and a happiness that made everything else fade away.", question:"Which meetup made your heart race the most?", media:["photo3.jpeg","photo4.jpeg","photo5.jpeg","photo6.jpeg","photo7.jpeg","photo8.jpeg"] },
  { title:"The Warmest Hug", text:"Your hugs felt like home — safe, warm, and full of love. In your arms, the world seemed quieter, and all my worries melted away like they didn’t matter", question:"Do my hugs still feel like your safe place?", media:["photo9.jpeg"] },
  { title:"Our Favorite Cafe Day💗🧿", text:"That simple day at our favorite café turned into one of my most treasured memories. Between soft laughter, shared glances, and comfortable silence, it became unforgettable in the most beautiful way.", question:"Would you relive that day with me again?", media:["photo10.jpeg","photo11.jpeg"] },
  { title:"The Kiss I’ll Never Forget😭😘", text:"When our lips met, time felt like it paused just for us. It wasn’t just a kiss — it was a moment filled with emotion, closeness, and everything we couldn’t put into words.", question:"What did you feel in that moment?", media:["photo12.jpeg"] },
  { title:"The Day I Realized I Love You❤️😭", text:"There was a quiet moment when my heart chose you without hesitation. I realized my feelings had grown deeper than I ever expected, and loving you felt like the most natural thing in the world.", question:"When did you first feel something special for me?", media:["photo13.jpeg","photo0.jpeg"] },
  { title:"Our Silent Comfort❤️", text:"Even when we said nothing at all, being beside you felt complete. Our silence was never empty — it was peaceful, understanding, and full of unspoken connection.", question:"Do you feel peace when we sit together quietly?", media:["photo14.jpeg","video12.mp4"] },
  { title:"The Day Out Adventures😍", text:"Every step we took together during our little adventures felt magical. It didn’t matter where we were — what mattered was that we were side by side, creating memories only we could share.", question:"Which outing of ours is your favorite?", media:["photo15.jpeg","photo16.jpeg","video1.mp4"] },
  { title:"Our Laughs", text:"Your laughter is truly my favorite sound. It’s bright, genuine, and contagious, and every silly moment we’ve shared still plays in my mind like a beautiful highlight reel.", question:"Which silly memory still makes you laugh?", media:[] },
  { title:"Our Long Talks😭💗", text:"Those late-night conversations meant more to me than you know. Talking about dreams, fears, random thoughts, and everything in between made me feel deeply connected to you.", question:"Which conversation of ours touched your heart most?", media:["photo17.jpeg","photo18.jpeg"] },
  { title:"Our Touch & Comfort😭🧿", text:"Your touch has always had a way of calming my chaos. In the gentlest ways, it reassures me, grounds me, and reminds me that I’m not alone.", question:"Do you feel the same peace in my touch?", media:["photo19.jpeg","photo20.jpeg","video2.mp4"] },
  { title:"Our Kisses 💋", text:"In those moments when we kissed, the world seemed to disappear. It was just us — close, connected, and wrapped in a feeling that words could never fully describe.", question:"Do you still feel that spark when we kiss?", media:["photo21.jpeg"] },
  { title:"Our Journey❤️🧿", text:"Our journey hasn’t been perfect, but it’s been beautifully real. Every challenge, every smile, every lesson has shaped something meaningful between us.", question:"What does our journey mean to you?", media:[] },
  { title:"A Question From My Heart😭", text:"No matter what life brings, you remain someone incredibly special to me. Every memory, every feeling, and every little moment we’ve shared holds a permanent place in my heart.", question:"Will you seal this day with a warm hug and kiss… just for us?", media:["photo22.gif"] }
];

const slidesContainer = document.getElementById("slidesContainer");

// create slides
memories.forEach((m,i)=>{
  const slide = document.createElement("div");
  slide.className = "slide card" + (i===0?" active":"");
  slide.style.margin = "20px auto";
  
  let mediaHTML = "";
  m.media.forEach(src=>{
    if(src.endsWith(".mp4")) mediaHTML += `<video controls src="${src}"></video>`;
    else mediaHTML += `<img src="${src}">`;
  });

  slide.innerHTML = `<h3>${m.title}</h3><p>${m.text}</p><p><b>${m.question}</b></p>${mediaHTML}<textarea id="answer${i}" placeholder="Write your answer here..."></textarea>`;
  slidesContainer.appendChild(slide);
});

const slides = document.querySelectorAll("#slidesContainer .slide");
function showSlide(i){ slides.forEach(s=>s.classList.remove("active")); slides[i].classList.add("active"); }
function nextSlide(){ if(currentSlide<slides.length-1){ currentSlide++; showSlide(currentSlide); } }
function prevSlide(){ if(currentSlide>0){ currentSlide--; showSlide(currentSlide); } }

// ---------------- SURPRISE MEMORIES ----------------
const surpriseContent = 
 [
  { 
    title: "Our First Meeting", 
    text: "The moment everything started changing is still so clear in my heart. From the very first glance, something felt different — like destiny quietly weaving our story together. My world didn’t shift loudly, but softly… gently… in the most beautiful way. That day wasn’t just a meeting, it was the beginning of us ❤️✨", 
    media: ["photo23.jpeg","photo24.jpeg"] 
  },

  { 
    title: "Holding Hands", 
    text: "When your hand slipped into mine, it felt like home in the simplest, purest way. That small touch carried warmth, safety, and a silent promise that I wasn’t alone anymore. In that moment, nothing else mattered — just us, walking side by side, fingers intertwined, hearts quietly syncing together 🤍🤝", 
    media: ["photo25.jpeg"] 
  },

  { 
    title: "Our Day Out", 
    text: "Ordinary places somehow turned magical when I was with you. Streets looked brighter, the air felt lighter, and every little thing became a memory worth keeping. It wasn’t about where we went — it was about who I was with. With you beside me, even the simplest day felt like a beautiful adventure 🌸✨", 
    media: ["video3.mp4","photo26.jpeg","photo27.jpeg","video4.mp4"] 
  },

  { 
    title: "Our Secret Meetups", 
    text: "Every risk we took just to see each other made my heart race in the sweetest way. The excitement, the stolen moments, the way our eyes searched for each other — it all felt thrilling and deeply romantic. Those secret meetups weren’t just meetings… they were proof that what we had was worth every heartbeat 💓🔥", 
    media: ["photo28.jpeg","photo29.jpeg","video5.mp4","video10.mp4","photo30.jpeg"] 
  },

  { 
    title: "Your Hug", 
    text: "Your arms became my safest place without even trying. The way you held me made the world feel smaller and softer, like nothing could hurt me there. In your embrace, my worries faded, my heart slowed down, and I felt completely at peace. Your hugs weren’t just hugs — they were comfort, love, and home all at once 🤗❤️", 
    media: ["photo31.jpeg","video6.mp4","photo32.jpeg"] 
  },

  { 
    title: "Our Laughs", 
    text: "Your laughter is still my favorite sound in the entire world. It’s bright, contagious, and filled with pure joy that makes my heart smile instantly. Every silly joke, every playful moment, every uncontrollable laugh we shared is a treasure I replay in my mind again and again 😂💖", 
    media: ["video7.mp4","video8.mp4","video13.mp4"] 
  },

  { 
    title: "Our Kisses 💋", 
    text: "Those moments when our lips met felt like time paused just for us. The world disappeared, the noise faded, and all I could feel was you — close, warm, and real. Each kiss carried emotions words could never fully explain… soft, deep, unforgettable. A spark that still lingers every time I think about it 💋🔥❤️", 
    media: ["photo33.jpeg","photo34.jpeg","photo36.jpeg"] 
  },

  { 
    title: "Silent Comfort", 
    text: "Even in silence, being with you felt complete. We didn’t always need words because our hearts understood each other effortlessly. Sitting beside you quietly felt peaceful, comforting, and deeply intimate in a way that only we could understand. That kind of silence is rare… and incredibly beautiful 🌙🤍", 
    media: ["photo35.jpeg","video11.mp4"] 
  },

  { 
    title: "Our Journey", 
    text: "Our journey hasn’t been perfect, but it has been beautifully real and full of meaning. Every smile, every challenge, every lesson has shaped something strong and precious between us. Through it all, we kept choosing each other — and that’s what makes our story so special. No matter where life takes us, this journey will always hold a piece of my heart forever ❤️✨", 
    media: ["video9.mp4"] 
  },
  { 
  title: " 1 years,2 month and 4days (431 aprox.) Days of Waiting 🤍", 
  text: "It’s been 431 days of loving you silently, deeply, endlessly. Through every single one of those days, my heart kept choosing you. I’ve been waiting for the moment you hug me tightly, look into my eyes, and whisper, ‘Now you’re totally mine… and I’m not going anywhere.’ I just want to feel your arms around me and know that I’m home — where I’ve always belonged 🤍✨", 
  media: [] 
}
]
function showMemorySurprise(){
  const container=document.getElementById("surpriseMemories");
  container.innerHTML="";
  surpriseContent.forEach(item=>{
    const div=document.createElement("div");
    div.className="card";
    div.style.margin="20px 0";
    
    let mediaHTML = "";
    item.media.forEach(src=>{
      if(src.endsWith(".mp4")) mediaHTML += `<video controls src="${src}"></video>`;
      else mediaHTML += `<img src="${src}">`;
    });

    div.innerHTML = `<h3>${item.title}</h3><p>${item.text}</p>${mediaHTML}`;
    container.appendChild(div);
  });
  container.style.display="block";
}

// ---------------- LOVE MESSAGE ----------------
function showLoveMessage(){ document.getElementById("loveMessage").style.display="block"; }
function saveMessage(){
  const msg=document.getElementById("personalMessage").value.trim();
  if(msg){
    localStorage.setItem("herLoveMessage", msg);
    displayMessage();
    alert("Your love message is saved! ❤️");
  } else { alert("Write something from your heart 💌"); }
}
function displayMessage(){
  const msg = localStorage.getItem("herLoveMessage");
  if(msg){ document.getElementById("messageDisplay").innerHTML = `<h3>Her Message 💖</h3><p>${msg}</p>`; document.getElementById("messageDisplay").style.display="block"; }
}

// ---------------- FINAL MESSAGE ----------------
function showFinal(){ document.getElementById("finalMessage").style.display="block"; }

// ---------------- FLOATING HEARTS ----------------
setInterval(()=>{
  const heart=document.createElement("div");
  heart.className="heart";
  heart.style.left=Math.random()*100+"vw";
  heart.innerHTML="❤️";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),6000);
},500);

// ---------------- SEND ANSWERS & SAVE ----------------
function sendAnswers(){
  const correctPassword="0913";
  const enteredPassword=prompt("Enter the secret password ❤️");
  if(enteredPassword!==correctPassword){ alert("Wrong password 💔 This love is protected!"); return; }

  let answersArray = [];
  memories.forEach((item,index)=>{
    const answer=document.getElementById("answer"+index).value || "No answer given";
    answersArray.push({ question: item.question, answer: answer });
  });

  // Save to localStorage
  localStorage.setItem("loveStoryAnswers", JSON.stringify(answersArray));
  displaySavedAnswers();

  document.getElementById("sendingOverlay").style.display="flex";
  setTimeout(()=>{
    document.getElementById("sendingOverlay").style.display="none";
    alert("Your love story answers are saved ❤️ Scroll down to see them!");
  }, 2000);
}

function displaySavedAnswers(){
  const saved = JSON.parse(localStorage.getItem("loveStoryAnswers"));
  if(!saved) return;

  let container = document.getElementById("answersDisplay");
  if(!container){
    container = document.createElement("div");
    container.id = "answersDisplay";
    container.className = "card";
    container.style.margin = "20px auto";
    document.body.appendChild(container);
  }

  let html = "<h2>Your Answers 💌</h2>";
  saved.forEach((item,index)=>{
    html += `<p><b>${index+1}. ${item.question}</b><br>${item.answer}</p><hr>`;
  });
  container.innerHTML = html;
}

// ---------------- LOAD PAGE ----------------
window.onload = () => {
  displaySavedAnswers();
  displayMessage();
};
</script>
</body>
</html>