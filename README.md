<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beaver Focus</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN"
        crossorigin="anonymous">
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Josefin+Sans&family=Vina+Sans&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Josefin Sans', sans-serif;
            text-align: center;
            margin: 50px;
            background-color: #FFF3BC;
        }

        #timer-container1 {
            align-items: center;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 20px;
            background-color: #accea0;
            width: 500px; /* Make the timer box square */
            min-height: 500px; /* Set a minimum height for the timer box */
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            align-items: center;
            margin: auto; /* Center the timer box */
        }

        #timer {
            font-size: 5em;
            margin: 0;
            color: #ffffff; /* White color */
            font-weight: bold; /* Bold font */
            padding: 0;
        }

        .btn-focus,
        .btn-break,
        .btn-long-break {
            font-size: 1em;
            padding: 10px 20px; /* Adjust padding for better alignment */
            margin: 10px; /* Adjust margin for better alignment */
            cursor: pointer;
            background-color: #5f3c2c;
            color: #accea0;
            border: none;
            border-radius: 20px;
            display: flex-top;
        }

        #startBtn,
        #pauseBtn,
        #resetBtn {
            font-size: 1em;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            background-color: #5f3c2c;
            color: #accea0;
            border: none;
            border-radius: 10px;
        }

        .container-fluid {
            padding: 0;
            /* Remove container padding */
        }

        .navbar {
            background-color: #FFF2BD;
        }

        .navbar-brand img {
            width: 100px;
            height: auto;
            margin-right: 10px;
        }

        .navbar-brand {
            font-size: 2rem; /* Adjust font size */
            font-weight: bold; /* Bold font */
            color: #5f3c2c;
            font-family: 'Fira Sans', sans-serif;
        }

        .jumbotron {
            text-align: center;
            margin-top: 20px;
        }

        .custom-btn {
            background-color: #5f3c2c;
            color: #accea0;
            border: none;
            padding: 10px 20px;
            margin-right: 10px;
            text-decoration: none;
            display: inline-block;
            font-size: 30px;
            cursor: pointer;
            border-radius: 5px;
        }

        @media (max-width: 767px) {
            .custom-btn {
                width: 100%;
                display: block;
                margin-bottom: 10px;
            }
        }

        .container1 {
            align-items: center;
            background-color: #accea0;
            width: 500px;
            /* Make the timer box square */
            min-height: 400px; /* Set a minimum height for the outer container */
            border-radius: 20px;
            margin-top: 10px;
            margin-bottom: 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            margin: auto;
            /* Center the outer container */
            font-size: 30px;

        }

        /* To-Do List Styling */
        #todo-container {
            background-color: #b43f2a;
            width: 600px; /* Extend the to-do box width */
            min-height: 90px; /* Extend the to-do box height */
            border: 2px dotted #ffffff;
            padding: 20px;
            margin: auto;
            margin-top: 20px;
            margin-bottom: 20px; /* Add a gap between timer and to-do list */
            position: relative;
            color: rgba(255, 255,255, 255, 255, 0.8);
            border-radius: 10px;
        }

        .add-todo-btn {
            background-color: #5f3c2c;
            color: #accea0;
            border: none;
            padding: 10px 20px;
            margin-right: 10px;
            text-decoration: none;
            display: inline-block;
            font-size: 30px;
            cursor: pointer;
            border-radius: 5px;
            position: absolute;
            top: 10px;
            right: 10px;
        }

        .todo-box {
            background-color: #b43f2a;
            min-height: 20px;
            border: 5px dotted #ffffff;
            padding: 10px;
            margin: 20px auto;
            position: relative;
            color: rgba(255, 255, 255, 0.8);
            border-radius: 5px;
        }

        .list-group-item {
            border: none;
        }

        .input-group {
            display: flex;
            align-items: center;
        }

        .form-control {
            flex: 1;
            margin-right: 10px;
        }

        /* Greenbox1 Styling */
        .green-box {
        background-color: #accea0;
 
		border-radius: 10px;
		margin: auto;
		margin-top: 80px;
		margin-right:175px; /* Adjusted margin-right */
		margin-left: 175px;
		display: flex;
		justify-content: flex-start; /* Align to the left */
		align-items: center;
		position: relative;
		}

        .image {
            width: 250px; /* Adjust the width of the image for smaller screens */
            margin-bottom: 20px; /* Add margin between the image and text */
            margin-left: 10px;
			align:left;
        }

        .greenbox1 {
            color: #5f3c2c; /* Brown color */
            text-align: right; /* Align text to the right */
        }

        .red-text {
            color: red;
            font-weight: bold;
            text-transform: uppercase;
        }

        /* Greenbox2 Styling */
        .green-box2 {
            background-color: #accea0; /* Green color */
            padding: 10px;
            border-radius: 10px;
            margin: auto;
            margin-top: 80px;
            display: flex;
            justify-content:center; /* Align to the right */
            align-items: center;
            position: relative;
			margin-right:10px;
			margin-left:10px;
        }

        .green-box2 {
            color: #5f3c2c; /* Brown color */
            text-align: left; /* Align text to the left */
        }

        @media (max-width: 767px) {
            .greenbox12 {
                flex-direction: column;
                align-items: center;
                text-align: right;
            }

            .image {
                width: 70%; /* Adjust the width of the image for smaller screens */
                margin-bottom: 20px; /* Add margin between the image and text */
            }
        }

        .icon {
            width: 3em; /* Set the size of the icon */
            height: auto;
            margin-right: 10px; /* Adjust margin for better alignment with text */
        }

        /* Additional Content Styling */
        .green-box3 {
            background-color: #accea0; /* Green color */
            padding: 30px;
            border-radius: 10px;
            margin: auto;
            margin-top: 80px;
			margin-right: 90px;
            margin-left: 90px;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
        }

        .question {
            color: #5f3c2c; /* Brown color */
            font-size: 2em;
            font-weight: bold;
            text-align: left; /* Align text to the left */
        }

        .question-highlight {
            color: red; /* Red color for highlighting */
        }

        .answer {
            color: #ffffff; /* White color */
            text-align: left; /* Align text to the left */
            margin-top: 20px;
        }

        .bridge-to-focus {
            color: #5f3c2c; /* Brown color */
            font-size: 2em;
            font-weight: bold;
            text-align: center; /* Align text to the center */
            margin-top: 20px;
        }

        /* Images and Subheadings */
        .image-container {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
        }

        .subheading {
            color: red; /* Red color for subheadings */
            margin-top: 10px;
            font-weight: bold;
        }
		/* Override Bootstrap Tooltip Styles */
        .tooltip {
          display: none !important;
        }
		.footer-link {
       color: #5f3c2c;
       text-decoration: none;
       margin: 0 5px;
       font-size: 18px;
        text-transform: uppercase;
         }

        .footer-link:hover {
        text-decoration: underline;
}


    </style>
</head>

<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">
                <img src="https://i.postimg.cc/kXBFQ2np/logo.png" alt="banner">
                Beaver Focus
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a href="about us.html" class="custom-btn">About Us</a>
                    </li>
                    <li class="nav-item">
                        <a href="settings.html" class="custom-btn" target="_blank">Settings</a>
                    </li>
                    <li class="nav-item">
                        <a href="login page.html" class="custom-btn">Login</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container1">
        <div id="timer-container1">
            <div class="row">
                <div class="col-sm-4">
                    <button class="btn btn-focus" onclick="setTimer(1500)">Focus</button>
                </div>
                <div class="col-sm-4">
                    <button class="btn btn-break" onclick="setTimer(300)">Short Break</button>
                </div>
                <div class="col-sm-4">
                    <button class="btn btn-long-break" onclick="setTimer(1800)">Long Break</button>
                </div>
            </div>
            <div id="timer" class="mb-4">25:00</div>
            <div class="row">
                <div class="col-sm-4">
                    <button id="startBtn" class="btn btn-primary" onclick="startTimer()">Start</button>
                </div>
                <div class="col-sm-4">
                    <button id="pauseBtn" class="btn btn-secondary" onclick="pauseTimer()" style="display:none;">Pause
                    </button>
                </div>
                <div class="col-sm-4">
                    <button id="resetBtn" class="btn btn-danger" onclick="resetTimer()" style="display:none;">Reset
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- To-Do List -->
    <div id="todo-container">
        <div class="add-todo-btn" onclick="addTodo()">+</div>
        <div id="todo-list" class="list-group" style="list-style-type: none; padding: 0;"></div>
    </div>

    <!-- Green Box -->
	<div class="green-box d-flex align-items-center">
		<img src="https://i.postimg.cc/nzrMyQw8/stick1.png" alt="Stick" class="image img-fluid">
		<div class="greenbox1 text-right">
			<h2>LIKE A BEAVER BUILDING ITS <span class="red-text">DAM,</span>FOCUS IS</h2>
			<h2><span class="red-text">THE FOUNDATION OF ACHIEVEMENT </span> </h2>
			<h2>ONE SMALL TASK AT A TIME</h2>
		</div>
	</div>
	
<!-- Green Box2 -->
<div class="green-box2 d-flex align-items-center">
    <div class="greenbox12">
        <div class="row">
            <div class="col-sm-1">
                <img src="https://i.postimg.cc/1t0PYRyx/time.png" alt="Time Icon" class="icon">
            </div>
            <div class="col-sm-11">
                <h2>25 MINUTE TIMER ON FOCUS MODE</h2>
            </div>
        </div>
		<br>
        <div class="row">
            <div class="col-sm-1">
                <img src="https://i.postimg.cc/8zFGgmTm/max.png" alt="Maximize Icon" class="icon">
            </div>
            <div class="col-sm-11">
                <h2>MAXIMIZE WORK WITHOUT DISTRACTIONS</h2>
            </div>
        </div>
		<br>
        <div class="row">
            <div class="col-sm-1">
                <img src="https://i.postimg.cc/15dxBVDn/tea-cup.png" alt="Time Icon" class="icon">
            </div>
            <div class="col-sm-11">
                <h2>SHORT BREAK AND LONG BREAK AFTER 4 CYCLES</h2>
            </div>
        </div>
    </div>
    <img src="https://i.postimg.cc/MTJqDf2b/stick0.png" alt="Stick" class="image img-fluid">
</div>
    <!-- ... (your existing HTML remains unchanged) ... -->

    <!-- Green Box3 -->
    <div class="green-box3">
        <div class="question">
            What is <span class="question-highlight">Beaver Focus</span>?
        </div>
        <div class="answer">
            Beaver Focus is a customizable timer that works on websites for users. The main aim of this app is to help
            you focus on any task you are working on, such as study, writing, or coding, and many more. This app is
            inspired by the Pomodoro Technique, which is a time management method developed by Francesco Cirillo.
        </div>
        <div class="bridge-to-focus">
            BUILD A BRIDGE TO FOCUS
        </div>
        <div class="image-container">
            <div>
                <img src="https://i.postimg.cc/QML2GL4j/stick3.png" alt="Stick 3" class="image img-fluid">
                <div class="subheading">FOCUS ON PRODUCTIVITY</div>
            </div>
            <div>
                <img src="https://i.postimg.cc/wMBPc9vQ/stick4.png" alt="Stick 4" class="image img-fluid">
                <div class="subheading">DISTRACTION CONTROL</div>
            </div>
            <div>
                <img src="https://i.postimg.cc/sgWLJ6Vq/stick5.png" alt="Stick 5" class="image img-fluid">
                <div class="subheading">SET GOAL AND TIMER</div>
            </div>
        </div>
    </div>
<!-- Footer -->
<footer class="text-center mt-5">
    <hr style="border-top: 2px solid #5f3c2c; width: 100%; margin-bottom: 30px;">

    <!-- Navigation Links -->
    <nav class="mb-3">
        <a href="#" class="footer-link">Home</a> |
        <a href="privacy.html" class="footer-link">Privacy</a> |
        <a href="terms.html" class="footer-link">Terms</a> |
        <a href="contact.html" class="footer-link">Contact</a>
    </nav>

    <!-- Icon Links -->
    <div>
        <a href="https://x.com" target="_blank" title="Visit x.com">
            <img src="https://i.postimg.cc/Zn07vj7f/X.png" alt="x Icon" class="icon img-fluid">
        </a>
        <a href="https://facebook.com" target="_blank" title="Visit Facebook">
            <img src="https://i.postimg.cc/yNPvf22Q/fb.png" alt="Facebook Icon" class="icon img-fluid">
        </a>
        <a href="https://instagram.com" target="_blank" title="Visit Instagram">
            <img src="https://i.postimg.cc/xdT4S0GD/insta.png" alt="Instagram Icon" class="icon img-fluid">
        </a>
    </div>

    <p class="mt-3">@beaverfocus 2023. All rights reserved.</p>
</footer>

    <script>
        let countdown;
        let timer = 1500; // 25 minutes in seconds
        let isPaused = false;

        function setTimer(seconds) {
            timer = seconds;
            displayTime(timer);
        }

        function startTimer() {
            clearInterval(countdown);

            if (isPaused) {
                isPaused = false;
            } else {
                countdown = setInterval(() => {
                    if (timer > 0 && !isPaused) {
                        timer--;
                        displayTime(timer);
                    } else {
                        clearInterval(countdown);
                    }
                }, 1000);
            }

            // Show pause and reset buttons
            document.getElementById('pauseBtn').style.display = 'inline-block';
            document.getElementById('resetBtn').style.display = 'inline-block';
            document.getElementById('startBtn').style.display = 'none';
        }

        function pauseTimer() {
            isPaused = !isPaused;

            if (isPaused) {
                clearInterval(countdown);
            } else {
                startTimer();
            }
        }

        function resetTimer() {
            clearInterval(countdown);
            timer = 1500; // Reset to 25 minutes in seconds
            displayTime(timer);
            isPaused = false;

            // Show start button, hide pause and reset buttons
            document.getElementById('startBtn').style.display = 'inline-block';
            document.getElementById('pauseBtn').style.display = 'none';
            document.getElementById('resetBtn').style.display = 'none';
        }

        function displayTime(seconds) {
            const minutes = Math.floor(seconds / 60);
            const remainderSeconds = seconds % 60;
            const display = `${minutes}:${remainderSeconds < 10 ? '0' : ''}${remainderSeconds}`;
            document.getElementById('timer').textContent = display;
        }

        // To-Do List Script
        function addTodo() {
            const todoContainer = document.getElementById('todo-list');
            const newTodo = document.createElement('div');
            newTodo.className = 'list-group-item todo-box';
            newTodo.innerHTML = `
                <div class="input-group">
                    <input type="text" class="form-control" placeholder="New To-Do">
                    <button class="btn btn-light" onclick="removeTodo(this)">-</button>
                </div>
            `;
            todoContainer.appendChild(newTodo);
        }

        function removeTodo(todoButton) {
            const todoItem = todoButton.parentElement.parentElement;
            todoItem.remove();
        }
    </script>

    <!-- ... (your HTML remains unchanged) ... -->

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
        crossorigin="anonymous"></script>
</body>

</html>
