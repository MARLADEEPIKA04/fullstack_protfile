<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Portfolio</title>
<style>
* { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
body { background: #111; color: #fff; }

/* HEADER */
header {
    background: #222;
    padding: 15px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky; top: 0; z-index: 1000;
}
header h1 { color: #00eaff; font-size: 28px; }
nav a {
    margin-left: 20px;
    color: #ddd;
    text-decoration: none;
    font-weight: 600;
}
nav a:hover { color: #00eaff; }

/* HOME PROFILE */
.profile {
    text-align: center;
    padding: 70px 10%;
}
.profile img {
    width: 180px; height: 180px;
    border-radius: 50%;
    border: 4px solid #00eaff;
    margin-bottom: 20px;
}
.profile h2 { font-size: 34px; color: #00eaff; margin-bottom: 10px; }
.profile h3 { font-size: 22px; color: #ccc; }

/* MAIN SECTIONS */
section h2 { font-size: 32px; color: #00eaff; margin-bottom: 20px; padding-top: 20px; }

/* ABOUT */
.about p { line-height: 1.7; font-size: 18px; }

/* SKILLS */
.skills div {
    background: #222; padding: 15px; margin: 10px 0;
    border-left: 5px solid #00eaff; font-size: 18px;
}

/* PROJECTS */
.projects .card {
    background: #222; padding: 20px; border-radius: 8px; margin-bottom: 15px;
}
.projects .card h3 { color: #00eaff; margin-bottom: 10px; }

/* CONTACT FORM */
form { max-width: 450px; }
form input, form textarea {
    width: 100%; padding: 10px; margin: 10px 0;
    border: none; border-bottom: 2px solid #00eaff;
    background: transparent; color: #fff; font-size: 16px;
}
button {
    padding: 10px 20px; border: none; background: #00eaff;
    color: #111; font-weight: bold; cursor: pointer; margin-top: 10px;
}
button:hover { background: #fff; color: #111; }
</style>
</head>

<body>

<header>
    <h1>Portfolio</h1>
    <nav>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<!-- ===== PROFILE WITH IMAGE + NAME ===== -->
<section class="profile">
    <img src="C:\Users\marla\Downloads\DEEPU_PIC.jpeg" alt="picture"> <!-- Replace this image -->
    <h2>MARLA DEEPIKA</h2>
    <h3>Web Developer | Programmer</h3>
</section>

<!-- ===== ABOUT ===== -->
<section id="about" class="about">
    <h2>About Me</h2>
    <p>Hello! I'm a web developer passionate about building beautiful and functional websites.
       I love working with HTML, CSS, JavaScript, and modern frameworks.</p>
</section>

<!-- ===== SKILLS ===== -->
<section id="skills" class="skills">
    <h2>My Skills</h2>
    <div>HTML, CSS, JavaScript</div>
    <div>React & Node.js</div>
    <div>Python & Django</div>
    <div>SQL & MongoDB</div>
</section>

<!-- ===== PROJECTS ===== -->
<section id="projects" class="projects">
    <h2>Projects</h2>
    <div class="card">
        <h3>Portfolio Website</h3>
        <p>A responsive personal profile website using HTML, CSS & JS.</p>
    </div>
    <div class="card">
        <h3>Weather App</h3>
        <p>Real-time weather details using API and JavaScript.</p>
    </div>
</section>

<!-- ===== CONTACT ===== -->
<section id="contact">
    <h2>Contact Me</h2>
    <form id="contactForm">
        <input type="text" id="name" placeholder="Your Name">
        <input type="email" id="email" placeholder="Your Email">
        <textarea id="msg" rows="4" placeholder="Message"></textarea>
        <button type="button" onclick="sendMessage()">Send Message</button>
    </form>
</section>

<script>
function sendMessage() {
    let name = document.getElementById("name").value;
    let email = document.getElementById("email").value;
    let msg = document.getElementById("msg").value;
    if(name == "" || email == "" || msg == ""){
        alert("Please fill all fields!");
    } else {
        alert("Message Sent Successfully!");
        document.getElementById("contactForm").reset();
    }
}
</script>

</body>
</html>
