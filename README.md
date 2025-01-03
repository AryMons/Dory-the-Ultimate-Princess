<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dory's Adventures</title>
    <style>
        /* General Styles */
        body {
            font-family: 'Verdana', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to right, #001f54, #003366);
            color: #e4e4e4;
        }

        /* Header Styles */
        header {
            background: linear-gradient(to right, #003366, #004080);
            color: #ffffff;
            padding: 1.5em;
            text-align: center;
            font-size: 1.5em;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        /* Navigation Bar Styles */
        nav {
            background: #002244;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        nav a {
            float: left;
            display: block;
            color: #ffffff;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.4s, transform 0.3s;
        }

        nav a:hover {
            background-color: #004080;
            color: #e4e4e4;
            transform: scale(1.1);
        }

        /* Main Content Styles */
        main {
            padding: 2em;
        }

        section {
            margin-bottom: 2.5em;
            background: #003366;
            border-radius: 10px;
            padding: 1.5em;
            color: #ffffff;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        section h2 {
            color: #66ccff;
            margin-bottom: 0.5em;
        }

        section ul {
            list-style-type: square;
            padding-left: 1.5em;
        }

        /* Button Styles */
        .button {
            background-color: #66ccff;
            border: none;
            color: #002244;
            padding: 10px 25px;
            text-align: center;
            font-size: 16px;
            margin: 10px 0;
            cursor: pointer;
            border-radius: 12px;
            transition: all 0.3s;
        }

        .button:hover {
            background-color: #004080;
            color: #ffffff;
            transform: scale(1.1);
        }

        /* Highlight Text Styles */
        .highlight {
            background-color: #66ccff;
            padding: 5px;
            border-radius: 5px;
            color: #002244;
        }

        /* Footer Styles */
        footer {
            background: linear-gradient(to right, #003366, #004080);
            color: #ffffff;
            text-align: center;
            padding: 1em;
            position: fixed;
            width: 100%;
            bottom: 0;
            box-shadow: 0 -4px 6px rgba(0, 0, 0, 0.2);
        }

        /* Hidden Content */
        #more-adventures {
            display: none;
            animation: fadeIn 1s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Form Styles */
        form {
            margin-top: 1em;
        }

        form label {
            display: block;
            margin-top: 1em;
            font-weight: bold;
            color: #e4e4e4;
        }

        form input, form textarea {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #66ccff;
            border-radius: 5px;
            font-size: 14px;
            background: #002244;
            color: #e4e4e4;
        }

        form input:focus, form textarea:focus {
            outline: none;
            border-color: #66ccff;
        }

        form input[type="submit"] {
            width: auto;
            background: #66ccff;
            color: #002244;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }

        form input[type="submit"]:hover {
            background: #004080;
            color: #ffffff;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Dory the Ultimate Princess of Carkind!</h1>
    </header>
    <nav>
        <a href="#about">About Dory</a>
        <a href="#adventures">Adventures</a>
        <a href="#contact">Contact</a>
    </nav>
    <main>
        <section id="about">
            <h2>About Dory</h2>
            <p><span class="highlight">Dory</span> is THE untangible princess of all cars, and this website is dedicated to sharing all the amazing adventures she has and will go on with her parents: Madame Esranur and Sir Aryana!</p>
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
            <div id="more-adventures">
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
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>

                <input type="submit" value="Submit">
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Dory's Adventures</p>
    </footer>
    <script>
        function showMoreAdventures() {
            var moreAdventures = document.getElementById('more-adventures');
            moreAdventures.style.display = (moreAdventures.style.display === 'none' || moreAdventures.style.display === '') ? 'block' : 'none';
        }

        function submitForm(event) {
            event.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
        }
    </script>
</body>
</html>
