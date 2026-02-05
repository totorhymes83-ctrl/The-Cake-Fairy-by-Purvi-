<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sandesh Bengali Sweets - Authentic Bengali Delicacies in Mumbai</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(139, 69, 19, 0.95), rgba(160, 82, 45, 0.9)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23f5deb3" width="1200" height="600"/><circle cx="200" cy="150" r="80" fill="%23daa520" opacity="0.3"/><circle cx="900" cy="400" r="120" fill="%23cd853f" opacity="0.2"/><circle cx="600" cy="300" r="100" fill="%23d2691e" opacity="0.25"/></svg>');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 50%, rgba(218, 165, 32, 0.2), transparent);
        }

        .hero-content {
            position: relative;
            z-index: 1;
            animation: fadeInUp 1s ease;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: 2px;
        }

        .hero .tagline {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            font-weight: 300;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }

        .rating {
            display: inline-flex;
            align-items: center;
            background: rgba(255, 255, 255, 0.2);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            backdrop-filter: blur(10px);
        }

        .stars {
            color: #ffd700;
            font-size: 1.5rem;
            margin-right: 0.5rem;
        }

        .rating-text {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .btn-primary {
            background: #ffd700;
            color: #8B4513;
        }

        .btn-primary:hover {
            background: #ffed4e;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 215, 0, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: white;
            color: #8B4513;
            transform: translateY(-3px);
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(139, 69, 19, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 5%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #ffd700;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            color: #ffd700;
        }

        /* About Section */
        .about {
            padding: 6rem 5%;
            background: #fff;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: #8B4513;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ffd700;
            margin: 1rem auto;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
            color: #555;
        }

        .about-image {
            text-align: center;
        }

        .about-image svg {
            max-width: 100%;
            height: auto;
            filter: drop-shadow(0 10px 20px rgba(0,0,0,0.1));
        }

        /* Services Section */
        .services {
            padding: 6rem 5%;
            background: linear-gradient(135deg, #f5f5f5, #e8e8e8);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            color: #8B4513;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .service-card p {
            color: #666;
            line-height: 1.6;
        }

        /* Location Section */
        .location {
            padding: 6rem 5%;
            background: white;
        }

        .location-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: start;
        }

        .location-info {
            background: linear-gradient(135deg, #8B4513, #A0522D);
            color: white;
            padding: 3rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .info-item {
            margin-bottom: 2rem;
            display: flex;
            align-items: start;
            gap: 1rem;
        }

        .info-icon {
            font-size: 1.5rem;
            color: #ffd700;
            min-width: 30px;
        }

        .info-item h3 {
            color: #ffd700;
            margin-bottom: 0.5rem;
            font-size: 1.2rem;
        }

        .info-item p {
            line-height: 1.6;
        }

        .map-container {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            height: 450px;
            background: #e0e0e0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            padding: 3rem 5%;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .social-links {
            margin: 2rem 0;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: #ffd700;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .tagline {
                font-size: 1.2rem;
            }

            .about-content,
            .location-content {
                grid-template-columns: 1fr;
            }

            nav ul {
                display: none;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">🍬 Sandesh Bengali Sweets</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Products</a></li>
                <li><a href="#location">Location</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Sandesh Bengali Sweets</h1>
            <p class="tagline">Experience the Authentic Taste of Bengal in Mumbai</p>
            <div class="rating">
                <span class="stars">⭐⭐⭐⭐</span>
                <span class="rating-text">3.9 Rating</span>
            </div>
            <div class="cta-buttons">
                <a href="tel:09029441441" class="btn btn-primary">📞 Call Now</a>
                <a href="#location" class="btn btn-secondary">📍 Visit Us</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title fade-in">About Our Legacy</h2>
            <div class="about-content">
                <div class="about-text fade-in">
                    <p>Welcome to Sandesh Bengali Sweets, Mumbai's premier destination for authentic Bengali delicacies. Located in the heart of Matunga West, we bring the rich culinary heritage of Bengal to your doorstep.</p>
                    <p>Our commitment to quality and authenticity has made us a trusted name among sweet lovers. Every sweet is crafted with traditional recipes passed down through generations, using only the finest ingredients.</p>
                    <p>From the iconic Rosogolla to the delicate Sandesh, each creation is a testament to our dedication to preserving the authentic Bengali taste while maintaining the highest standards of hygiene and quality.</p>
                </div>
                <div class="about-image fade-in">
                    <svg width="400" height="400" viewBox="0 0 400 400">
                        <circle cx="200" cy="200" r="180" fill="#f5deb3"/>
                        <circle cx="200" cy="200" r="140" fill="#daa520"/>
                        <circle cx="200" cy="200" r="100" fill="#cd853f"/>
                        <text x="200" y="210" font-size="60" text-anchor="middle" fill="#8B4513">🍬</text>
                    </svg>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title fade-in">Our Specialties</h2>
            <div class="services-grid">
                <div class="service-card fade-in">
                    <div class="service-icon">🥮</div>
                    <h3>Traditional Sandesh</h3>
                    <p>Handcrafted fresh daily with authentic Bengali recipes using premium cottage cheese and pure ingredients.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">🍡</div>
                    <h3>Rosogolla & Rasgulla</h3>
                    <p>Soft, spongy, and perfectly sweet - our signature rosogollas melt in your mouth with every bite.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">🍮</div>
                    <h3>Mishti Doi</h3>
                    <p>Sweet yogurt prepared the traditional way, offering the authentic taste of Bengal's beloved dessert.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">🎂</div>
                    <h3>Special Occasion Orders</h3>
                    <p>Custom sweet boxes and bulk orders for festivals, celebrations, and corporate gifting needs.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">🥛</div>
                    <h3>Fresh Daily Production</h3>
                    <p>All our sweets are prepared fresh daily ensuring maximum freshness and uncompromising quality.</p>
                </div>
                <div class="service-card fade-in">
                    <div class="service-icon">✨</div>
                    <h3>Premium Quality</h3>
                    <p>We use only the finest ingredients with strict quality control to deliver the best Bengali sweets.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Location Section -->
    <section id="location" class="location">
        <div class="container">
            <h2 class="section-title fade-in">Visit Our Store</h2>
            <div class="location-content">
                <div class="location-info fade-in">
                    <div class="info-item">
                        <div class="info-icon">📍</div>
                        <div>
                            <h3>Address</h3>
                            <p>Lokmanya Nagar, Ganha Vihaar<br>Matunga West<br>Mumbai, Maharashtra 400016</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">📞</div>
                        <div>
                            <h3>Contact Number</h3>
                            <p><a href="tel:09029441441" style="color: white; text-decoration: none;">090294 41441</a></p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🕐</div>
                        <div>
                            <h3>Opening Hours</h3>
                            <p>Monday - Sunday<br>9:00 AM - 9:00 PM</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⭐</div>
                        <div>
                            <h3>Customer Rating</h3>
                            <p>3.9/5 - Trusted by thousands of satisfied customers</p>
                        </div>
                    </div>
                </div>
                <div class="map-container fade-in">
                    <svg width="100%" height="100%" viewBox="0 0 400 400">
                        <rect width="400" height="400" fill="#e0e0e0"/>
                        <circle cx="200" cy="200" r="60" fill="#8B4513" opacity="0.3"/>
                        <circle cx="200" cy="200" r="40" fill="#8B4513" opacity="0.5"/>
                        <circle cx="200" cy="200" r="20" fill="#8B4513"/>
                        <path d="M200 180 L200 200 L210 210" stroke="#ffd700" stroke-width="3" fill="none"/>
                        <text x="200" y="260" font-size="16" text-anchor="middle" fill="#333">Sandesh Bengali Sweets</text>
                        <text x="200" y="280" font-size="14" text-anchor="middle" fill="#666">Matunga West, Mumbai</text>
                    </svg>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="footer-content">
            <h3>Sandesh Bengali Sweets</h3>
            <p>Experience the authentic taste of Bengal</p>
            <div class="social-links">
                <a href="tel:09029441441">📞</a>
                <a href="#location">📍</a>
                <a href="#">📧</a>
            </div>
            <p>&copy; 2024 Sandesh Bengali Sweets. All rights reserved.</p>
            <p>Lokmanya Nagar, Ganha Vihaar, Matunga West, Mumbai - 400016</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Scroll animations
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

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // Navbar background on scroll
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 100) {
                nav.style.background = 'rgba(139, 69, 19, 0.98)';
            } else {
                nav.style.background = 'rgba(139, 69, 19, 0.95)';
            }
        });
    </script>
</body>
</html>
