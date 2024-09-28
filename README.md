# skillhub.github.io
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SkillHub | Elevate Your Skills</title>
    <!-- Font Awesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="stylesheet" href="styles.css">
</head>
<style>
    /* Global Styles */
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        margin: 0;
        padding: 0;
        background-color: #f7f9fc;
        color: #333;
        scroll-behavior: smooth;
    }

    /* Header */
    header {
        background-color: #2C3E50;
        color: white;
        padding: 1.5em 2em;
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: sticky;
        top: 0;
        z-index: 1000;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transform: translateY(-100%);
        opacity: 0;
        animation: slideDown 1s ease-out forwards;
    }

    @keyframes slideDown {
        to {
            transform: translateY(0);
            opacity: 1;
        }
    }

    header h1 {
        margin: 0;
        font-size: 28px;
        font-weight: bold;
        letter-spacing: 1px;
    }

    nav ul {
        list-style: none;
        display: flex;
        margin: 0;
        padding: 0;
    }

    nav ul li {
        margin: 0 15px;
    }

    nav ul li a {
        color: white;
        text-decoration: none;
        font-size: 16px;
        display: flex;
        align-items: center;
        transition: color 0.3s ease-in-out;
    }

    nav ul li a i {
        margin-right: 5px; /* Space between icon and text */
    }

    nav ul li a:hover {
        color: #1ABC9C;
    }

    /* Hero Section */
    #hero {
        background-image: url('hero-background.jpg');
        background-size: cover;
        background-position: center;
        color: rgb(238, 154, 154);
        text-align: center;
        padding: 100px 20px;
    }

    #hero h1,
    #hero p,
    #hero button {
        opacity: 0;
        animation: fadeInUp 1.5s ease-out forwards;
    }

    #hero h1 {
        font-size: 48px;
        margin-bottom: 20px;
        animation-delay: 0.3s;
    }

    #hero p {
        font-size: 20px;
        margin-bottom: 40px;
        animation-delay: 0.6s;
    }

    #hero button {
        padding: 15px 30px;
        background-color: #1ABC9C;
        color: white;
        border: none;
        border-radius: 30px;
        font-size: 18px;
        cursor: pointer;
        transition: background-color 0.3s ease-in-out;
        animation-delay: 0.9s;
    }

    #hero button:hover {
        background-color: #16a085;
    }

    /* Course List Section */
    #courses {
        background-color: #f7f9fc;
        padding: 4em 2em;
    }

    #courses h2 {
        text-align: center;
        font-size: 36px;
        margin-bottom: 30px;
    }

    .course-filter {
        text-align: center;
        margin-bottom: 30px;
    }

    .filter-button {
        padding: 10px 20px;
        background-color: #1ABC9C;
        color: white;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        font-size: 16px;
        margin: 0 5px;
        transition: background-color 0.3s ease;
    }

    .filter-button:hover {
        background-color: #16a085;
    }

    .course-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .course-item {
        background-color: #fff;
        border-radius: 10px;
        text-align: center;
        padding: 20px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
        opacity: 0;
        transform: translateY(30px);
        animation: fadeInUp 1.5s ease forwards;
    }

    .course-item:nth-child(1) {
        animation-delay: 0.3s;
    }

    .course-item:nth-child(2) {
        animation-delay: 0.4s;
    }

    .course-item:nth-child(3) {
        animation-delay: 0.5s;
    }

    .course-item:nth-child(4) {
        animation-delay: 0.6s;
    }

    .course-item:nth-child(5) {
        animation-delay: 0.7s;
    }

    .course-item:nth-child(6) {
        animation-delay: 0.8s;
    }

    .course-item:hover {
        transform: translateY(-10px);
    }

    .course-item img {
        width: 100px;
        margin-bottom: 15px;
    }

    .course-item h3 {
        font-size: 20px;
        margin-bottom: 10px;
    }

    .course-item p {
        font-size: 14px;
        color: #555;
        margin-bottom: 15px;
    }

    .course-item button {
        display: inline-block;
        background-color: #1ABC9C;
        color: white;
        padding: 10px 20px;
        border-radius: 30px;
        border: none;
        cursor: pointer;
        font-size: 16px;
        transition: background-color 0.3s ease;
    }

    /* Course item hover effect */
    .course-item:hover {
        transform: scale(1.05);
        box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    /* Button hover effect in course item */
    .course-item button:hover {
        background-color: #16a085;
    }

    /* Course Details */
    .course-details {
        display: none;
        margin-top: 15px;
        color: #555;
    }

   /* Projects Section Styles */
.projects-section {
    padding: 30px;
    background: linear-gradient(to right, #f9f9f9, #e1e1e1); /* Gradient background */
    border-radius: 10px; /* Slightly more rounded corners */
    margin: 30px 0; /* Increased spacing */
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
}

.projects-section h2 {
    text-align: center;
    color: #2c3e50; /* Darker color for better contrast */
    font-size: 2.5em; /* Larger font size */
    margin-bottom: 20px; /* Space below the title */
    text-transform: uppercase; /* Uppercase letters */
    letter-spacing: 1px; /* Spacing between letters */
}

.project-category {
    margin: 20px 0; /* Space between project categories */
    padding: 20px; /* Padding around each category */
    border: 2px solid #3498db; /* Bright border color */
    border-radius: 5px; /* Rounded corners */
    background-color: #fff; /* White background for categories */
    transition: transform 0.3s, box-shadow 0.3s; /* Smooth transition effects */
}

.project-category:hover {
    transform: translateY(-5px); /* Lift effect on hover */
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2); /* Shadow for hover effect */
}

.project-category h3 {
    color: #2980b9; /* Bright color for category titles */
    margin-bottom: 15px; /* Space below category titles */
    font-size: 1.8em; /* Slightly larger font size for category titles */
}

.project-category ul {
    list-style-type: none; /* Remove default list styling */
    padding: 0; /* Remove default padding */
}

.project-category ul li {
    padding: 10px 0; /* Space between list items */
    color: #555; /* Gray color for project ideas */
    font-size: 1.2em; /* Slightly larger font size for project ideas */
    position: relative; /* Positioning for pseudo-element */
}

.project-category ul li:hover {
    color: #2980b9; /* Change color on hover for interactivity */
    cursor: pointer; /* Change cursor to pointer on hover */
}

.project-category ul li::before {
    content: '➤'; /* Arrow indicator before each project */
    position: absolute; /* Positioning the arrow */
    left: -20px; /* Space from the left */
    color: #3498db; /* Color for the arrow */
    transition: transform 0.3s; /* Smooth transition for arrow */
}

.project-category ul li:hover::before {
    transform: scale(1.2); /* Scale up arrow on hover */
}


    /* Centralized Roadmap Section */
    #roadmap {
        background-color: #f1f2f6;
        padding: 4em 2em;
        text-align: center;
    }

    .roadmap-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .roadmap-item {
        background-color: #fff;
        border-radius: 10px;
        padding: 20px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        text-align: left;
    }

    .roadmap-item h3 {
        font-size: 24px;
        margin-bottom: 15px;
    }

    .roadmap-item ul {
        list-style-type: none;
        padding: 0;
    }

    .roadmap-item ul li {
        padding: 10px 0;
        border-bottom: 1px solid #ddd;
    }

    /* About Section */
    #about {
        background-color: #ecf0f1;
        padding: 4em 2em;
        text-align: center;
    }

    #about h2 {
        font-size: 36px;
        margin-bottom: 20px;
    }

    #about p {
        font-size: 18px;
        color: #333;
        margin-bottom: 15px;
        line-height: 1.6;
    }

    

    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(20px);
        }

        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    /* Add this style to hide roadmap details initially */
    .hidden {
        display: none;
    }
</style>
<body>
    <!-- Header -->
    <header>
        <h1>SkillHub</h1>
        <nav>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#featured">Featured Courses</a></li>
                <li><a href="#courses">Courses</a></li>
                <li><a href="#roadmap">Roadmap</a></li>
                <li><a href="#project">Projects</a></li>
                <li><a href="#about">About</a></li>
            </ul>
            
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <h1>Welcome to SkillHub</h1>
        <p id="hero-topic">Elevate your skills and advance your career with our online courses.</p>
        
    </section>

    <!-- Featured Courses Section -->
    <section id="featured">
        <h2>Featured Courses</h2>
        <div class="featured-course">
            <img src="9776473.jpg" alt="Web Development">
            <h3>Web Development</h3>
            <p>Learn to build modern websites using HTML, CSS, and JavaScript.</p>
            <button onclick="window.location.href='https://www.youtube.com/watch?v=tVzUXW6siu0&list=PLu0W_9lII9agq5TrH9XLIKQvv0iaF2X3w'">Enroll Now</button>
        </div>
        
        <div class="featured-course">
            <img src="ai-generated-8136170_1280.png" alt="Cyber Security">
            <h3>Cyber Security</h3>
            <p>Protect your data and learn how to defend against cyber threats.</p>
            <button onclick="window.location.href='https://youtu.be/YOuRsJSjurs?si=D2NX1Wanrp7ELYtl'">Enroll Now</button>
        </div>
        

    </section>
    <!-- Courses Section -->
    <section id="courses">
        <h2>All Courses</h2>
        <div class="course-filter">
            <button class="filter-button" onclick="filterCourses('all')">All Courses</button>
            <button class="filter-button" onclick="filterCourses('frontend')">Frontend</button>
            <button class="filter-button" onclick="filterCourses('backend')">Backend</button>
        </div>
        <div class="course-grid">
            <div class="course-item frontend">
                <img src="icons8-html-240.png" alt="HTML">
                <h3>HTML</h3>
                <p>Learn HTML from the basics</p>
                <a href="https://www.codewithharry.com/tutorial/html-home/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item frontend">
                <img src="icons8-css3-240.png" alt="CSS">
                <h3>CSS</h3>
                <p>Style your web pages with CSS</p>
                <a href="https://www.codewithharry.com/tutorial/css-home/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item backend">
                <img src="icons8-javascript-240.png" alt="JavaScript">
                <h3>JavaScript</h3>
                <p>Interactive web development with JavaScript</p>
                <a href="https://www.codewithharry.com/tutorial/js/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item backend">
                <img src="icons8-python-240.png" alt="Python">
                <h3>Python</h3>
                <p>Begin your programming journey with Python</p>
                <a href="https://www.codewithharry.com/tutorial/python/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item backend">
                <img src="data stru.jpg" alt="DSA">
                <h3>Data Structures & Algorithms</h3>
                <p>Master the core concepts of DSA</p>
                <button class="start-learning" onclick="showDetails(this)">Start Learning</button>
                <p class="course-details">Data Structures and Algorithms (DSA) form the foundation of efficient
                    problem-solving in computer science. This course covers key topics like arrays, linked lists, trees,
                    graphs, searching, sorting algorithms, dynamic programming, and much more. You'll learn how to
                    approach problems systematically and design optimal solutions to tackle complex challenges.
                <a href="https://www.programiz.com/dsa"> View course</a></p>
            </div>
            <div class="course-item backend">
                <img src="c++.png" alt="C++">
                <h3>C++</h3>
                <p>Master the art of system-level programming</p>
                <a href="https://www.codewithharry.com/tutorial/cplusplus/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item backend">
                <img src="c.png" alt="C Programming">
                <h3>C Programming</h3>
                <p>Understand the core of programming with C</p>
                <a href="https://www.codewithharry.com/tutorial/c/" target="_blank">Visit Tutorial</a>
            </div>
            
            <div class="course-item backend">
                <img src="icons8-php-100.png" alt="PHP Programming">
                <h3>PHP Programming</h3>
                <p>Learn server-side scripting with PHP</p>
                <a href="https://www.codewithharry.com/tutorial/php/" target="_blank">Visit Tutorial</a>
            </div>
            

            <!-- Add more courses as needed -->
        </div>
    </section>

    <!-- Projects Section -->
<section id="project">
    <div class="projects-section">
        <h2>Projects</h2>
        
        <div class="project-category">
            <h3>Web Development Projects</h3>
            <ul>
                <li>1. Personal Portfolio Website</li>
                <li>2. Blog Platform</li>
                <li>3. E-commerce Store</li>
                <li>4. Weather App</li>
                <li>5. Task Manager</li>
                <li>6. Recipe Finder</li>
                <li>7. Social Media Dashboard</li>
                <li>8. Event Management System</li>
                <li>9. Interactive Quiz App</li>
                <li>10. Online Survey Tool</li>
            </ul>
        </div>
    
        <div class="project-category">
            <h3>C++ Projects</h3>
            <ul>
                <li>1. Text-Based Adventure Game</li>
                <li>2. Library Management System</li>
                <li>3. Student Grade Management</li>
                <li>4. Snake Game</li>
                <li>5. Weather Station Simulator</li>
                <li>6. Simple Chat Application</li>
                <li>7. Tic-Tac-Toe Game</li>
                <li>8. Bank Management System</li>
                <li>9. File Compression Tool</li>
                <li>10. Music Player</li>
            </ul>
        </div>
    
        <div class="project-category">
            <h3>C Projects</h3>
            <ul>
                <li>1. Basic Shell</li>
                <li>2. To-Do List Application</li>
                <li>3. File Encryption/Decryption Tool</li>
                <li>4. Mini Text Editor</li>
                <li>5. Budget Tracker</li>
                <li>6. Calculator</li>
                <li>7. Simple HTTP Server</li>
                <li>8. Memory Management Simulation</li>
                <li>9. Game of Life</li>
                <li>10. Maze Solver</li>
            </ul>
        </div>
    
        <div class="project-category">
            <h3>Python Projects</h3>
            <ul>
                <li>1. Web Scraper</li>
                <li>2. Chatbot</li>
                <li>3. Image Gallery</li>
                <li>4. Automated Email Sender</li>
                <li>5. Personal Finance Tracker</li>
                <li>6. Stock Price Tracker</li>
                <li>7. Text Summarizer</li>
                <li>8. Fitness Tracker</li>
                <li>9. Game Development</li>
                <li>10. Voice Assistant</li>
            </ul>
        </div>
    </div>
</section>

<!-- Centralized Roadmap Section -->
<section id="roadmap">
    <h2>Learning Roadmap</h2>
    <div class="roadmap-grid">
        <div class="roadmap-item">
            <h3 onclick="toggleRoadmap('webDev')">Web Development Roadmap</h3>
            <ul id="webDev" class="hidden">
                <li><strong>Step 1: Learn HTML & CSS</strong>
                    <ul>
                        <li><a href="https://www.w3schools.com/html/" target="_blank">W3Schools HTML Tutorial</a> - Comprehensive guide to HTML basics.</li>
                        <li><a href="https://www.freecodecamp.org/learn/responsive-web-design/#basic-html-and-html5" target="_blank">FreeCodeCamp: Basic HTML and HTML5</a> - Free course on HTML fundamentals.</li>
                    </ul>
                </li>
                <li><strong>Step 2: JavaScript Basics</strong>
                    <ul>
                        <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide" target="_blank">MDN JavaScript Guide</a> - Official guide covering JavaScript basics.</li>
                        <li><a href="https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/#basic-javascript" target="_blank">FreeCodeCamp: Basic JavaScript</a> - Interactive lessons on JavaScript.</li>
                    </ul>
                </li>
                <li><strong>Step 3: Frontend Frameworks (React.js)</strong>
                    <ul>
                        <li><a href="https://reactjs.org/tutorial/tutorial.html" target="_blank">Official React Tutorial</a> - Learn React step by step.</li>
                        <li><a href="https://scrimba.com/learn/learnreact" target="_blank">Scrimba: Learn React for Free</a> - Interactive React course.</li>
                    </ul>
                </li>
                <li><strong>Step 4: Backend Development</strong>
                    <ul>
                        <li><a href="https://www.freecodecamp.org/learn/back-end-development-and-apis/#basic-node-and-express" target="_blank">FreeCodeCamp: Node.js and Express</a> - Introduction to backend development.</li>
                        <li><a href="https://www.codecademy.com/learn/learn-nodejs" target="_blank">Codecademy: Learn Node.js</a> - Interactive Node.js course.</li>
                    </ul>
                </li>
                <li><strong>Step 5: Build Projects</strong>
                    <ul>
                        <li>Build a personal portfolio website to showcase your work.</li>
                        <li>Contribute to open-source projects on <a href="https://github.com/" target="_blank">GitHub</a>.</li>
                    </ul>
                </li>
            </ul>
        </div>
        <div class="roadmap-item">
            <h3 onclick="toggleRoadmap('dataScience')">Data Science Roadmap</h3>
            <ul id="dataScience" class="hidden">
                <li><strong>Step 1: Introduction to Python</strong>
                    <ul>
                        <li><a href="https://www.learnpython.org/" target="_blank">Learn Python.org</a> - Free interactive Python tutorial.</li>
                        <li><a href="https://www.codecademy.com/learn/learn-python-3" target="_blank">Codecademy: Learn Python 3</a> - Interactive Python course.</li>
                    </ul>
                </li>
                <li><strong>Step 2: Data Analysis with Pandas</strong>
                    <ul>
                        <li><a href="https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html" target="_blank">Official Pandas Documentation</a> - Learn about Pandas for data manipulation.</li>
                        <li><a href="https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python" target="_blank">DataCamp: Pandas Tutorial</a> - Comprehensive guide to Pandas.</li>
                    </ul>
                </li>
                <li><strong>Step 3: Data Visualization</strong>
                    <ul>
                        <li><a href="https://matplotlib.org/stable/tutorials/introductory/pyplot.html" target="_blank">Matplotlib Official Tutorials</a> - Learn data visualization with Matplotlib.</li>
                        <li><a href="https://seaborn.pydata.org/tutorial.html" target="_blank">Seaborn Official Tutorials</a> - Learn about statistical data visualization.</li>
                    </ul>
                </li>
                <li><strong>Step 4: Machine Learning</strong>
                    <ul>
                        <li><a href="https://www.coursera.org/learn/machine-learning" target="_blank">Coursera: Machine Learning by Andrew Ng</a> - Free to audit course on machine learning basics.</li>
                        <li><a href="https://www.kaggle.com/learn/overview" target="_blank">Kaggle Learn: Intro to Machine Learning</a> - Learn machine learning through practical exercises.</li>
                    </ul>
                </li>
                <li><strong>Step 5: Build Projects</strong>
                    <ul>
                        <li>Participate in data science competitions on <a href="https://www.kaggle.com/" target="_blank">Kaggle</a>.</li>
                        <li>Create a portfolio showcasing your projects on <a href="https://github.com/" target="_blank">GitHub</a>.</li>
                    </ul>
                </li>
            </ul>
        </div>
        <div class="roadmap-item">
            <h3 onclick="toggleRoadmap('cyberSec')">Cyber Security Roadmap</h3>
            <ul id="cyberSec" class="hidden">
                <li><strong>Step 1: Basics of Networking</strong>
                    <ul>
                        <li><a href="https://www.coursera.org/learn/networking-basics" target="_blank">Coursera: Networking Basics</a> - Free course on networking fundamentals.</li>
                        <li><a href="https://www.w3schools.com/whatis/whatis_networking.asp" target="_blank">W3Schools: Networking Basics</a> - Introduction to networking concepts.</li>
                    </ul>
                </li>
                <li><strong>Step 2: Understanding Security Principles</strong>
                    <ul>
                        <li><a href="https://www.cybrary.it/course/cyber-security-fundamentals/" target="_blank">Cybrary: Cyber Security Fundamentals</a> - Introductory course on cybersecurity.</li>
                        <li><a href="https://www.edx.org/course/cybersecurity-fundamentals" target="_blank">edX: Cybersecurity Fundamentals</a> - Free course on fundamental security concepts.</li>
                    </ul>
                </li>
                <li><strong>Step 3: Ethical Hacking Techniques</strong>
                    <ul>
                        <li><a href="https://www.cybrary.it/course/ethical-hacking/" target="_blank">Cybrary: Ethical Hacking Course</a> - Learn ethical hacking skills.</li>
                        <li><a href="https://www.udemy.com/course/learn-ethical-hacking-from-scratch/" target="_blank">Udemy: Learn Ethical Hacking from Scratch</a> - Free course on ethical hacking techniques.</li>
                    </ul>
                </li>
                <li><strong>Step 4: Incident Response</strong>
                    <ul>
                        <li><a href="https://www.sans.org/cyber-security-courses/incident-response-team-management/" target="_blank">SANS: Incident Response Team Management</a> - Learn about incident response strategies.</li>
                        <li><a href="https://www.cybrary.it/course/incident-response-and-handling/" target="_blank">Cybrary: Incident Response and Handling</a> - Understand the fundamentals of incident response.</li>
                    </ul>
                </li>
                <li><strong>Step 5: Build a Cyber Security Lab</strong>
                    <ul>
                        <li>Set up a home lab using virtual machines to practice your skills.</li>
                        <li>Participate in Capture The Flag (CTF) challenges on <a href="https://www.hackerrank.com/domains/tutorials/10-days-of-security" target="_blank">HackerRank</a> or <a href="https://ctflearn.com/" target="_blank">CTFlearn</a>.</li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</section>




    <!-- About Section -->
    <section id="about">
        <h2>About SkillHub</h2>
        <p>SkillHub is your ultimate destination for learning and personal growth. Our mission is to provide
            high-quality online courses that cater to learners of all levels. Whether you're a beginner looking to get
            started or a seasoned professional aiming to enhance your skills, we have something for everyone.</p>
        <p>With our experienced instructors and engaging course materials, we aim to empower learners and help them
            achieve their career goals. Join SkillHub today and embark on your learning journey!</p>
    </section>

    <section id="contact" class="contact-section">
        <h2>Contact Us</h2>
        <p>We'd love to hear from you! Please fill out the form below to get in touch.</p>
        <form action="https://example.com/submit" method="POST">
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="5" required></textarea>
            </div>
            <button type="submit">Send Message</button>
        </form>
    </section>
    


    <!-- Footer -->
    <footer>
        <p>&copy; 2024 SkillHub. All Rights Reserved.</p>
    </footer>


    <!-- JavaScript -->
    <script>
        // Array of topics to display in the hero section
        const topics = [
            "Elevate your skills and advance your career with our online courses.",
            "Learn Web Development with HTML, CSS, and JavaScript.",
            "Master Cyber Security and protect your data from cyber threats.",
            "Explore Data Science and Machine Learning with Python."
        ];

        let topicIndex = 0; // Start from the first topic

        // Function to change topics
        function changeTopic() {
            const topicElement = document.getElementById('hero-topic');
            topicIndex = (topicIndex + 1) % topics.length; // Move to the next topic, loop back to the first
            topicElement.textContent = topics[topicIndex]; // Update the hero topic text
        }
        // Show course details
        function showDetails(button) {
            const details = button.nextElementSibling;
            details.style.display = details.style.display === 'block' ? 'none' : 'block';
        }

        function toggleRoadmap(id) {
        const element = document.getElementById(id);
        if (element.classList.contains('hidden')) {
            element.classList.remove('hidden');
        } else {
            element.classList.add('hidden');
        }
    }


        // Set interval for changing topics every 4 seconds (4000ms)
        setInterval(changeTopic, 4000);
    </script>
</body>

</html>
