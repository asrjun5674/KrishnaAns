
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Krishna Answers</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, "Times New Roman", serif;
    background: linear-gradient(180deg, #dff5ff, #91d5f5);
    color: #174b70;
    text-align: center;
    display: flex;
    justify-content: center;
}

.container {
    width: 100%;
    max-width: 500px;
    padding: 30px 20px;
}

.om {
    font-size: 25px;
    color: #bf8b28;
    margin-bottom: 12px;
}

h1 {
    font-size: 32px;
    letter-spacing: 2px;
    margin: 10px 0;
}

.subtitle {
    font-size: 16px;
    line-height: 1.7;
    margin: 15px 0 24px;
}

.krishna-image {
    display: block;
    width: 100%;
    max-width: 300px;
    height: 300px;
    object-fit: cover;
    margin: 0 auto;
    border-radius: 20px;
    border: 4px solid #ffffff;
    box-shadow: 0 8px 25px #397fa344;
    cursor: pointer;
    transition: transform 0.25s;
}

.krishna-image:hover {
    transform: scale(1.025);
}

.instruction {
    font-size: 15px;
    margin: 18px 0;
}

.answer-box {
    min-height: 90px;
    padding: 20px;
    margin: 15px 0;
    border-radius: 15px;
    background: #ffffff99;
    border: 1px solid #ffffff;
}

.answer {
    font-size: 34px;
    font-weight: bold;
    letter-spacing: 3px;
}

.answer:empty {
    display: none;
}

.reset-button {
    margin-top: 20px;
    padding: 13px 38px;
    border: none;
    border-radius: 30px;
    background: #176da0;
    color: white;
    font-size: 16px;
    letter-spacing: 1px;
    cursor: pointer;
}

.reset-button:hover {
    background: #10547e;
}

.footer {
    margin-top: 30px;
    font-size: 14px;
    color: #376b89;
}
</style>
</head>

<body>
<main class="container">

    <div class="om">॥ ॐ ॥</div>

    <h1>KRISHNA ANSWERS</h1>

    <p class="subtitle">
        Close your eyes, think of your question,<br>
        remember Lord Krishna and click His image.
    </p>

    <!-- Replace the image URL below with your preferred
         Lord Krishna image if desired. -->
    <img
        id="krishna"
        class="krishna-image"
        src="https://images.unsplash.com/photo-1604608672516-7d4b9a1c9e3b?auto=format&fit=crop&w=700&q=85"
        alt="Lord Krishna"
        title="Click for Krishna's answer"
        onclick="getAnswer()"
    >

    <p class="instruction">🙏 Click Lord Krishna's image for your answer 🙏</p>

    <div class="answer-box" aria-live="polite">
        <div id="answer" class="answer"></div>
        <div id="message"></div>
    </div>

    <button class="reset-button" onclick="resetAnswer()">
        ↻ RESET
    </button>

    <div class="footer">
        Hare Krishna • Hare Krishna<br>
        Krishna Krishna • Hare Hare
    </div>

</main>

<script>
function getAnswer() {
    const answers = ["YES", "NO", "WAIT"];
    const result = answers[Math.floor(Math.random() * answers.length)];

    const answerElement = document.getElementById("answer");
    const messageElement = document.getElementById("message");

    answerElement.textContent = result;

    const colors = {
        YES: "#16834a",
        NO: "#c0392b",
        WAIT: "#b17b12"
    };

    const messages = {
        YES: "Proceed with faith and a thoughtful heart.",
        NO: "Pause and consider another path.",
        WAIT: "Be patient. Give the situation more time."
    };

    answerElement.style.color = colors[result];
    messageElement.textContent = messages[result];
}

function resetAnswer() {
    document.getElementById("answer").textContent = "";
    document.getElementById("message").textContent = "";
}
</script>

</body>
</html>
