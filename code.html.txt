<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tommy Question</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="container">
        <p>Can you send me a photo of Tommy?</p>
        <button id="yesButton">Yes</button>
        <button id="noButton">No</button>
    </div>
    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const catGifUrl = 'https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif';

        const noButtonTexts = [
            'Adichi saavedichiruve',
            'I miss Tommy',
            'Pleaseeee',
            'Cut panniruve',
            'Ungaluku vere vali iruku nenekiringelaa?',
            'Ungalukella manasatchiye illeya?',
            'Kalnenjakaare',
            'Yes'
        ];

        yesButton.addEventListener('click', () => {
            window.location.href = catGifUrl;
        });

        let noClickCount = 0;
        noButton.addEventListener('click', () => {
            if (noClickCount < noButtonTexts.length) {
                noButton.textContent = noButtonTexts[noClickCount];
                noClickCount++;
            }
            if (noClickCount === noButtonTexts.length) {
                yesButton.style.display = 'inline';
            }
        });
    </script>
</body>
</html>
