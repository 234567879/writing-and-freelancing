<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Freelance Copywriting Services</title>
    <link rel="stylesheet" href="styles.css">
    <script src="script.js" defer></script>
</head>
<body>
    <header>
        <h1>Freelance Copywriting Services</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#pricing">Pricing</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="animated-section">
        <h2>Welcome to My Copywriting Services</h2>
        <p>Providing high-quality copywriting services to help your business grow.</p>
    </section>

    <section id="pricing" class="animated-section">
        <h2>Pricing</h2>
        <ul>
            <li>Basic Package: $100</li>
            <li>Standard Package: $200</li>
            <li>Premium Package: $300</li>
        </ul>
    </section>

    <section id="blog" class="animated-section">
        <h2>Blog</h2>
        <article>
            <h3>How to Write Compelling Copy</h3>
            <p>Writing compelling copy is essential for engaging your audience...</p>
        </article>
        <article>
            <h3>Top Tips for Freelancers</h3>
            <p>As a freelancer, managing your time and clients is crucial...</p>
        </article>
    </section>

    <section id="contact" class="animated-section">
        <h2>Contact Me</h2>
        <p>If you have any questions or would like to work together, feel free to reach out!</p>
        <p>Email: <a href="mailto:your-email@example.com">your-email@example.com</a></p>
    </section>

    <footer>
        <p>&copy; 2023 Your Name. All rights reserved.</p>
    </footer>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

.animated-section {
    padding: 20px;
    margin: 20px;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.5s ease, transform 0.5s ease;
}

.animated-section.visible {
    opacity: 1;
    transform: translateY(0);
}

footer {
    text-align: center;
    padding: 10px 0;
    background: #333;
    color: #fff;
    position: relative;
    bottom: 0;
    width: 100%;
    document.addEventListener("DOMContentLoaded", function() {
    const sections = document.querySelectorAll('.animated-section');

    const options = {
        root: null,
        threshold: 0.1,
        rootMargin: "0px"
    };

    const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');
                observer.unobserve(entry.target);
            }
        });
    }, options);

    sections.forEach(section => {
        observer.observe(section);
    });
});
}
