# studywith-ai
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Study with AI</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: url('img3.png') no-repeat center center fixed;
            background-size: cover;
            color: #ffffff;
            overflow-x: hidden;
        }
        header {
            background: linear-gradient(to right, #3a3a3a, #474747);
            color: rgb(255, 255, 255);
            padding: 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0px 4px 10px rgb(255, 255, 255);
        }
        .logo {
            display: flex;
            align-items: center;
        }
        .logo img {
            width: 50px;
            height: 50px;
            margin-right: 15px;
            border-radius: 50%;
        }
        .logo h1, .logo p {
            margin: 0;
        }
        .auth-links a {
            text-decoration: none;
            color: rgb(84, 82, 82);
            background: #ffffff;
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: bold;
            margin-left: 15px;
            transition: background-color 0.3s;
        }
        .auth-links a:hover {
            background: #ddd;
        }
        .container {
            text-align: center;
            padding: 50px;
        }
        .container h1 {
            font-size: 3em;
            color: #000000;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
        }
        .container p {
            font-size: 1.2em;
            max-width: 700px;
            margin: 20px auto;
            color: #000000;
        }
        .buttons a {
            text-decoration: none;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            color: rgb(0, 0, 0);
            padding: 15px 40px;
            margin: 15px;
            border-radius: 50px;
            font-size: 1.2em;
            display: inline-block;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0px 4px 8px rgba(63, 63, 63, 0.934);
        }
        .buttons a:hover {
            transform: translateY(-5px);
            box-shadow: 0px 8px 15px rgba(255, 255, 255, 0.916);
        }
        .section {
            padding: 50px;
            text-align: center;
            background: #f3f3f3;
            margin-top: 30px;
            border-radius: 10px;
        }
        .section h2 {
            font-size: 2.5em;
            color: #000000;
        }
        .section p {
            font-size: 1.2em;
            color: #000000;
        }
        input[type="text"] {
            padding: 10px;
            font-size: 1em;
            width: 60%;
            border-radius: 5px;
            border: 1px solid #000000;
            margin: 10px 0;
        }
        button {
            background: #ff7e5f;
            color: rgb(0, 0, 0);
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
            transition: background 0.3s;
        }
        button:hover {
            background: #d35400;
        }
        footer {
            background: #ffffff;
            color: rgb(0, 0, 0);
            text-align: center;
            padding: 15px 0;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <img src="img4.jpg" alt="Study with AI">
            <div>
                <h1>Study with AI</h1>
                <p>Your ultimate AI-powered student assistant</p>
            </div>
        </div>
        <div class="auth-links">
            <a href="login.html">Login</a>
            <a href="signup.html">Sign Up</a>
        </div>
    </header>

    <div class="container">
        <h1>Welcome to Study with AI</h1>
        <p>Explore tools to create presentations, complete homework, and get project ideas with the power of AI.</p>
        <div class="buttons">
            <a href="#create-ppt">Create PPT</a>
            <a href="#homework-helper">Homework Helper</a>
            <a href="#project-ideas">Project Ideas</a>
        </div>
    </div>

    <div id="create-ppt" class="section">
        <h2>Create PPT</h2>
        <p>Use AI to design professional presentations in minutes.</p>
        <input type="text" id="ppt-command" placeholder="Enter your PPT prompt...">
        <button id="generate-ppt">Generate PPT</button>
        <div id="ppt-result"></div>
    </div>

    <div id="homework-helper" class="section">
        <h2>Homework Helper</h2>
        <p>Get AI-powered assistance for your homework.</p>
        <input type="text" id="homework-command" placeholder="Enter your homework question...">
        <button id="generate-homework">Get Help</button>
        <div id="homework-result"></div>
    </div>

    <div id="project-ideas" class="section">
        <h2>Project Ideas</h2>
        <p>Find innovative project ideas tailored to your interests.</p>
        <input type="text" id="project-command" placeholder="Enter your interest...">
        <button id="generate-project">Generate Idea</button>
        <div id="project-result"></div>
    </div>

    <footer>
        <p>&copy; 2025 Study with AI. All rights reserved.</p>
    </footer>

    <script>
        window.onload = function() {
            document.getElementById('generate-ppt').onclick = function() {
                let prompt = document.getElementById('ppt-command').value;
                document.getElementById('ppt-result').innerHTML = "Generating a PowerPoint presentation based on: " + prompt;
            };

            document.getElementById('generate-homework').onclick = function() {
                let prompt = document.getElementById('homework-command').value;
                document.getElementById('homework-result').innerHTML = "Assisting with homework: " + prompt;
            };

            document.getElementById('generate-project').onclick = function() {
                let prompt = document.getElementById('project-command').value;
                document.getElementById('project-result').innerHTML = "Finding project ideas related to: " + prompt;
            };
            app.listen(8080, '0.0.0.0', () => {
                console.log('Server running on port 8080');
            });
        };
    </script>
</body>
</html>
