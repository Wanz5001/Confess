<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hi Cinta</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin-top: 50px;
        }
        h1 {
            font-size: 40px; /* Tulisan besar sikit */
        }
        p {
            font-size: 20px; /* Tulisan kecik sikit */
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <h1>Hi Cinta</h1>
    <p>Awak suka saya tak?</p>
    <button id="yesButton">Ya</button>
    <button id="noButton">Tidak</button>

    <audio id="loveSong" class="hidden">
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Your browser does not support the audio tag.
    </audio>

    <img id="loveImage" src="https://images.app.goo.gl/TvpgX57idZuyWqAA7" alt="Gambar Cinta" class="hidden" />

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const loveSong = document.getElementById('loveSong');
        const loveImage = document.getElementById('loveImage');

        noButton.addEventListener('click', () => {
            alert("Dia lari!");
        });

        yesButton.addEventListener('click', () => {
            loveSong.classList.remove('hidden');
            loveSong.play();
            loveImage.classList.remove('hidden');
        });
    </script>

</body>
</html>
