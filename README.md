<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Be My Valentine ❤️</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff4e8a, #ff9eb5);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    overflow: hidden;
}

.container {
    text-align: center;
    color: white;
}

.heart {
    font-size: 80px;
    animation: beat 1s infinite;
}

@keyframes beat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
}

h1 {
    margin: 20px 0;
}

button {
    padding: 12px 25px;
    font-size: 18px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    margin: 10px;
    transition: 0.3s;
}

#yesBtn {
    background-color: white;
    color: #ff4e8a;
}

#yesBtn:hover {
    background-color: #ffe6ee;
}

#noBtn {
    background-color: #333;
    color: white;
    position: absolute;
}
</style>
</head>

<body>

<div class="container">
    <div class="heart">❤️</div>
    <h1 id="question">Will you be my Valentine?</h1>
    <button id="yesBtn">Yes 💖</button>
    <button id="noBtn">No 😢</button>
</div>

<script>
const yesBtn = document.getElementById("yesBtn");
const noBtn = document.getElementById("noBtn");
const question = document.getElementById("question");

yesBtn.addEventListener("click", () => {
    question.innerHTML = "I love you so much 💕";
    yesBtn.style.display = "none";
    noBtn.style.display = "none";
});

noBtn.addEventListener("mouseover", () => {
    moveButton();
});

noBtn.addEventListener("click", (e) => {
    e.preventDefault();
    moveButton();
});

function moveButton() {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}
</script>

</body>
</html>
