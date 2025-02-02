# Samitha
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Riddle Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            text-align: center;
            padding: 50px;
        }

        .container {
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 500px;
            margin: auto;
        }

        h1 {
            color: #333;
        }

        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 15px 32px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 20px 0;
            cursor: pointer;
            border-radius: 5px;
        }

        button:hover {
            background-color: #45a049;
        }

        p {
            font-size: 18px;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to the Riddle Generator!</h1>
        <button id="riddleButton">Show me a riddle!</button>
        <p id="riddle"></p>
        <p id="answer"></p>
    </div>
    <script>
        const riddles = [
            { riddle: "What has keys but can't open locks?", answer: "A piano." },
            { riddle: "What has a head, a tail, is brown, and has no legs?", answer: "A penny." },
            { riddle: "What comes once in a minute, twice in a moment, but never in a thousand years?", answer: "The letter M." },
            { riddle: "I speak without a mouth and hear without ears. I have no body, but I come alive with the wind. What am I?", answer: "An echo." },
            { riddle: "What can travel around the world while staying in a corner?", answer: "A stamp." }
        ];

        document.getElementById('riddleButton').addEventListener('click', function() {
            const randomIndex = Math.floor(Math.random() * riddles.length);
            const riddle = riddles[randomIndex];
            document.getElementById('riddle').innerText = riddle.riddle;
            document.getElementById('answer').innerText = riddle.answer;
        });
    </script>
</body>
</html>
