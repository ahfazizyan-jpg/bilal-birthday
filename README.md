<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For Bilal 🎂</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    min-height: 100vh;
    background: linear-gradient(135deg, #020024, #090979, #00d4ff);
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}

/* Floating lights */

.light {
    position: fixed;
    width: 6px;
    height: 6px;
    background: white;
    border-radius: 50%;
    opacity: 0.7;
    animation: float 5s infinite ease-in-out;
}

@keyframes float {
    0% {
        transform: translateY(100vh);
        opacity: 0;
    }

    50% {
        opacity: 1;
    }

    100% {
        transform: translateY(-10vh);
        opacity: 0;
    }
}

.container {
    width: 90%;
    max-width: 620px;
    padding: 40px 25px;
    text-align: center;

    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(255,255,255,0.25);

    border-radius: 25px;

    backdrop-filter: blur(12px);

    box-shadow: 0 0 45px rgba(0,212,255,0.35);

    z-index: 2;
}

/* Steps */

.step {
    display: none;
    animation: appear 0.8s ease;
}

.step.active {
    display: block;
}

@keyframes appear {

    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Text */

.emoji {
    font-size: 75px;
    margin-bottom: 20px;

    animation: bounce 1.5s infinite;
}

@keyframes bounce {

    50% {
        transform: translateY(-12px);
    }
}

h1 {
    font-size: 42px;
    margin-bottom: 20px;
}

h2 {
    font-size: 30px;
    margin-bottom: 20px;
}

p {
    font-size: 18px;
    line-height: 1.7;
    margin-bottom: 25px;
    color: #eeeeee;
}

.name {
    color: #61e8ff;

    text-shadow:
        0 0 10px #00d4ff,
        0 0 25px #00d4ff;
}

.big {
    font-size: 55px;
    font-weight: bold;

    color: #61e8ff;

    text-shadow:
        0 0 15px #00d4ff,
        0 0 35px #00d4ff;

    margin: 25px;
}

/* Button */

button {
    padding: 14px 30px;

    border: none;
    border-radius: 30px;

    background: linear-gradient(
        90deg,
        #00d4ff,
        #0077ff
    );

    color: white;

    font-size: 17px;

    cursor: pointer;

    transition: 0.3s;

    box-shadow: 0 5px 20px rgba(0,212,255,0.3);
}

button:hover {

    transform: scale(1.08);

    box-shadow:
        0 0 20px #00d4ff,
        0 0 40px #00d4ff;
}

/* Signature */

.signature {

    margin-top: 30px;

    color: #bdefff;

    font-style: italic;

    font-size: 17px;
}

/* Confetti */

.confetti {

    position: fixed;

    top: -30px;

    z-index: 10;

    animation:
        fall 4s linear forwards;
}

@keyframes fall {

    to {

        transform:
            translateY(110vh)
            rotate(720deg);

        opacity: 0;
    }
}

/* Heart */

.heart {

    font-size: 70px;

    animation:
        heartbeat 1s infinite;
}

@keyframes heartbeat {

    50% {
        transform: scale(1.2);
    }
}

</style>
</head>

<body>


<!-- Floating lights -->

<script>

for(let i = 0; i < 40; i++){

    const light =
        document.createElement("div");

    light.className = "light";

    light.style.left =
        Math.random() * 100 + "vw";

    light.style.animationDelay =
        Math.random() * 5 + "s";

    light.style.animationDuration =
        (3 + Math.random() * 5) + "s";

    document.body.appendChild(light);
}

</script>


<div class="container">


<!-- ================= STEP 1 ================= -->

<div class="step active" id="step1">

    <div class="emoji">🔐</div>

    <h1>ACCESS GRANTED?</h1>

    <p>

        Hey Bilal 👀

        <br><br>

        You have received a mysterious
        birthday message.

        <br><br>

        But there's one problem...

        <br>

        You have to unlock it first. 😏

    </p>

    <button onclick="nextStep(2)">

        Unlock 🔓

    </button>

</div>



<!-- ================= STEP 2 ================= -->

<div class="step" id="step2">

    <div class="emoji">🤔</div>

    <h2>Let's play a little game...</h2>

    <p>

        Someone was born on this very special day.

        <br><br>

        And today...

        <br>

        that person is getting older. 😂

        <br><br>

        Can you guess who?

    </p>

    <button onclick="nextStep(3)">

        Reveal the mystery 👀

    </button>

</div>



<!-- ================= STEP 3 ================= -->

<div class="step" id="step3">

    <div class="emoji">🎂</div>

    <h1>

        IT'S YOU!

        <br>

        <span class="name">

            BILAL

        </span>

    </h1>

    <div class="big">

        🎉 🎂 🎉

    </div>

    <p>

        HAPPY BIRTHDAY BRO! 🥳

        <br><br>

        Today is officially

        <strong>

            BILAL DAY! 😂

        </strong>

    </p>

    <button onclick="nextStep(4)">

        Continue → ✨

    </button>

</div>



<!-- ================= STEP 4 ================= -->

<div class="step" id="step4">

    <div class="heart">

        💙

    </div>

    <h2>

        A Birthday Wish For You

    </h2>

    <p>

        May this new year of your life
        bring you happiness, success,
        good health and countless
        unforgettable memories.

        <br><br>

        May you always have reasons
        to smile and people around you
        who genuinely care about you.

        <br><br>

        Keep enjoying life, bro! 😎

    </p>

    <button onclick="nextStep(5); celebrate()">

        There's one more thing... 👀

    </button>

</div>



<!-- ================= STEP 5 ================= -->

<div class="step" id="step5">

    <div class="emoji">

        💍❤️

    </div>

    <h2>

        And Finally...

    </h2>

    <p>

        I have one special wish for you. 😏

        <br><br>

        I hope that one day

        <strong>

            you and Laiba

        </strong>

        get married,

        if that's what you both want. ❤️

        <br><br>

        May your future be full of
        happiness, understanding,
        success and beautiful memories.

        ✨

    </p>

    <div class="signature">

        Once again...

        <br><br>

        <strong>

            🎂 HAPPY BIRTHDAY BILAL! 🎂

        </strong>

        <br><br>

        — Aanish 😎❤️

    </div>

</div>


</div>



<script>


/* =========================
   STEP CHANGER
========================= */

function nextStep(number){

    document
        .querySelectorAll(".step")
        .forEach(function(step){

            step.classList.remove("active");

        });

    document
        .getElementById("step" + number)
        .classList.add("active");
}



/* =========================
   BIRTHDAY CELEBRATION
========================= */

function celebrate(){

    const emojis = [

        "🎉",
        "🎊",
        "🎂",
        "🥳",
        "✨",
        "💙",
        "⭐",
        "🎈"

    ];

    for(let i = 0; i < 120; i++){

        const confetti =
            document.createElement("div");

        confetti.className =
            "confetti";

        confetti.innerHTML =
            emojis[
                Math.floor(
                    Math.random() *
                    emojis.length
                )
            ];

        confetti.style.left =
            Math.random() * 100 + "vw";

        confetti.style.fontSize =
            (15 + Math.random() * 25) + "px";

        confetti.style.animationDuration =
            (2 + Math.random() * 4) + "s";

        document.body.appendChild(
            confetti
        );

        setTimeout(function(){

            confetti.remove();

        }, 6000);

    }

}

</script>

</body>
</html>
