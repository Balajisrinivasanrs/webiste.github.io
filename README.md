<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Students</title>
    <style>
        body {
            font-family: cursive;
            background-color: #f0f0f0;
            background-image: url('svce.jpg');
            background-size: cover;
            background-repeat: no-repeat;
            background-position: center;
            background-attachment: fixed; /* Ensure the background image covers the page */
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        h2 {
            color: #dfe2e0;
            margin: 20px 10px;
            text-align: center;
            font-weight: bold;
            font-family: cursive;
            font-size: 16px;
            opacity: 0;
            animation: fadeIn 2s forwards 1s; /* Fade in effect */
        }

        h1 {
            text-align: center;
            margin: 80px 10px;
            font-size: 36px;
            animation: fadeInUp 2s forwards; /* Slide up and fade in effect */
            opacity: 0;
            position: relative; /* Ensure it's in the normal flow */
            z-index: 10; /* Bring it above other elements */
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes colorful-pop {
            0% {
                opacity: 0;
                transform: scale(0.8) rotate(-10deg);
                color: #ff6b6b;
            }
            25% {
                color: #4ecdc4;
            }
            50% {
                opacity: 1;
                transform: scale(1.2) rotate(5deg);
                color: #45b7d1;
            }
            75% {
                color: #ffa07a;
            }
            100% {
                opacity: 1;
                transform: scale(1) rotate(0);
                color: #B22222;
            }
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 100%;
            margin-top: 20px;
        }

        .subject-box {
            width: calc(100% - 30px);
            max-width: 200px;
            height: 150px;
            margin: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
            font-weight: bold;
            color: white;
            cursor: pointer;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            animation: slideIn 0.6s ease-out; /* Slide in animation */
        }

        .subject-box:hover {
            transform: scale(1.1) rotate(2deg); /* Slight rotation on hover */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Instagram Link Styles */
        .instagram-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: 20px;
            opacity: 0;
            animation: fadeInUp 2s forwards 1s; /* Fade in effect with delay */
        }

        .instagram-icon {
            width: 60px;
            height: 60px;
            transition: transform 0.3s ease;
        }

        .instagram-icon:hover {
            transform: scale(1.1);
        }

        .instagram-link {
            display: inline-block;
            text-decoration: none;
            margin-top: 10px;
        }

        .follow-text {
            font-size: 18px;
            font-weight: bold;
            color: #333;
            margin-bottom: 10px;
        }

        /* Media Query for Mobile Devices */
        @media (max-width: 600px) {
            .subject-box {
                font-size: 14px;
                height: 120px;
            }
            .instagram-icon {
                width: 25px;
                height: 25px;
            }
            .follow-text {
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <h1>GREETINGS!</h1>
    <h2>"Hi! This basic webpage is designed to understand the fundamentals of HTML, CSS, and JavaScript. Here, you can easily access our third-semester subject resources, including notes and question papers, by clicking on the desired subjects below, which will redirect you to the corresponding Google Drive folder."
    </h2>
    <div class="container">
        <div class="subject-box" style="background-color: #FF6B6B;" onclick="redirect('subject1')">Digital System Design</div>
        <div class="subject-box" style="background-color: #4ECDC4;" onclick="redirect('subject2')">Electronic Circuits</div>
        <div class="subject-box" style="background-color: #45B7D1;" onclick="redirect('subject3')">OOPS</div>
        <div class="subject-box" style="background-color: #FFA07A;" onclick="redirect('subject4')">Transforms & Random</div>
        <div class="subject-box" style="background-color: #98D8C8;" onclick="redirect('subject5')">EMF</div>
        <div class="subject-box" style="background-color: #F7B801;" onclick="redirect('subject6')">Signals and System</div>
    </div>
    
    <div class="instagram-container">
        <span class="follow-text">FOLLOW ME ON -> Click icon</span>
        <a href="https://www.instagram.com/your_username" target="_blank" class="instagram-link">
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram" class="instagram-icon">
        </a>
    </div>

    <script>
        function redirect(subject) {
            const links = {
                subject1: 'https://drive.google.com/drive/folders/1XHQkIHKfbYqm-ZuBWfTpgxSTTZBLjvck?usp=sharing',
                subject2: 'https://drive.google.com/drive/folders/15yhYltw_CS4AQlJRH5ZMbFYJLAYaR8-m?usp=sharing',
                subject3: 'https://drive.google.com/drive/folders/1S0h5qAv6OuHryUataiYw2_MzcemGd1wt?usp=sharing',
                subject4: 'https://drive.google.com/drive/folders/1lrBjd_Btt5N6Z2x3vlx13YWapEBVQmvu?usp=sharing',
                subject5: 'https://drive.google.com/drive/folders/13rzwP0nDofQLb6VOA4JBUmNJff8h2lAi?usp=sharing',
                subject6: 'https://drive.google.com/drive/folders/1hifaqaqgvViQPcnbfvzjjc_k8v07enPd?usp=sharing'
            };
            window.location.href = links[subject];
        }
    </script>
</body>
</html>
