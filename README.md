# be-my-valentine
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: pink;
            overflow: hidden;
        }
        .container {
            text-align: center;
            position: relative;
            z-index: 2;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .yes-btn {
            background-color: #4CAF50;
            color: white;
        }
        .no-btn {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
        /* Fullscreen YouTube iframe (hidden by default) */
        .video-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: black;
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 3;
        }
        .video-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
    </style>
</head>
<body>

    <!-- YouTube Video Embed (Hidden Initially) -->
    <div class="video-container" id="videoContainer">
        <iframe id="youtubeVideo" src="" allow="autoplay"></iframe>
    </div>

    <!-- Main Content -->
    <div class="container" id="content">
        <h1>Will you be my Valentine? 💖</h1>
        <button class="yes-btn" onclick="playVideo()">Yes</button>
        <button class="no-btn" id="noButton" onmouseover="moveButton()">No</button>
    </div>

    <script>
        function playVideo() {
            document.getElementById('videoContainer').style.display = 'flex';
            document.getElementById('youtubeVideo').src = "https://www.youtube.com/embed/CXJJDxg7Mos?autoplay=1&mute=1";

            document.getElementById('content').style.display = 'none';
        }

        function moveButton() {
            let button = document.getElementById('noButton');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
    </script>

</body>
</html>
