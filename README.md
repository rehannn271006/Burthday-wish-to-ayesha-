<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Ayesha ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#030305;
    color:white;
    font-family:Poppins,sans-serif;
    overflow-x:hidden;
}

/* BACKGROUND */

body:before{
    content:"";
    position:fixed;
    inset:0;
    background:
    radial-gradient(circle at 20% 20%,rgba(255,70,130,.08),transparent 30%),
    radial-gradient(circle at 80% 70%,rgba(130,70,255,.06),transparent 30%);
    pointer-events:none;
    z-index:-2;
}

.stars{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:-1;
}

.star{
    position:absolute;
    width:2px;
    height:2px;
    background:white;
    border-radius:50%;
    animation:twinkle 3s infinite;
}

@keyframes twinkle{
    0%,100%{opacity:.15}
    50%{opacity:1}
}

/* INTRO */

section{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
}

.intro{
    text-align:center;
    padding:25px;
}

.intro small{
    letter-spacing:6px;
    color:#aaa;
    font-size:10px;
}

.intro h1{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(65px,15vw,140px);
    font-weight:500;
    line-height:.85;
    margin:30px 0;
}

.pink{
    color:#ff709d;
}

.intro p{
    color:#999;
    font-size:14px;
    margin-bottom:40px;
}

.btn{
    padding:15px 32px;
    border-radius:50px;
    border:1px solid rgba(255,255,255,.25);
    background:rgba(255,255,255,.05);
    color:white;
    cursor:pointer;
    transition:.4s;
    backdrop-filter:blur(15px);
}

.btn:hover{
    background:#ff5c91;
    transform:translateY(-4px);
    box-shadow:0 15px 40px rgba(255,60,130,.3);
}

/* LOCK */

#lock{
    display:none;
    padding:20px;
}

.lockbox{
    width:min(380px,100%);
    padding:35px 25px;
    text-align:center;
    border-radius:25px;
    background:rgba(255,255,255,.04);
    border:1px solid rgba(255,255,255,.1);
    backdrop-filter:blur(20px);
}

.lockbox h2{
    font-family:"Cormorant Garamond",serif;
    font-size:40px;
    margin:15px 0 5px;
}

.lockbox p{
    color:#888;
    font-size:12px;
    margin-bottom:25px;
}

.code{
    height:40px;
    font-size:24px;
    letter-spacing:8px;
    color:#ff709d;
}

.keypad{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:10px;
}

.key{
    height:55px;
    border-radius:15px;
    border:1px solid rgba(255,255,255,.1);
    background:rgba(255,255,255,.04);
    color:white;
    font-size:17px;
    cursor:pointer;
}

.key:hover{
    background:rgba(255,80,140,.2);
}

.error{
    color:#ff709d;
    font-size:11px;
    height:20px;
    margin-top:15px;
}

/* HERO */

#main{
    display:none;
}

.hero{
    text-align:center;
    padding:30px;
    background:
    radial-gradient(circle at center,rgba(255,60,130,.16),transparent 35%);
}

.hero small{
    letter-spacing:7px;
    color:#888;
    font-size:10px;
}

.hero h1{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(70px,16vw,150px);
    line-height:.75;
    font-weight:500;
    margin:35px 0;
}

.hero p{
    max-width:600px;
    color:#999;
    line-height:2;
    font-size:14px;
    margin:0 auto 35px;
}

/* MESSAGE */

.message{
    padding:70px 25px;
    text-align:center;
    background:linear-gradient(#030305,#090609);
}

.message-inner{
    max-width:750px;
}

.message h2{
    font-family:"Cormorant Garamond",serif;
    font-size:70px;
    font-weight:500;
    margin-bottom:35px;
}

.message p{
    color:#aaa;
    line-height:2.1;
    font-size:14px;
}

/* CINEMATIC PHOTOS */

.photos{
    padding:100px 0;
    display:block;
    background:#030305;
}

.photo-title{
    text-align:center;
    padding:0 20px 60px;
}

.photo-title small{
    letter-spacing:5px;
    color:#777;
    font-size:9px;
}

.photo-title h2{
    font-family:"Cormorant Garamond",serif;
    font-size:70px;
    font-weight:500;
    margin-top:10px;
}

/* Each photo fills most of screen */

.photo-scene{
    height:100vh;
    min-height:650px;
    position:relative;
    overflow:hidden;
    display:flex;
    align-items:flex-end;
    justify-content:center;
    margin-bottom:5px;
}

/* IMAGE */

.photo-image{
    position:absolute;
    inset:0;
    width:100%;
    height:100%;
    object-fit:cover;
    transform:scale(1.12);
    filter:brightness(.65);
    transition:
        transform 8s cubic-bezier(.2,.6,.2,1),
        filter 2s ease;
}

/* Cinematic image zoom when visible */

.photo-scene.visible .photo-image{
    transform:scale(1);
    filter:brightness(.72);
}

/* Dark cinematic gradient */

.photo-scene:after{
    content:"";
    position:absolute;
    inset:0;
    background:
    linear-gradient(
        to bottom,
        rgba(0,0,0,.15),
        transparent 40%,
        rgba(0,0,0,.85)
    );
    pointer-events:none;
}

/* LIGHT LEAK */

.photo-scene:before{
    content:"";
    position:absolute;
    width:350px;
    height:350px;
    border-radius:50%;
    background:rgba(255,90,150,.12);
    filter:blur(90px);
    top:10%;
    left:-100px;
    z-index:1;
    animation:lightmove 8s infinite alternate ease-in-out;
}

@keyframes lightmove{
    from{transform:translateX(0) translateY(0)}
    to{transform:translateX(80vw) translateY(40vh)}
}

/* CAPTION */

.photo-caption{
    position:relative;
    z-index:3;
    width:100%;
    padding:40px 25px 60px;
    text-align:center;
    transform:translateY(40px);
    opacity:0;
    transition:1.2s ease;
}

.photo-scene.visible .photo-caption{
    transform:translateY(0);
    opacity:1;
}

.photo-number{
    font-size:10px;
    letter-spacing:4px;
    color:#bbb;
}

.photo-caption h3{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(38px,8vw,70px);
    font-weight:500;
    margin:10px 0;
}

.photo-caption p{
    color:#bbb;
    font-size:12px;
}

/* FINAL */

.final{
    text-align:center;
    padding:30px;
    background:
    radial-gradient(circle,rgba(255,50,120,.18),transparent 40%);
}

.bigheart{
    font-size:85px;
    animation:heartbeat 1.5s infinite;
    margin-bottom:25px;
}

@keyframes heartbeat{
    0%,100%{transform:scale(1)}
    50%{transform:scale(1.15)}
}

.final h2{
    font-family:"Cormorant Garamond",serif;
    font-size:clamp(60px,13vw,120px);
    font-weight:500;
    line-height:.8;
}

.final p{
    color:#999;
    margin:30px auto;
    max-width:500px;
    line-height:1.8;
}

.signature{
    margin-top:70px;
    color:#666;
    font-family:"Cormorant Garamond",serif;
    font-size:23px;
}

/* HEARTS */

.heart{
    position:fixed;
    bottom:-30px;
    z-index:20;
    pointer-events:none;
    animation:float 5s linear forwards;
}

@keyframes float{
    0%{
        transform:translateY(0) scale(.5);
        opacity:0;
    }
    15%{opacity:1}
    100%{
        transform:translateY(-110vh) scale(1.4) rotate(30deg);
        opacity:0;
    }
}

/* MUSIC */

.music{
    position:fixed;
    right:18px;
    bottom:18px;
    width:45px;
    height:45px;
    border-radius:50%;
    border:1px solid rgba(255,255,255,.2);
    background:rgba(0,0,0,.5);
    color:white;
    z-index:50;
}

/* MOBILE */

@media(max-width:600px){

    .photo-scene{
        height:90vh;
        min-height:550px;
    }

    .photo-caption h3{
        font-size:45px;
    }

    .message h2,
    .photo-title h2{
        font-size:55px;
    }

}

</style>
</head>

<body>

<div class="stars" id="stars"></div>


<!-- INTRO -->

<section class="intro" id="intro">

    <div>

        <small>A LITTLE SURPRISE</small>

        <h1>
            For<br>
            <span class="pink">Ayesha</span>
        </h1>

        <p>
            I made something just for you ❤️
        </p>

        <button class="btn" onclick="start()">
            Start the Journey ✨
        </button>

    </div>

</section>


<!-- LOCK -->

<section id="lock">

    <div class="lockbox">

        <div style="font-size:45px">🔐</div>

        <h2>One little secret...</h2>

        <p>
            Enter the secret code to continue
        </p>

        <div class="code" id="code"></div>

        <div class="keypad">

            <button class="key" onclick="key('1')">1</button>
            <button class="key" onclick="key('2')">2</button>
            <button class="key" onclick="key('3')">3</button>

            <button class="key" onclick="key('4')">4</button>
            <button class="key" onclick="key('5')">5</button>
            <button class="key" onclick="key('6')">6</button>

            <button class="key" onclick="key('7')">7</button>
            <button class="key" onclick="key('8')">8</button>
            <button class="key" onclick="key('9')">9</button>

            <button class="key" onclick="back()">⌫</button>
            <button class="key" onclick="key('0')">0</button>
            <button class="key" onclick="check()">✓</button>

        </div>

        <div class="error" id="error"></div>

    </div>

</section>


<!-- MAIN -->

<div id="main">

    <!-- HERO -->

    <section class="hero">

        <div>

            <small>THE DAY YOU WERE BORN</small>

            <h1>
                Happy<br>
                <span class="pink">Birthday</span><br>
                Ayesha ❤️
            </h1>

            <p>
                Today isn't just another day.
                It's the day someone incredibly special came into this world.
            </p>

            <button class="btn"
            onclick="document.getElementById('message').scrollIntoView()">
                There's more ↓
            </button>

        </div>

    </section>


    <!-- MESSAGE -->

    <section class="message" id="message">

        <div class="message-inner">

            <h2>
                A message<br>
                <span class="pink">for you.</span>
            </h2>

            <p>

                Ayesha,<br><br>

                I hope this birthday brings you everything your heart wishes for.

                You deserve happiness, beautiful moments, genuine smiles,
                and people who truly appreciate you.

                <br><br>

                Some people enter our lives and somehow become
                a beautiful part of our memories.

                <br><br>

                Today is your day.

                Smile a little more.
                Dream a little bigger.
                And enjoy every second of it.

                <br><br>

                Happy Birthday, Ayesha. ❤️

            </p>

        </div>

    </section>


    <!-- CINEMATIC PHOTO SECTION -->

    <section class="photos">

        <div class="photo-title">

            <small>MEMORIES</small>

            <h2>Little Moments</h2>

        </div>


        <!-- PHOTO 1 -->

        <div class="photo-scene">

            <img
                src="photo1.jpg"
                class="photo-image"
                alt="Memory 1"
            >

            <div class="photo-caption">

                <div class="photo-number">01 / MEMORY</div>

                <h3>A beautiful moment.</h3>

                <p>
                    Some moments are worth remembering forever. ❤️
                </p>

            </div>

        </div>


        <!-- PHOTO 2 -->

        <div class="photo-scene">

            <img
                src="photo2.jpg"
                class="photo-image"
                alt="Memory 2"
            >

            <div class="photo-caption">

                <div class="photo-number">02 / MEMORY</div>

                <h3>That smile.</h3>

                <p>
                    A picture can hold a thousand memories.
                </p>

            </div>

        </div>


        <!-- PHOTO 3 -->

        <div class="photo-scene">

            <img
                src="photo3.jpg"
                class="photo-image"
                alt="Memory 3"
            >

            <div class="photo-caption">

                <div class="photo-number">03 / MEMORY</div>

                <h3>One for the memories.</h3>

                <p>
                    Some memories deserve their own little place.
                </p>

            </div>

        </div>


        <!-- PHOTO 4 -->

        <div class="photo-scene">

            <img
                src="photo4.jpg"
                class="photo-image"
                alt="Memory 4"
            >

            <div class="photo-caption">

                <div class="photo-number">04 / MEMORY</div>

                <h3>Forever special.</h3>

                <p>
                    Keep this moment close to your heart. 💗
                </p>

            </div>

        </div>

    </section>


    <!-- FINAL -->

    <section class="final">

        <div>

            <div class="bigheart">❤️</div>

            <h2>
                Happy Birthday<br>
                <span class="pink">Ayesha</span>
            </h2>

            <p>
                May this year bring you more happiness,
                more beautiful memories,
                and countless reasons to smile.
            </p>

            <button class="btn" onclick="surprise()">
                One Last Surprise 🎁
            </button>

            <div class="signature">
                Made with ❤️, just for you.
            </div>

        </div>

    </section>

</div>


<!-- MUSIC BUTTON -->

<button class="music" onclick="musicToggle()" id="musicBtn">
    ♫
</button>

<audio id="music" loop>
    <source src="music.mp3" type="audio/mpeg">
</audio>


<script>

/* STARS */

for(let i=0;i<150;i++){

    let s=document.createElement("div");

    s.className="star";

    s.style.left=Math.random()*100+"%";
    s.style.top=Math.random()*100+"%";

    s.style.animationDelay=Math.random()*4+"s";

    document.getElementById("stars").appendChild(s);

}


/* START */

function start(){

    document.getElementById("intro").style.display="none";

    document.getElementById("lock").style.display="flex";

    window.scrollTo(0,0);

}


/* PASSWORD */

let entered="";

function key(n){

    if(entered.length<6){

        entered+=n;

        document.getElementById("code").innerText=
        "•".repeat(entered.length);

    }

}

function back(){

    entered=entered.slice(0,-1);

    document.getElementById("code").innerText=
    "•".repeat(entered.length);

}

function check(){

    if(entered==="271006"){

        document.getElementById("lock").style.display="none";

        document.getElementById("main").style.display="block";

        window.scrollTo(0,0);

        hearts();

    }else{

        document.getElementById("error").innerText=
        "Try again, birthday girl ❤️";

        entered="";

        document.getElementById("code").innerText="";

    }

}


/* CINEMATIC SCROLL ANIMATION */

const observer=new IntersectionObserver(

    entries=>{

        entries.forEach(entry=>{

            if(entry.isIntersecting){

                entry.target.classList.add("visible");

            }

        });

    },

    {
        threshold:.35
    }

);

document.querySelectorAll(".photo-scene")
.forEach(scene=>observer.observe(scene));


/* PARALLAX */

window.addEventListener("scroll",()=>{

    document.querySelectorAll(".photo-scene").forEach(scene=>{

        const image=scene.querySelector(".photo-image");

        const rect=scene.getBoundingClientRect();

        const center=window.innerHeight/2;

        const distance=rect.top-center;

        const movement=distance*.035;

        image.style.transform=
        scene.classList.contains("visible")
        ? `scale(1.03) translateY(${movement}px)`
        : "scale(1.12)";

    });

});


/* HEARTS */

function hearts(){

    for(let i=0;i<35;i++){

        setTimeout(()=>{

            let h=document.createElement("div");

            h.className="heart";

            h.innerText=
            ["❤️","💗","💕","✨","💖"][Math.floor(Math.random()*5)];

            h.style.left=Math.random()*100+"%";

            h.style.fontSize=
            (12+Math.random()*25)+"px";

            h.style.animationDuration=
            (4+Math.random()*4)+"s";

            document.body.appendChild(h);

            setTimeout(()=>h.remove(),8000);

        },i*120);

    }

}


/* FINAL SURPRISE */

function surprise(){

    hearts();

    let screen=document.createElement("div");

    screen.style.position="fixed";
    screen.style.inset="0";
    screen.style.zIndex="999";
    screen.style.background="#030305";
    screen.style.display="flex";
    screen.style.alignItems="center";
    screen.style.justifyContent="center";
    screen.style.textAlign="center";

    screen.innerHTML=`

        <div style="animation:fadeUp 2s ease;padding:25px">

            <div style="
                font-size:90px;
                animation:heartbeat 1.5s infinite;
            ">
                ❤️
            </div>

            <div style="
                font-family:'Cormorant Garamond',serif;
                font-size:clamp(55px,12vw,110px);
                line-height:.8;
                margin-top:30px;
            ">
                Happy Birthday<br>
                <span style="color:#ff709d">
                    Ayesha
                </span>
            </div>

            <p style="
                color:#999;
                margin-top:35px;
                line-height:1.8;
            ">
                Keep smiling.<br>
                You deserve beautiful things. ❤️
            </p>

        </div>

    `;

    document.body.appendChild(screen);

}


/* MUSIC */

let playing=false;

function musicToggle(){

    let music=document.getElementById("music");

    if(!playing){

        music.play();

        playing=true;

        document.getElementById("musicBtn").innerText="🔊";

    }else{

        music.pause();

        playing=false;

        document.getElementById("musicBtn").innerText="♫";

    }

}

</script>

</body>
</html>
