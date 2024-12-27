<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dory's Website</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f8ff;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4682b4;
            color: white;
            padding: 1em;
            text-align: center;
        }
        nav {
            background-color: #333;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        nav a:hover {
            background-color: #575757;
            color: #fff;
        }
        main {
            padding: 2em;
        }
        section {
            margin-bottom: 2em;
        }
        footer {
            background-color: #4682b4;
            color: white;
            text-align: center;
            padding: 1em;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .button {
            background-color: #4682b4;
            border: none;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 12px;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #315f7d;
        }
        .highlight {
            background-color: #ffeb3b;
            padding: 5px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Dory's Website!</h1>
    </header>
    <nav>
        <a href="#about">About Dory</a>
        <a href="#adventures">Adventures</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <section id="about">
            <h2>About Dory</h2>
            <p>Dory is my beloved car, and this website is dedicated to sharing all the amazing adventures we've had together.</p>
        </section>
        <section id="adventures">
            <h2>Adventures</h2>
            <p>Here are some of the exciting places Dory and I have visited:</p>
            <ul>
                <li>Road trip to the mountains</li>
                <li>Beach getaway</li>
                <li>City exploration</li>
            </ul>
            <button class="button" onclick="showMoreAdventures()">See More Adventures</button>
            <div id="more-adventures" style="display:none;">
                <ul>
                    <li>Desert safari</li>
                    <li>Forest camping</li>
                    <li>Snowy mountains</li>
                </ul>
            </div>
        </section>
        <section id="contact">
            <h2>Contact</h2>
            <p>If you want to know more about Dory or share your own car adventures, feel free to reach out!</p>
            <form onsubmit="submitForm(event)">
                <label for="name">Name:</label><br>
                <input type="text" id="name" name="name" required><br>
                <label for="email">Email:</label><br>
                <input type="email" id="email" name="email" required><br>
                <label for="message">Message:</label><br>
                <textarea id="message" name="message" rows="4" cols="50" required></textarea><br>
                <input type="submit" value="Submit" class="button">
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Dory's Adventures</p>
    </footer>
    <script>
        function showMoreAdventures() {
            var moreAdventures = document.getElementById('more-adventures');
            if (moreAdventures.style.display === 'none') {
                moreAdventures.style.display = 'block';
            } else {
                moreAdventures.style.display = 'none';
            }
        }

        function submitForm(event) {
            event.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
        }
    </script>
</body>
</html>
