<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ruba Osama</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* Basic Reset & Font */
        body {
            margin: 0;
            font-family: 'Inter', sans-serif;
            background-color: #fce4ec; /* Light Pink Background */
            color: #4a148c; /* Dark Purple Text */
            line-height: 1.6;
            padding: 20px;
        }

        /* Container for content */
        .container {
            max-width: 900px;
            margin: 20px auto;
            background-color: #fff8fd; /* Very Light Pink/Off-white for content areas */
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
        }

        /* Header Styling */
        header {
            text-align: center;
            padding-bottom: 20px;
            border-bottom: 2px solid #f8bbd0; /* Medium Pink Border */
            margin-bottom: 30px;
        }

        header h1 {
            color: #e91e63; /* Bright Pink for Name */
            font-size: 2.8em;
            margin-bottom: 5px;
        }

        header p {
            color: #880e4f; /* Darker Pink for Title */
            font-size: 1.2em;
            font-weight: 300;
        }

        /* Navigation Menu */
        nav {
            background-color: #f8bbd0; /* Medium Pink for nav background */
            padding: 10px 0;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
            flex-wrap: wrap; /* Allow items to wrap on smaller screens */
        }

        nav ul li {
            margin: 5px 15px;
            position: relative;
        }

        /* Standard menu items */
        nav ul li a {
            text-decoration: none;
            color: #880e4f; /* Darker Pink for nav links */
            font-weight: 700;
            font-size: 1.1em;
            padding: 8px 15px; /* Standard padding */
            border-radius: 20px; /* Rounded corners for buttons */
            transition: background-color 0.3s ease, color 0.3s ease;
            display: inline-block; /* Ensure padding and border-radius apply */
        }

        /* Remove heart shape pseudo-elements */
        nav ul li a::before,
        nav ul li a::after {
            content: none; /* Remove pseudo-elements */
        }

        nav ul li a:hover {
            background-color: #e91e63; /* Bright Pink on hover */
            color: #fff; /* White text on hover */
        }

        /* Section Styling */
        section {
            margin-bottom: 40px;
            padding: 20px;
            background-color: #fff; /* White background for sections */
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
        }

        section h2 {
            color: #ad1457; /* Raspberry Pink for Section Titles */
            font-size: 2em;
            margin-bottom: 15px;
            text-align: center;
        }

        /* About Me Section */
        .about-me {
            display: flex;
            flex-direction: column; /* Stack on small screens */
            align-items: center;
            gap: 20px;
            text-align: center;
        }

        .about-me img {
            width: 180px;
            height: 180px;
            border-radius: 50%; /* Circular image */
            object-fit: cover;
            border: 5px solid #f48fb1; /* Pink border around image */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        .about-me p {
            max-width: 600px;
            font-size: 1.1em;
            color: #6a1b9a; /* Purple for text */
        }

        /* Experience, Education, Skills Lists */
        ul {
            list-style: none; /* No default bullets */
            padding: 0;
            text-align: center;
        }

        ul li {
            background-color: #fce4ec; /* Light pink background for list items */
            margin-bottom: 10px;
            padding: 12px 20px;
            border-radius: 8px;
            border-left: 5px solid #f48fb1; /* Pink accent on the left */
            color: #4a148c;
            font-weight: 400;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.08);
        }

        ul li strong {
            color: #ad1457; /* Raspberry Pink for important text */
        }

        /* Portfolio/Projects Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Responsive grid */
            gap: 25px;
            justify-content: center;
        }

        .portfolio-item {
            background-color: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: transform 0.2s ease-in-out;
        }

        .portfolio-item:hover {
            transform: translateY(-5px);
        }

        .portfolio-item img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-bottom: 3px solid #f8bbd0;
        }

        .portfolio-item h3 {
            color: #ad1457;
            font-size: 1.3em;
            margin: 15px 0 5px;
        }

        .portfolio-item p {
            color: #6a1b9a;
            font-size: 0.95em;
            padding: 0 15px 15px;
        }

        /* Contact Section */
        .contact-info {
            text-align: center;
            margin-bottom: 30px;
        }

        .contact-info p {
            font-size: 1.1em;
            margin-bottom: 10px;
        }

        .contact-info a {
            color: #e91e63; /* Bright Pink for links */
            text-decoration: none;
            font-weight: 700;
            transition: color 0.2s ease;
        }

        .contact-info a:hover {
            color: #ad1457; /* Darker pink on hover */
        }

        .social-links {
            margin-top: 20px;
        }

        .social-links a {
            display: inline-block;
            margin: 0 10px;
            font-size: 2em;
            color: #f48fb1; /* Light Pink for social icons */
            transition: transform 0.2s ease;
        }

        .social-links a:hover {
            transform: scale(1.1);
            color: #e91e63; /* Bright pink on hover */
        }

        /* Contact Form Styling */
        .contact-form {
            max-width: 500px;
            margin: 0 auto;
            padding: 25px;
            background-color: #fff8fd; /* Very Light Pink for form background */
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
        }

        .contact-form label {
            display: block;
            margin-bottom: 8px;
            color: #ad1457; /* Raspberry Pink for labels */
            font-weight: 600;
            text-align: left;
        }

        .contact-form input[type="text"],
        .contact-form input[type="email"],
        .contact-form textarea {
            width: calc(100% - 20px); /* Adjust for padding */
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #f8bbd0; /* Medium Pink border */
            border-radius: 8px;
            font-family: 'Inter', sans-serif;
            font-size: 1em;
            color: #4a148c;
            background-color: #fff;
        }

        .contact-form textarea {
            resize: vertical; /* Allow vertical resizing */
            min-height: 100px;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #e91e63; /* Bright Pink on focus */
            box-shadow: 0 0 0 3px rgba(233, 30, 99, 0.2); /* Soft pink glow on focus */
        }

        .contact-form button {
            background-color: #e91e63; /* Bright Pink button */
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            font-size: 1.1em;
            font-weight: 700;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 10px rgba(233, 30, 99, 0.3);
        }

        .contact-form button:hover {
            background-color: #ad1457; /* Darker pink on hover */
            transform: translateY(-2px);
        }


        /* Footer Styling */
        footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid #f8bbd0;
            color: #880e4f;
            font-size: 0.9em;
        }

        /* Responsive Adjustments */
        @media (min-width: 768px) {
            .about-me {
                flex-direction: row; /* Row layout on larger screens */
                text-align: left;
            }

            .about-me div {
                flex: 1;
            }

            .about-me img {
                margin-right: 30px;
            }
        }

        @media (max-width: 600px) {
            body {
                padding: 10px;
            }

            .container {
                padding: 20px;
                margin: 10px auto;
            }

            header h1 {
                font-size: 2em;
            }

            header p {
                font-size: 1em;
            }

            section h2 {
                font-size: 1.6em;
            }

            .portfolio-grid {
                grid-template-columns: 1fr; /* Single column on very small screens */
            }

            nav ul {
                flex-direction: column; /* Stack nav items vertically on small screens */
            }

            nav ul li {
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🌸 Ruba Osama 🌸</h1>
            <p>Aspiring Web Designer & Creative Enthusiast</p>
        </header>

        <nav>
            <ul>
                <li><a href="#about">About Me</a></li>
                <li><a href="#experience">Work Experience</a></li>
                <li><a href="#portfolio">My Work</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

        <section id="about" class="about-me">
            <img src="https://raw.githubusercontent.com/rubaosama/ruba_osama/main/picrew%20icon%20_3.jpg" alt="Ruba Osama's Profile Picture">
            <div>
                <h2>About Me</h2>
                <p>Hello! I'm Ruba, a passionate beginner in the world of web design, eager to create beautiful and functional online spaces. I love bringing ideas to life with a touch of sparkle and creativity. When I'm not coding, you can find me sketching, reading, or exploring new cafes!</p>
                <p>I'm currently looking for opportunities to grow my skills and contribute to exciting projects. Let's create something wonderful together!</p>
            </div>
        </section>

        <section id="experience">
            <h2>Experience</h2>
            <ul>
                <li><strong>Junior Web Intern</strong> | Creative Spark Agency | Jan 2024 - Present
                    <br>Assisted with front-end development tasks, learned basic HTML, CSS, and JavaScript.</li>
                <li><strong>Volunteer Graphic Designer</strong> | Local Community Center | Sep 2023 - Dec 2023
                    <br>Created flyers and social media graphics for various events.</li>
            </ul>
        </section>

        <section id="education">
            <h2>Education</h2>
            <ul>
                <li><strong>Certificate in Web Development Basics</strong> | Online Coding Academy | 2023
                    <br>Completed courses in HTML5, CSS3, and responsive design principles.</li>
                <li><strong>High School Diploma</strong> | Blossom Valley High School | 2022</li>
            </ul>
        </section>

        <section id="skills">
            <h2>Skills</h2>
            <ul>
                <li><strong>Web Development:</strong> HTML, CSS, Basic JavaScript</li>
                <li><strong>Design Tools:</b> Canva, Figma (beginner)</li>
                <li><strong>Soft Skills:</strong> Creativity, Problem-Solving, Quick Learner, Teamwork</li>
            </ul>
        </section>

        <section id="portfolio">
            <h2>My Projects</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://raw.githubusercontent.com/rubaosama/ruba_osama/main/%F0%9F%A7%A0.jpg" onerror="this.onerror=null;this.src='https://placehold.co/300x180/f8bbd0/4a148c?text=Boutique+App';" alt="Project 1 Thumbnail: Boutique App">
                    <h3>Shopping Boutique</h3>
                    <p>A simple, responsive landing page for a fictional boutique, showcasing basic CSS layout techniques.</p>
                </div>
                <div class="portfolio-item">
                    <img src="https://raw.githubusercontent.com/rubaosama/ruba_osama/main/Recetas%20ilustradas%2C%20por%20Cartoon%20cooking.jpg" onerror="this.onerror=null;this.src='https://placehold.co/300x180/f48fb1/fff?text=Recipe+Cards';" alt="Project 2 Thumbnail: Recipe Cards">
                    <h3>Recipe Cards</h3>
                    <p>An online recipe card collection, demonstrating basic HTML structure and styling for content.</p>
                </div>
                <div class="portfolio-item">
                    <img src="https://raw.githubusercontent.com/rubaosama/ruba_osama/main/Pink%20Heart%20Aura.jpg" onerror="this.onerror=null;this.src='https://placehold.co/300x180/e91e63/fff?text=Blog+Design';" alt="Project 3 Thumbnail: Blog Design">
                    <h3>Blog</h3>
                    <p>A personal blog layout concept, focusing on typography and image integration.</p>
                </div>
            </div>
        </section>

        <section id="contact">
            <h2>Get in Touch!</h2>
            <div class="contact-info">
                <p>I'd love to connect and discuss potential collaborations or opportunities.</p>
                <p>Email me at: <a href="mailto:rubaosamaabdalla@gmail.com">rubaosamaabdalla@gmail.com</a></p>
                <div class="social-links">
                    <!-- Placeholder for social media icons - you can replace with actual icons or text links -->
                    <a href="#" aria-label="LinkedIn"><span style="font-size: 1.5em;">&#128100;</span></a> <!-- Placeholder for LinkedIn icon -->
                    <a href="#" aria-label="GitHub"><span style="font-size: 1.5em;">&#128187;</span></a> <!-- Placeholder for GitHub icon -->
                    <a href="#" aria-label="Instagram"><span style="font-size: 1.5em;">&#128247;</span></a> <!-- Placeholder for Instagram icon -->
                </div>
            </div>

            <div class="contact-form">
                <h3>Send Me a Message</h3>
                <form action="#" method="POST"> <!-- Action attribute can be updated to a backend script -->
                    <label for="name">Your Name:</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">Your Email:</label>
                    <input type="email" id="email" name="email" required>

                    <label for="message">Your Message:</label>
                    <textarea id="message" name="message" required></textarea>

                    <button type="submit">Send Message</button>
                </form>
            </div>
        </section>

        <footer>
            <p>&copy; 2025 Ruba Osama. All rights reserved. Made with love and a touch of pink! 💖</p>
        </footer>
    </div>
</body>
</html>
