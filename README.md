<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Narayan | Interactive Introduction</title>

<style>

/* =====================================================
   RESET
===================================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {

    font-family: Arial, sans-serif;

    background:
        radial-gradient(
            circle at 20% 20%,
            #151052 0%,
            #050816 35%,
            #02030b 100%
        );

    color: white;

    overflow-x: hidden;
}


/* =====================================================
   MOUSE GLOW
===================================================== */

.cursor-glow {

    position: fixed;

    width: 300px;
    height: 300px;

    border-radius: 50%;

    background:
        radial-gradient(
            circle,
            rgba(0, 255, 255, 0.12),
            transparent 70%
        );

    pointer-events: none;

    transform: translate(-50%, -50%);

    z-index: 0;

    transition:
        left 0.1s,
        top 0.1s;
}


/* =====================================================
   BACKGROUND BLOBS
===================================================== */

.blob {

    position: fixed;

    border-radius: 50%;

    filter: blur(100px);

    opacity: 0.35;

    z-index: -2;

    animation: blobMove 12s infinite alternate ease-in-out;
}

.blob.one {

    width: 400px;
    height: 400px;

    background: #6c5ce7;

    top: -150px;
    left: -100px;
}

.blob.two {

    width: 350px;
    height: 350px;

    background: #00cec9;

    right: -120px;
    top: 35%;

    animation-delay: 2s;
}

.blob.three {

    width: 300px;
    height: 300px;

    background: #fd79a8;

    bottom: -120px;
    left: 35%;

    animation-delay: 4s;
}

@keyframes blobMove {

    from {
        transform: translate(0, 0) scale(1);
    }

    to {
        transform: translate(80px, -60px) scale(1.2);
    }
}


/* =====================================================
   PARTICLES
===================================================== */

.particle {

    position: fixed;

    width: 3px;
    height: 3px;

    border-radius: 50%;

    background: white;

    opacity: 0.5;

    animation:
        particleFloat
        8s
        infinite
        ease-in-out;

    z-index: -1;
}

.p1 { left: 5%; top: 20%; }
.p2 { left: 15%; top: 70%; animation-delay: 2s; }
.p3 { left: 30%; top: 30%; animation-delay: 4s; }
.p4 { left: 45%; top: 80%; animation-delay: 1s; }
.p5 { left: 60%; top: 15%; animation-delay: 3s; }
.p6 { left: 75%; top: 65%; animation-delay: 5s; }
.p7 { left: 90%; top: 25%; animation-delay: 2s; }
.p8 { left: 80%; top: 85%; animation-delay: 6s; }
.p9 { left: 55%; top: 50%; animation-delay: 3s; }

@keyframes particleFloat {

    0%,100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-80px);
    }
}


/* =====================================================
   NAVBAR
===================================================== */

nav {

    width: 90%;

    max-width: 1200px;

    margin: 25px auto;

    padding: 15px 22px;

    border-radius: 20px;

    display: flex;

    justify-content: space-between;

    align-items: center;

    background:
        rgba(255,255,255,0.05);

    border:
        1px solid rgba(255,255,255,0.1);

    backdrop-filter: blur(15px);

    position: relative;

    z-index: 10;
}

.logo {

    font-size: 23px;

    font-weight: bold;

    letter-spacing: 2px;

    background:
        linear-gradient(
            90deg,
            #00ffff,
            #6c5ce7,
            #fd79a8
        );

    -webkit-background-clip: text;

    color: transparent;
}

.nav-status {

    display: flex;

    align-items: center;

    gap: 8px;

    color: #aaa;

    font-size: 13px;
}

.status-dot {

    width: 8px;
    height: 8px;

    border-radius: 50%;

    background: #00ff9d;

    box-shadow:
        0 0 12px #00ff9d;

    animation: blink 1.5s infinite;
}

@keyframes blink {

    50% {
        opacity: 0.3;
    }
}


/* =====================================================
   HERO
===================================================== */

.hero {

    width: 90%;

    max-width: 1200px;

    min-height: 82vh;

    margin: auto;

    display: flex;

    align-items: center;

    justify-content: space-between;

    gap: 70px;
}

.hero-left {

    flex: 1;

    position: relative;

    z-index: 2;
}

.hero-small {

    color: #00ffff;

    letter-spacing: 5px;

    font-size: 13px;

    margin-bottom: 20px;
}

h1 {

    font-size:
        clamp(55px, 8vw, 105px);

    line-height: 0.9;

    margin-bottom: 25px;
}

.gradient-name {

    background:
        linear-gradient(
            90deg,
            white,
            #00ffff,
            #6c5ce7,
            #fd79a8
        );

    background-size: 300%;

    -webkit-background-clip: text;

    color: transparent;

    animation:
        gradientMove
        5s
        infinite
        linear;
}

@keyframes gradientMove {

    0% {
        background-position: 0%;
    }

    50% {
        background-position: 100%;
    }

    100% {
        background-position: 0%;
    }
}


/* =====================================================
   TYPING
===================================================== */

.typing {

    font-size: 22px;

    margin-bottom: 25px;

    color: #aaa;
}

#typing {

    color: #00ffff;

    font-weight: bold;
}


/* =====================================================
   DESCRIPTION
===================================================== */

.description {

    max-width: 650px;

    color: #999;

    font-size: 17px;

    line-height: 1.9;
}

.highlight {

    color: #00ffff;

    font-weight: bold;
}


/* =====================================================
   BUTTONS
===================================================== */

.buttons {

    display: flex;

    gap: 15px;

    margin-top: 35px;

    flex-wrap: wrap;
}

button {

    padding:
        15px 27px;

    border-radius: 40px;

    font-weight: bold;

    font-size: 15px;

    cursor: pointer;

    transition:
        0.3s;

    font-family: inherit;
}

.primary {

    border: none;

    color: white;

    background:
        linear-gradient(
            90deg,
            #6c5ce7,
            #00cec9
        );

    box-shadow:
        0 0 25px
        rgba(0,206,201,0.3);
}

.primary:hover {

    transform:
        translateY(-5px)
        scale(1.05);

    box-shadow:
        0 0 45px
        rgba(0,206,201,0.5);
}

.secondary {

    color: white;

    background:
        rgba(255,255,255,0.04);

    border:
        1px solid #444;
}

.secondary:hover {

    border-color:
        #00ffff;

    transform:
        translateY(-5px);
}


/* =====================================================
   PROFILE ORB
===================================================== */

.hero-right {

    flex: 0.75;

    display: flex;

    justify-content: center;

    align-items: center;
}

.orbit {

    width: 360px;
    height: 360px;

    position: relative;

    display: flex;

    align-items: center;

    justify-content: center;
}

.orbit-ring {

    position: absolute;

    border-radius: 50%;

    border:
        1px solid
        rgba(0,255,255,0.5);

    animation:
        rotate
        10s
        linear
        infinite;
}

.ring-one {

    width: 360px;
    height: 360px;
}

.ring-two {

    width: 280px;
    height: 280px;

    border-color:
        rgba(108,92,231,0.6);

    animation-direction:
        reverse;

    animation-duration:
        7s;
}

.ring-three {

    width: 220px;
    height: 220px;

    border-color:
        rgba(253,121,168,0.5);

    animation-duration:
        5s;
}

@keyframes rotate {

    from {
        transform: rotate(0deg);
    }

    to {
        transform: rotate(360deg);
    }
}

.orb {

    width: 175px;
    height: 175px;

    border-radius: 50%;

    display: flex;

    justify-content: center;

    align-items: center;

    font-size: 75px;

    font-weight: bold;

    background:
        radial-gradient(
            circle at 30% 25%,
            #00ffff,
            #6c5ce7 45%,
            #17102f
        );

    box-shadow:
        0 0 50px #6c5ce7,
        0 0 100px rgba(0,255,255,0.3);

    animation:
        orbFloat
        3s
        infinite
        ease-in-out;

    z-index: 3;
}

@keyframes orbFloat {

    50% {
        transform:
            translateY(-12px)
            scale(1.04);
    }
}


/* =====================================================
   SCROLL INDICATOR
===================================================== */

.scroll-indicator {

    text-align: center;

    color: #555;

    font-size: 12px;

    letter-spacing: 3px;

    animation:
        bounce
        2s
        infinite;
}

@keyframes bounce {

    50% {
        transform:
            translateY(8px);
    }
}


/* =====================================================
   ABOUT SECTION
===================================================== */

#about {

    display: none;

    padding:
        120px 5%;

    min-height: 100vh;

    position: relative;
}

.section-heading {

    text-align: center;

    font-size:
        clamp(40px,6vw,70px);

    background:
        linear-gradient(
            90deg,
            #00ffff,
            #6c5ce7,
            #fd79a8
        );

    -webkit-background-clip: text;

    color: transparent;

    margin-bottom: 15px;
}

.section-sub {

    text-align: center;

    color: #777;

    margin-bottom: 70px;
}


/* =====================================================
   GLASS CARDS
===================================================== */

.about-grid {

    max-width: 1150px;

    margin: auto;

    display: grid;

    grid-template-columns:
        repeat(2,1fr);

    gap: 25px;
}

.about-card {

    padding: 35px;

    border-radius: 25px;

    background:
        linear-gradient(
            135deg,
            rgba(255,255,255,0.08),
            rgba(255,255,255,0.025)
        );

    border:
        1px solid
        rgba(255,255,255,0.12);

    backdrop-filter:
        blur(20px);

    position: relative;

    overflow: hidden;

    opacity: 0;

    transform:
        translateY(50px);

    transition:
        0.7s;
}

.about-card.show {

    opacity: 1;

    transform:
        translateY(0);
}

.about-card::before {

    content: "";

    position: absolute;

    width: 120px;
    height: 120px;

    background:
        #00ffff;

    filter:
        blur(80px);

    opacity: 0.08;

    right: -50px;

    top: -50px;
}

.about-card:hover {

    transform:
        translateY(-10px);

    border-color:
        rgba(0,255,255,0.5);

    box-shadow:
        0 20px 60px
        rgba(0,255,255,0.08);
}

.icon {

    font-size: 42px;

    margin-bottom: 20px;
}

.about-card h3 {

    font-size: 24px;

    margin-bottom: 15px;
}

.about-card p {

    color: #999;

    line-height: 1.8;
}


/* =====================================================
   STATS
===================================================== */

.stats {

    max-width: 1000px;

    margin:
        70px auto;

    display: grid;

    grid-template-columns:
        repeat(3,1fr);

    gap: 20px;
}

.stat {

    text-align: center;

    padding: 30px;

    border-radius: 20px;

    background:
        rgba(255,255,255,0.04);

    border:
        1px solid
        rgba(255,255,255,0.08);
}

.stat-number {

    font-size: 45px;

    font-weight: bold;

    color: #00ffff;

    margin-bottom: 8px;
}

.stat-label {

    color: #777;

    font-size: 13px;
}


/* =====================================================
   INTERESTS
===================================================== */

.interests {

    max-width: 1000px;

    margin: 90px auto;
}

.interests h2 {

    text-align: center;

    font-size: 35px;

    margin-bottom: 35px;
}

.tags {

    display: flex;

    justify-content: center;

    flex-wrap: wrap;

    gap: 15px;
}

.tag {

    padding:
        13px 20px;

    border-radius: 30px;

    background:
        rgba(108,92,231,0.12);

    border:
        1px solid
        rgba(108,92,231,0.4);

    color: #bbb;

    transition:
        0.3s;
}

.tag:hover {

    background:
        #6c5ce7;

    color: white;

    transform:
        translateY(-5px)
        scale(1.05);
}


/* =====================================================
   JOURNEY
===================================================== */

.journey {

    max-width: 850px;

    margin:
        100px auto;
}

.journey h2 {

    text-align: center;

    font-size: 35px;

    margin-bottom: 50px;
}

.timeline {

    border-left:
        2px solid
        #00ffff;

    padding-left: 35px;
}

.timeline-item {

    margin-bottom: 40px;

    position: relative;
}

.timeline-item::before {

    content: "";

    position: absolute;

    width: 13px;
    height: 13px;

    background:
        #00ffff;

    border-radius: 50%;

    left: -43px;

    top: 5px;

    box-shadow:
        0 0 18px #00ffff;
}

.timeline-item h3 {

    color:
        #00ffff;

    margin-bottom:
        8px;
}

.timeline-item p {

    color:
        #888;

    line-height:
        1.7;
}


/* =====================================================
   FOOTER
===================================================== */

footer {

    text-align: center;

    color: #555;

    padding:
        50px 0 20px;

    font-size:
        13px;
}


/* =====================================================
   RESPONSIVE
===================================================== */

@media(max-width:850px) {

    .hero {

        flex-direction:
            column;

        text-align:
            center;

        padding-top:
            70px;
    }

    .description {

        margin:
            auto;
    }

    .buttons {

        justify-content:
            center;
    }

    .hero-right {

        margin-top:
            50px;
    }

    .about-grid {

        grid-template-columns:
            1fr;
    }
}


@media(max-width:500px) {

    nav {

        width: 94%;
    }

    .nav-right {

        display:
            none;
    }

    .orbit {

        transform:
            scale(0.75);
    }

    .stats {

        grid-template-columns:
            1fr;
    }

    #about {

        padding:
            80px 5%;
    }
}

</style>

</head>


<body>


<!-- MOUSE LIGHT -->

<div class="cursor-glow"
     id="cursorGlow">
</div>


<!-- BACKGROUND -->

<div class="blob one"></div>
<div class="blob two"></div>
<div class="blob three"></div>


<!-- PARTICLES -->

<div class="particle p1"></div>
<div class="particle p2"></div>
<div class="particle p3"></div>
<div class="particle p4"></div>
<div class="particle p5"></div>
<div class="particle p6"></div>
<div class="particle p7"></div>
<div class="particle p8"></div>
<div class="particle p9"></div>


<!-- =====================================================
     NAVIGATION
===================================================== -->

<nav>

    <div class="logo">
        NARAYAN.
    </div>

    <div class="nav-status">

        <span class="status-dot"></span>

        Currently Learning & Exploring

    </div>

</nav>


<!-- =====================================================
     HERO
===================================================== -->

<section class="hero">


    <div class="hero-left">

        <div class="hero-small">
            HELLO, I'M
        </div>


        <h1>

            <span class="gradient-name">
                Narayan
            </span>

        </h1>


        <div class="typing">

            <span id="typing"></span>

        </div>


        <p class="description">

            I'm from
            <span class="highlight">
                Gaya, Bihar
            </span>

            and currently pursuing

            <span class="highlight">
                B.Tech in Computer Science Engineering
            </span>

            at

            <span class="highlight">
                Quantum University, Roorkee.
            </span>

            <br><br>

            I'm at the beginning of my college journey —
            curious, excited and ready to explore the world
            of technology.

        </p>


        <div class="buttons">

            <button
                class="primary"
                onclick="openAbout()">

                ✨ Discover Me

            </button>


            <button
                class="secondary"
                onclick="scrollToAbout()">

                ↓ Explore

            </button>

        </div>

    </div>


    <!-- ORB -->

    <div class="hero-right">

        <div class="orbit">

            <div class="orbit-ring ring-one"></div>

            <div class="orbit-ring ring-two"></div>

            <div class="orbit-ring ring-three"></div>

            <div class="orb">
                N
            </div>

        </div>

    </div>

</section>


<div class="scroll-indicator">

    SCROLL TO EXPLORE ↓

</div>


<!-- =====================================================
     ABOUT
===================================================== -->

<section id="about">


    <h2 class="section-heading">

        GET TO KNOW ME

    </h2>


    <p class="section-sub">

        A little more about the person behind the introduction.

    </p>


    <div class="about-grid">


        <!-- CARD 1 -->

        <div class="about-card">

            <div class="icon">
                🎓
            </div>

            <h3>
                My Education
            </h3>

            <p>

                I'm currently a
                <strong>
                    1st semester B.Tech CSE student
                </strong>
                at Quantum University, Roorkee.

                <br><br>

                I'm starting with the basics and looking
                forward to discovering different areas of
                computer science.

            </p>

        </div>


        <!-- CARD 2 -->

        <div class="about-card">

            <div class="icon">
                📍
            </div>

            <h3>
                Where I'm From
            </h3>

            <p>

                I come from
                <strong>
                    Gaya, Bihar
                </strong>.

                <br><br>

                College is a completely new chapter for me,
                giving me the opportunity to meet new people,
                experience new things and become more independent.

            </p>

        </div>


        <!-- CARD 3 -->

        <div class="about-card">

            <div class="icon">
                🎮
            </div>

            <h3>
                Outside the Classroom
            </h3>

            <p>

                When I'm not studying, I enjoy
                <strong>
                    gaming
                </strong>
                and exploring interesting things online.

                <br><br>

                I like discovering new technology and
                learning things that catch my attention.

            </p>

        </div>


        <!-- CARD 4 -->

        <div class="about-card">

            <div class="icon">
                🚀
            </div>

            <h3>
                My Ambition
            </h3>

            <p>

                I want to use my college years to develop
                useful skills and become better every day.

                <br><br>

                My long-term goal is to build a successful
                career in the technology field.

            </p>

        </div>

    </div>


    <!-- =================================================
         STATS
    ================================================= -->

    <div class="stats">

        <div class="stat">

            <div
                class="stat-number"
                data-target="1">

                0

            </div>

            <div class="stat-label">
                Semester Started
            </div>

        </div>


        <div class="stat">

            <div
                class="stat-number"
                data-target="1">

                0

            </div>

            <div class="stat-label">
                New Journey
            </div>

        </div>


        <div class="stat">

            <div
                class="stat-number"
                data-target="∞">

                0

            </div>

            <div class="stat-label">
                Things To Learn
            </div>

        </div>

    </div>


    <!-- =================================================
         INTERESTS
    ================================================= -->

    <div class="interests">

        <h2>
            ⚡ Things I Like
        </h2>


        <div class="tags">

            <div class="tag">
                💻 Technology
            </div>

            <div class="tag">
                🎮 Gaming
            </div>

            <div class="tag">
                👨‍💻 Programming
            </div>

            <div class="tag">
                🚀 New Technologies
            </div>

            <div class="tag">
                📚 Learning
            </div>

            <div class="tag">
                🌎 Exploring
            </div>

            <div class="tag">
                🎧 Music
            </div>

            <div class="tag">
                🤝 Meeting People
            </div>

        </div>

    </div>


    <!-- =================================================
         JOURNEY
    ================================================= -->

    <div class="journey">

        <h2>
            🧭 My Journey
        </h2>


        <div class="timeline">


            <div class="timeline-item">

                <h3>
                    📍 Gaya, Bihar
                </h3>

                <p>
                    This is where my journey began.
                </p>

            </div>


            <div class="timeline-item">

                <h3>
                    🎓 Started B.Tech CSE
                </h3>

                <p>

                    Joined Quantum University, Roorkee,
                    and started my Computer Science journey.

                </p>

            </div>


            <div class="timeline-item">

                <h3>
                    🌱 First Semester
                </h3>

                <p>

                    Learning the fundamentals, adapting to
                    college life and meeting new people.

                </p>

            </div>


            <div class="timeline-item">

                <h3>
                    🚀 What's Next?
                </h3>

                <p>

                    Learning new skills, exploring technology,
                    working on projects and seeing where this
                    journey takes me.

                </p>

            </div>

        </div>

    </div>


    <footer>

        Made with ❤️ by Narayan

        <br><br>

        B.Tech CSE • Quantum University, Roorkee

    </footer>

</section>


<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>


/* =====================================================
   MOUSE FOLLOW GLOW
===================================================== */

document.addEventListener(
    "mousemove",
    function(event) {

        const glow =
            document.getElementById(
                "cursorGlow"
            );

        glow.style.left =
            event.clientX + "px";

        glow.style.top =
            event.clientY + "px";

    }
);


/* =====================================================
   TYPING ANIMATION
===================================================== */

const words = [

    "Computer Science Student 💻",
    "Tech Enthusiast 🚀",
    "Gamer 🎮",
    "Future Developer 👨‍💻",
    "College Explorer 🌎"

];

let wordIndex = 0;

let letterIndex = 0;

let deleting = false;


function typeText() {

    const typing =
        document.getElementById(
            "typing"
        );

    const current =
        words[wordIndex];


    if (!deleting) {

        typing.textContent =
            current.substring(
                0,
                letterIndex + 1
            );

        letterIndex++;


        if (
            letterIndex ===
            current.length
        ) {

            deleting = true;

            setTimeout(
                typeText,
                1400
            );

            return;

        }

    }

    else {

        typing.textContent =
            current.substring(
                0,
                letterIndex - 1
            );

        letterIndex--;


        if (letterIndex === 0) {

            deleting = false;

            wordIndex++;

            if (
                wordIndex >=
                words.length
            ) {

                wordIndex = 0;

            }

        }

    }


    setTimeout(

        typeText,

        deleting ? 40 : 80

    );

}

typeText();


/* =====================================================
   OPEN ABOUT
===================================================== */

function openAbout() {

    const about =
        document.getElementById(
            "about"
        );

    about.style.display =
        "block";


    setTimeout(
        function() {

            about.scrollIntoView({
                behavior: "smooth"
            });


            const cards =
                document.querySelectorAll(
                    ".about-card"
                );


            cards.forEach(
                function(card, index) {

                    setTimeout(
                        function() {

                            card.classList.add(
                                "show"
                            );

                        },

                        index * 180
                    );

                }
            );


            animateStats();

        },

        100
    );

}


/* =====================================================
   EXPLORE BUTTON
===================================================== */

function scrollToAbout() {

    openAbout();

}


/* =====================================================
   ANIMATED STATS
===================================================== */

let statsAnimated = false;


function animateStats() {

    if (statsAnimated) {
        return;
    }

    statsAnimated = true;


    const numbers =
        document.querySelectorAll(
            ".stat-number"
        );


    numbers.forEach(
        function(number) {

            const target =
                number.dataset.target;


            if (target === "∞") {

                setTimeout(
                    function() {

                        number.textContent =
                            "∞";

                    },
                    800
                );

                return;

            }


            let current = 0;

            const final =
                parseInt(target);


            const interval =
                setInterval(
                    function() {

                        current++;

                        number.textContent =
                            current;


                        if (
                            current >=
                            final
                        ) {

                            clearInterval(
                                interval
                            );

                        }

                    },

                    400
                );

        }
    );

}

</script>


</body>
</html>

<!--
**narayanispro-creator/narayanispro-creator** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
