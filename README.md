<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Timeless Love Story</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(to bottom, #ffe6f2, #ffb3ba);
            color: #333;
            text-align: center;
            padding: 50px;
            margin: 0;
            overflow-x: hidden;
        }
        .container {
            max-width: 700px;
            margin: auto;
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            animation: fadeIn 2s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        h1 {
            color: #d32f2f;
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        .story {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 30px;
        }
        .photos {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 30px;
        }
        .photos img {
            width: 150px;
            height: 150px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .heart {
            font-size: 3em;
            color: #e91e63;
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        .quiz {
            margin-top: 30px;
        }
        .question {
            font-size: 20px;
            margin-bottom: 20px;
        }
        .options button {
            padding: 10px 20px;
            margin: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background: #f0f0f0;
        }
        .options button:hover {
            background: #ddd;
        }
        .buttons {
            margin-top: 30px;
            display: none; /* Hidden until quiz completes */
        }
        button {
            padding: 15px 30px;
            margin: 0 15px;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .yes {
            background: linear-gradient(45deg, #4CAF50, #66BB6A);
            color: white;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .yes:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
        }
        .no {
            background: linear-gradient(45deg, #f44336, #e57373);
            color: white;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .no:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
        }
        .message-form {
            margin-top: 30px;
            display: none; /* Show after answer */
        }
        .message-form textarea {
            width: 100%;
            height: 100px;
            padding: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .message-form button {
            margin-top: 10px;
            background: #2196F3;
            color: white;
        }
        .footer {
            margin-top: 40px;
            font-style: italic;
            color: #666;
        }
    </style>
    <script>
        let step = 0;
        const questions = [
            "What's the first thing that comes to mind when you think of us?",
            "If our love were a movie, what would the title be?",
            "What's one adventure we haven't had yet that you'd love to try together?",
            "How do you feel about spending every day with me forever?"
        ];

        function nextQuestion(answer) {
            step++;
            if (step < questions.length) {
                document.querySelector('.question').textContent = questions[step];
            } else {
                document.querySelector('.quiz').style.display = 'none';
                document.querySelector('.buttons').style.display = 'block';
            }
        }

        function handleYes() {
            alert('Forever starts now! I love you endlessly!');
            document.querySelector('.message-form').style.display = 'block';
        }

        function handleNo() {
            alert('Think of our beautiful future together? Let\'s try one more question!');
            step = 0; // Reset quiz for fun
            document.querySelector('.question').textContent = questions[0];
            document.querySelector('.quiz').style.display = 'block';
            document.querySelector('.buttons').style.display = 'none';
        }

        function sendMessage() {
            const message = document.querySelector('textarea').value;
            alert('Message sent! (As admin, you\'d see: ' + message + ')'); // Demo; in real site, send to backend
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>My Eternal Flame, Taiaba Tabassum Shital</h1>
        <div class="story">
            <p>In the quiet whispers of the night, under a canopy of stars that pale in comparison to your eyes, I found my forever. Every beat of my heart echoes your name, a symphony of love that knows no end.</p>
            <p>You've turned my world into a garden of roses, where every petal blooms with the promise of tomorrow. With you, I've discovered the true meaning of passion, tenderness, and unbreakable bonds.</p>
            <p>Today, as the sun sets on our shared dreams, I kneel before you—not just in body, but in soul. Will you join me in this grand adventure, hand in hand, heart to heart?</p>
            <p>And now, to make this moment even more magical, let's play a little game of love...</p>
        </div>
        <div class="photos">
            MyWebsite/
   index.html
   photo 1.jpg
   photo 2.jpg
   Photo 3.jpg

        </div>
        <div class="heart">❤️</div>
        <div class="quiz">
            <div class="question">What's the first thing that comes to mind when you think of us?</div>
            <div class="options">
                <button onclick="nextQuestion('answer')">Love</button>
                <button onclick="nextQuestion('answer')">Adventure</button>
                <button onclick="nextQuestion('answer')">Forever</button>
            </div>
        </div>
        <div class="buttons">
            <button class="yes" onclick="handleYes()">Yes, My Love!</button>
            <button class="no" onclick="handleNo()">No... But Maybe?</button>
        </div>
        <div class="message-form">
            <p>Leave me a follow-up message:</p>
            <textarea placeholder="Your thoughts..."></textarea>
            <button onclick="sendMessage()">Send</button>
        </div>
        <p class="footer">Add more photos, a playlist, or a video here to make it even more personal. Your love story deserves the spotlight!</p>
    </div>
</body>
</html>
