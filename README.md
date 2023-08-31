# Real-time-Character-Counter host link-: https://vivekpatel2903.github.io/Real-time-Character-Counter/
This is a simple HTML and JavaScript code that allows the user to Real-time-Character-Counter .
Step 1: Create the HTML file-
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Real-time Charater Counter</title>
    <link rel="stylesheet" href="style.css" />
</head>

<body>
    <div class="container">
        <h2>Real-time Charater Counter</h2>
        <textarea id="textarea" class="textarea" placeholder="Please write your text here..." maxlength="50"></textarea>
        <div class="counter-container">
            <p>
                Total Charaters:
                <span class="total-counter" id="total-counter"></span>
            </p>
            <p>
                Remaining:
                <span class="remaining-counter" id="remaining-counter"></span>
            </p>
        </div>
    </div>
    <script src="script.js"></script>
</body>

</html>

Step 2: Create the JavaScript file-
const textareaEl = document.getElementById("textarea");
const totalCounterEl = document.getElementById("total-counter");
const remainingCounterEl = document.getElementById("remaining-counter");

textareaEl.addEventListener("keyup", () => {
    updateCounter();
});

updateCounter()

function updateCounter() {
    totalCounterEl.innerText = textareaEl.value.length;
    remainingCounterEl.innerText =
        textareaEl.getAttribute("maxLength") - textareaEl.value.length;
}
Step 3: Create the CSS file-
body {
    margin: 0;
    display: flex;
    justify-content: center;
    height: 100vh;
    align-items: center;
    background-color: salmon;
    font-family: cursive;
}

.container {
    background-color: lightpink;
    width: 400px;
    padding: 20px;
    margin: 5px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
}

.textarea {
    resize: none;
    width: 100%;
    height: 100px;
    font-size: 18px;
    font-family: sans-serif;
    padding: 10px;
    box-sizing: border-box;
    border: solid 2px darkgray;
}

.counter-container {
    display: flex;
    justify-content: space-between;
    padding: 0 5px;
}

.counter-container p {
    font-size: 18px;
    color: gray;
}

.total-counter {
    color: slateblue;
}

.remaining-counter {
    color: orangered;
}
Step 3: Run the code.


