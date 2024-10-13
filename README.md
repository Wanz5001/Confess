<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Confession Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            background-color: #f0f8ff;
        }
        #buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
        }
        #noBtn {
            position: absolute;
        }
        .blushing-stickers {
            display: none;
            margin-top: 20px;
        }
        img {
            width: 100px;
            height: 100px;
        }
        /* Style for the YouTube iframe */
        #video {
            display: none; /* Initially hide the video */
            margin-top: 20px;
            max-width: 560px; /* Adjust width as needed */
        }
    </style>
</head>
<body>

<h1>Hi cinta, awak suka saya tak?</h1>

<div id="buttons">
    <button id="yesBtn">Ya</button>
    <button id="noBtn">Tidak</button>
</div>

<!-- Audio file -->
<audio id="song" src="content://media/external/downloads/18250"></audio>

<div class="blushing-stickers" id="stickers">
    <img src="https://example.com/blushing-sticker1.png" alt="Blushing Sticker 1">
    <img src="https://example.com/blushing-sticker2.png" alt="Blushing Sticker 2">
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const song = document.getElementById("song");
    const stickers = document.getElementById("stickers");

    noBtn.addEventListener('mouseover', function() {
        noBtn.style.top = `${Math.random() * window.innerHeight}px`;
        noBtn.style.left = `${Math.random() * window.innerWidth}px`;
    });

    yesBtn.addEventListener('click', function() {
        song.play(); // Play the audio file
        stickers.style.display = "block"; // Show blushing stickers
    });
</script>

</body>
</html>
