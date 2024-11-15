<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I Love You</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100vh;
            background: linear-gradient(to right, #ffecd2 0%, #fcb69f 100%);
            font-family: 'Courier New', Courier, monospace;
            margin: 0;
            overflow: hidden;
            position: relative;
        }
        h1 {
            color: #ffffff;
            font-size: 4em;
            text-shadow: 2px 2px #f46b45;
            animation: fadeIn 3s ease-in-out infinite alternate, float 6s ease-in-out infinite;
            position: relative;
            margin-bottom: 20px;
        }
        p {
            color: #ffffff;
            font-size: 1.5em;
            margin-bottom: 20px;
            position: absolute;
            bottom: 20%;
            text-align: center;
        }
        button {
            padding: 10px 20px;
            font-size: 1.2em;
            color: #ffffff;
            background-color: #f46b45;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            animation: pulse 2s infinite;
            margin: 5px;
        }
        button:hover {
            background-color: #ff6347;
        }
        @keyframes fadeIn {
            0% {
                opacity: 0.5;
            }
            100% {
                opacity: 1;
            }
        }
        @keyframes float {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
            100% {
                transform: translateY(0);
            }
        }
        @keyframes heartBeat {
            0%, 100% {
                transform: scale(1) rotate(45deg);
            }
            50% {
                transform: scale(1.2) rotate(45deg);
            }
        }
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
            100% {
                transform: scale(1);
            }
        }
        .heart {
            position: absolute;
            width: 100px;
            height: 90px;
            background: #ff69b4;
            left: 50%;
            top: 30%;
            transform: translate(-50%, -50%) rotate(45deg);
            animation: heartBeat 1.5s ease-in-out infinite;
        }
        .heart::before, .heart::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 100px;
            background: #ff69b4;
            border-radius: 50%;
        }
        .heart::before {
            top: -50px;
            left: 0;
        }
        .heart::after {
            left: 50px;
            top: 0;
        }
    </style>
</head>
<body>
    <div class="heart"></div>
    <h1>I Love You!</h1>
    <p>Do you like me too?</p>
    <div style="position: absolute; bottom: 5%;">
        <button onclick="alert('Yay! She likes you! 💖')">Yes, I like you!</button>
        <button onclick="alert('Aww, she\'ll come around! 😊')">No, not yet...</button>
    </div>
</body>
</html>

