# 00Marcus00.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MBR Mart</title>
<style>
* {
margin: 0;
padding: 0;
box-sizing: border-box;
}

body {
font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
color: white;
overflow-x: hidden;
line-height: 1.6;
}

/* Animated background particles */
.particles {
position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
pointer-events: none;
z-index: 1;
}

.particle {
position: absolute;
width: 2px;
height: 2px;
background: rgba(0, 255, 255, 0.6);
border-radius: 50%;
animation: float 8s infinite linear;
}

@keyframes float {
0% { transform: translateY(100vh) translateX(0px); opacity: 0; }
10% { opacity: 1; }
90% { opacity: 1; }
100% { transform: translateY(-100px) translateX(200px); opacity: 0; }
}

/* Navigation */
nav {
position: fixed;
top: 0;
width: 100%;
padding: 20px 50px;
background: rgba(0, 0, 0, 0.1);
backdrop-filter: blur(20px);
border-bottom: 1px solid rgba(255, 255, 255, 0.1);
z-index: 1000;
transition: all 0.3s ease;
}

.nav-container {
display: flex;
justify-content: space-between;
align-items: center;
max-width: 1200px;
margin: 0 auto;
}

.logo {
font-size: 28px;
font-weight: 800;
background: linear-gradient(45deg, #00ffff, #ff00ff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

.nav-links {
display: flex;
gap: 30px;
}

.nav-links a {
color: white;
text-decoration: none;
font-weight: 500;
transition: all 0.3s ease;
position: relative;
}

.nav-links a:hover {
color: #00ffff;
transform: translateY(-2px);
}

.nav-links a::after {
content: '';
position: absolute;
bottom: -5px;
left: 0;
width: 0;
height: 2px;
background: linear-gradient(90deg, #00ffff, #ff00ff);
transition: width 0.3s ease;
}

.nav-links a:hover::after {
width: 100%;
}

/* Hero Section */
.hero {
height: 100vh;
display: flex;
align-items: center;
justify-content: center;
text-align: center;
position: relative;
z-index: 2;
}

.hero-content {
max-width: 800px;
padding: 0 20px;
}

.hero h1 {
font-size: clamp(3rem, 8vw, 6rem);
font-weight: 900;
margin-bottom: 20px;
background: linear-gradient(45deg, #ffffff, #00ffff, #ff00ff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
animation: glow 3s ease-in-out infinite alternate;
}

@keyframes glow {
from { filter: drop-shadow(0 0 20px rgba(0, 255, 255, 0.3)); }
to { filter: drop-shadow(0 0 30px rgba(255, 0, 255, 0.5)); }
}

.hero p {
font-size: 1.5rem;
margin-bottom: 40px;
opacity: 0.9;
animation: fadeInUp 1s ease 0.5s both;
}

@keyframes fadeInUp {
from { opacity: 0; transform: translateY(30px); }
to { opacity: 1; transform: translateY(0); }
}

.cta-button {
display: inline-block;
padding: 18px 40px;
background: linear-gradient(45deg, #00ffff, #ff00ff);
color: white;
text-decoration: none;
border-radius: 50px;
font-weight: 600;
font-size: 1.1rem;
transition: all 0.3s ease;
position: relative;
overflow: hidden;
animation: fadeInUp 1s ease 1s both;
}

.cta-button::before {
content: '';
position: absolute;
top: 0;
left: -100%;
width: 100%;
height: 100%;
background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
transition: left 0.5s;
}

.cta-button:hover::before {
left: 100%;
}

.cta-button:hover {
transform: translateY(-3px) scale(1.05);
box-shadow: 0 20px 40px rgba(0, 255, 255, 0.3);
}

/* Sections */
.section {
padding: 100px 50px;
max-width: 1200px;
margin: 0 auto;
position: relative;
z-index: 2;
}

.section h2 {
font-size: 3rem;
margin-bottom: 60px;
text-align: center;
background: linear-gradient(45deg, #ffffff, #00ffff);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
}

/* Services Grid */
.services-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
gap: 40px;
margin-top: 60px;
}

.service-card {
background: rgba(255, 255, 255, 0.05);
padding: 40px 30px;
border-radius: 20px;
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.1);
transition: all 0.3s ease;
position: relative;
overflow: hidden;
}

.service-card::before {
content: '';
position: absolute;
top: 0;
left: 0;
right: 0;
height: 3px;
background: linear-gradient(90deg, #00ffff, #ff00ff);
transform: scaleX(0);
transition: transform 0.3s ease;
}

.service-card:hover::before {
transform: scaleX(1);
}

.service-card:hover {
transform: translateY(-10px);
box-shadow: 0 30px 60px rgba(0, 255, 255, 0.2);
background: rgba(255, 255, 255, 0.1);
}

.service-icon {
font-size: 3rem;
margin-bottom: 20px;
color: #00ffff;
}

.service-card h3 {
font-size: 1.5rem;
margin-bottom: 15px;
color: white;
}

.service-card p {
opacity: 0.8;
line-height: 1.6;
}

/* About section */
.about-content {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 60px;
align-items: center;
}

.about-text {
font-size: 1.2rem;
opacity: 0.9;
}

.stats {
display: grid;
grid-template-columns: repeat(2, 1fr);
gap: 30px;
}

.stat {
text-align: center;
padding: 30px;
background: rgba(255, 255, 255, 0.05);
border-radius: 15px;
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.1);
}

.stat-number {
font-size: 2.5rem;
font-weight: 800;
color: #00ffff;
margin-bottom: 10px;
}

.stat-label {
opacity: 0.8;
}

/* Contact form */
.contact-form {
max-width: 600px;
margin: 0 auto;
}

.form-group {
margin-bottom: 25px;
}

.form-group input,
.form-group textarea {
width: 100%;
padding: 15px 20px;
background: rgba(255, 255, 255, 0.05);
border: 1px solid rgba(255, 255, 255, 0.2);
border-radius: 10px;
color: white;
font-size: 1rem;
transition: all 0.3s ease;
backdrop-filter: blur(10px);
}

.form-group input:focus,
.form-group textarea:focus {
outline: none;
border-color: #00ffff;
box-shadow: 0 0 20px rgba(0, 255, 255, 0.2);
}

.form-group input::placeholder,
.form-group textarea::placeholder {
color: rgba(255, 255, 255, 0.6);
}

.submit-btn {
width: 100%;
padding: 18px;
background: linear-gradient(45deg, #00ffff, #ff00ff);
border: none;
border-radius: 10px;
color: white;
font-size: 1.1rem;
font-weight: 600;
cursor: pointer;
transition: all 0.3s ease;
}

.submit-btn:hover {
transform: translateY(-2px);
box-shadow: 0 15px 30px rgba(0, 255, 255, 0.3);
}

/* Footer */
footer {
text-align: center;
padding: 50px;
background: rgba(0, 0, 0, 0.3);
border-top: 1px solid rgba(255, 255, 255, 0.1);
position: relative;
z-index: 2;
}

/* Responsive */
@media (max-width: 768px) {
nav { padding: 15px 20px; }
.nav-links { display: none; }
.section { padding: 60px 20px; }
.about-content { grid-template-columns: 1fr; }
.hero h1 { font-size: 3rem; }
.hero p { font-size: 1.2rem; }
}

/* Scroll animations */
.fade-in {
opacity: 0;
transform: translateY(30px);
transition: all 0.6s ease;
}

.fade-in.visible {
opacity: 1;
transform: translateY(0);
}
</style>
</head>
<body>
<!-- Animated background particles -->
<div class="particles" id="particles"></div>

<!-- Navigation -->
<nav>
<div class="nav-container">
<div class="logo">Nexus</div>
<div class="nav-links">
<a href="#home">Home</a>
<a href="#services">Services</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</div>
</div>
</nav>

<!-- Hero Section -->
<section id="home" class="hero">
<div class="hero-content">
<h1>Digital Innovation</h1>
<p>Transforming ideas into extraordinary digital experiences</p>
<a href="#services" class="cta-button">Explore Our Work</a>
</div>
</section>

<!-- Services Section -->
<section id="services" class="section">
<h2 class="fade-in">Our Services</h2>
<div class="services-grid">
<div class="service-card fade-in">
<div class="service-icon">🚀</div>
<h3>Web Development</h3>
<p>Creating lightning-fast, responsive websites that captivate your audience and drive results.</p>
</div>
<div class="service-card fade-in">
<div class="service-icon">📱</div>
<h3>Mobile Apps</h3>
<p>Native and cross-platform mobile applications that deliver seamless user experiences.</p>
</div>
<div class="service-card fade-in">
<div class="service-icon">🎨</div>
<h3>UI/UX Design</h3>
<p>Intuitive designs that balance aesthetics with functionality for maximum user engagement.</p>
</div>
<div class="service-card fade-in">
<div class="service-icon">☁️</div>
<h3>Cloud Solutions</h3>
<p>Scalable cloud infrastructure and deployment solutions for modern businesses.</p>
</div>
<div class="service-card fade-in">
<div class="service-icon">🤖</div>
<h3>AI Integration</h3>
<p>Intelligent automation and machine learning solutions to streamline your operations.</p>
</div>
<div class="service-card fade-in">
<div class="service-icon">🔒</div>
<h3>Cybersecurity</h3>
<p>Robust security measures to protect your digital assets and customer data.</p>
</div>
</div>
</section>

<!-- About Section -->
<section id="about" class="section">
<h2 class="fade-in">About Nexus</h2>
<div class="about-content">
<div class="about-text fade-in">
<p>We are a cutting-edge digital agency specializing in creating innovative solutions that push the boundaries of technology. Our team of passionate developers, designers, and strategists work together to bring your vision to life.</p>
<br>
<p>With years of experience and a commitment to excellence, we've helped hundreds of businesses transform their digital presence and achieve remarkable growth.</p>
</div>
<div class="stats fade-in">
<div class="stat">
<div class="stat-number">500+</div>
<div class="stat-label">Projects Completed</div>
</div>
<div class="stat">
<div class="stat-number">50+</div>
<div class="stat-label">Happy Clients</div>
</div>
<div class="stat">
<div class="stat-number">5</div>
<div class="stat-label">Years Experience</div>
</div>
<div class="stat">
<div class="stat-number">24/7</div>
<div class="stat-label">Support</div>
</div>
</div>
</div>
</section>

<!-- Contact Section -->
<section id="contact" class="section">
<h2 class="fade-in">Get In Touch</h2>
<form class="contact-form fade-in">
<div class="form-group">
<input type="text" placeholder="Your Name" required>
</div>
<div class="form-group">
<input type="email" placeholder="Your Email" required>
</div>
<div class="form-group">
<input type="text" placeholder="Subject" required>
</div>
<div class="form-group">
<textarea rows="6" placeholder="Your Message" required></textarea>
</div>
<button type="submit" class="submit-btn">Send Message</button>
</form>
</section>

<!-- Footer -->
<footer>
<p>&copy; 2025 Nexus Digital. Crafted with passion and innovation.</p>
</footer>

<script>
// Create floating particles
function createParticles() {
const particlesContainer = document.getElementById('particles');
const particleCount = 50;

for (let i = 0; i < particleCount; i++) {
const particle = document.createElement('div');
particle.className = 'particle';
particle.style.left = Math.random() * 100 + '%';
particle.style.animationDuration = (Math.random() * 3 + 5) + 's';
particle.style.animationDelay = Math.random() * 2 + 's';
particlesContainer.appendChild(particle);
}
}

// Smooth scrolling for navigation links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
anchor.addEventListener('click', function (e) {
e.preventDefault();
const target = document.querySelector(this.getAttribute('href'));
if (target) {
target.scrollIntoView({
behavior: 'smooth',
block: 'start'
});
}
});
});

// Scroll animation observer
const observerOptions = {
threshold: 0.1,
rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
entries.forEach(entry => {
if (entry.isIntersecting) {
entry.target.classList.add('visible');
}
});
}, observerOptions);

// Observe all fade-in elements
document.querySelectorAll('.fade-in').forEach(el => {
observer.observe(el);
});

// Form submission
document.querySelector('.contact-form').addEventListener('submit', function(e) {
e.preventDefault();

// Get form data
const formData = new FormData(this);
const name = this.querySelector('input[placeholder="Your Name"]').value;
const email = this.querySelector('input[placeholder="Your Email"]').value;
const subject = this.querySelector('input[placeholder="Subject"]').value;
const message = this.querySelector('textarea').value;

// Show success message
alert(`Thank you, ${name}! Your message has been received. We'll get back to you soon.`);

// Reset form
this.reset();
});

// Dynamic navbar background on scroll
window.addEventListener('scroll', () => {
const nav = document.querySelector('nav');
if (window.scrollY > 100) {
nav.style.background = 'rgba(0, 0, 0, 0.9)';
} else {
nav.style.background = 'rgba(0, 0, 0, 0.1)';
}
});

// Initialize particles when page loads
document.addEventListener('DOMContentLoaded', createParticles);

// Add mouse movement parallax effect
document.addEventListener('mousemove', (e) => {
const mouseX = e.clientX / window.innerWidth;
const mouseY = e.clientY / window.innerHeight;

document.querySelectorAll('.particle').forEach((particle, index) => {
const speed = (index % 5 + 1) * 0.5;
const x = (mouseX - 0.5) * speed;
const y = (mouseY - 0.5) * speed;
particle.style.transform = `translate(${x}px, ${y}px)`;
});
});
</script>
</body>
</html>

