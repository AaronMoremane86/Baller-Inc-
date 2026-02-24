index.htlm
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nexus Digital | Modern Solutions</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav class="navbar">
        <div class="logo">Nexus<span>Digital</span></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button class="btn-toggle" id="theme-toggle">🌙</button>
    </nav>

    <header id="home" class="hero">
        <h1>Scalable Solutions for <br><strong>Modern Businesses</strong></h1>
        <p>We build high-performance digital products that drive growth.</p>
        <a href="#contact" class="cta-button">Get Started</a>
    </header>

    <section id="services" class="services">
        <h2>Our Expertise</h2>
        <div class="service-grid">
            <div class="card">
                <h3>Web Design</h3>
                <p>Creating intuitive and stunning user interfaces.</p>
            </div>
            <div class="card">
                <h3>Development</h3>
                <p>Robust backends and lightning-fast frontends.</p>
            </div>
            <div class="card">
                <h3>SEO Strategy</h3>
                <p>Getting your brand to the top of search results.</p>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Work With Us</h2>
        <form id="contactForm">
            <input type="text" placeholder="Name" required>
            <input type="email" placeholder="Email" required>
            <textarea placeholder="Your Message"></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <script src="script.js"></script>
</body>
</html>
:root {
    --primary: #2563eb;
    --dark: #1e293b;
    --light: #f8fafc;
}

body {
    font-family: 'Segoe UI', sans-serif;
    margin: 0;
    color: var(--dark);
    scroll-behavior: smooth;
}

/* Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    padding: 1.5rem 10%;
    background: white;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

.logo { font-weight: bold; font-size: 1.5rem; }
.logo span { color: var(--primary); }
.nav-links { list-style: none; display: flex; gap: 2rem; }
.nav-links a { text-decoration: none; color: var(--dark); font-weight: 500; }

/* Hero Section */
.hero {
    padding: 100px 10%;
    text-align: center;
    background: linear-gradient(135deg, #f1f5f9 0%, #e2e8f0 100%);
}

.hero h1 { font-size: 3rem; margin-bottom: 1rem; }
.cta-button {
    background: var(--primary);
    color: white;
    padding: 1rem 2.5rem;
    border-radius: 30px;
    text-decoration: none;
    display: inline-block;
    margin-top: 2rem;
}

/* Services */
.service-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    padding: 50px 10%;
}

.card {
    padding: 2rem;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    transition: transform 0.3s;
}

.card:hover { transform: translateY(-10px); }

/* Contact Form */
.contact { padding: 50px 10%; background: #f8fafc; text-align: center; }
form { max-width: 500px; margin: 0 auto; display: flex; flex-direction: column; gap: 1rem; }
input, textarea { padding: 1rem; border: 1px solid #cbd5e1; border-radius: 8px; }
button[type="submit"] { background: var(--dark); color: white; padding: 1rem; border: none; border-radius: 8px; cursor: pointer; }
// Theme Toggle
const toggleBtn = document.getElementById('theme-toggle');
const body = document.body;

toggleBtn.addEventListener('click', () => {
    body.classList.toggle('dark-theme');
    // Change icon based on mode
    toggleBtn.textContent = body.classList.contains('dark-theme') ? '☀️' : '🌙';
});

// Form Submission Handling
document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();
    alert('Thank you! Your message has been sent to our team.');
    this.reset();
});
