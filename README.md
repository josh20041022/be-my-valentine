# be-my-valentine
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: pink;
            color: white;
        }
        .container {
            margin-top: 100px;
        }
        h1 {
            font-size: 2em;
        }
        .heart {
            font-size: 50px;
            animation: heartbeat 1s infinite alternate;
        }
        @keyframes heartbeat {
            from { transform: scale(1); }
            to { transform: scale(1.2); }
        }
        .btn {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
        }
        .yes-btn {
            background-color: red;
            color: white;
        }
        .no-btn {
            background-color: white;
            color: red;
            position: absolute;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Will You Be My Valentine? 💖</h1>
        <span class="heart">❤️</span>
        <br><br>
        <button class="btn yes-btn" onclick="yesClick()">Yes</button>
        <button class="btn no-btn" onmouseover="moveButton()" onclick="moveButton()">No</button>
    </div>

    <script>
        function yesClick() {
            alert("YAMHUU YAMHU YAMHUU kimsh! 💕");
        }

        function moveButton() {
            let x = Math.random() * window.innerWidth * 0.8;
            let y = Math.random() * window.innerHeight * 0.8;
            document.querySelector(".no-btn").style.transform = `translate(${x}px, ${y}px)`;
        }
    </script>

</body>
</html>
