<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Excel Electricals | Leading Electrical Solutions & Equipment</title>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary: #004b93;
            --primary-dark: #003366;
            --accent: #ff9900;
            --accent-hover: #e68a00;
            --text-dark: #1e293b;
            --text-light: #64748b;
            --bg-light: #f8fafc;
            --white: #ffffff;
            --border: #e2e8f0;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            color: var(--text-dark);
            background-color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        /* --- HEADER & TOPBAR --- */
        .top-bar {
            background-color: var(--primary-dark);
            color: var(--white);
            font-size: 0.85rem;
            padding: 8px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-info span {
            margin-right: 20px;
        }

        .top-info i {
            color: var(--accent);
            margin-right: 6px;
        }

        header {
            position: sticky;
            top: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 15px rgba(0,0,0,0.05);
            z-index: 1000;
            transition: var(--transition);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
        }

        .logo i {
            color: var(--accent);
            font-size: 1.8rem;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .nav-links a {
            font-weight: 500;
            font-size: 0.95rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--accent);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            outline: none;
            text-align: center;
        }

        .btn-primary {
            background-color: var(--accent);
            color: var(--white);
        }

        .btn-primary:hover {
            background-color: var(--accent-hover);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 153, 0, 0.3);
        }

        .btn-outline {
            border: 2px solid var(--white);
            color: var(--white);
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--primary);
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary);
        }

        /* --- HERO SECTION --- */
        .hero {
            background: linear-gradient(135deg, rgba(0, 75, 147, 0.92), rgba(0, 30, 60, 0.95)), url('https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
            color: var(--white);
            padding: 120px 5% 100px;
            min-height: 85vh;
            display: flex;
            align-items: center;
        }

        .hero-container {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .hero-text h1 {
            font-size: 3.2rem;
            line-height: 1.2;
            margin-bottom: 20px;
            font-weight: 800;
        }

        .hero-text h1 span {
            color: var(--accent);
        }

        .hero-text p {
            font-size: 1.1rem;
            margin-bottom: 35px;
            opacity: 0.9;
            max-width: 550px;
        }

        .hero-btns {
            display: flex;
            gap: 15px;
        }

        .hero-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 25px;
            border-radius: 12px;
            text-align: center;
        }

        .stat-card h3 {
            font-size: 2.2rem;
            color: var(--accent);
            margin-bottom: 5px;
        }

        .stat-card p {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        /* --- SECTION COMMONS --- */
        section {
            padding: 90px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header span {
            color: var(--accent);
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 1.5px;
        }

        .section-header h2 {
            font-size: 2.4rem;
            color: var(--primary-dark);
            margin-top: 5px;
        }

        /* --- ABOUT SECTION --- */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-img {
            position: relative;
        }

        .about-img img {
            width: 100%;
            border-radius: 12px;
            box-shadow: var(--shadow);
        }

        .experience-badge {
            position: absolute;
            bottom: -20px;
            right: -20px;
            background: var(--primary);
            color: var(--white);
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .experience-badge h4 {
            font-size: 2rem;
            color: var(--accent);
            line-height: 1;
        }

        .about-content h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .about-content p {
            color: var(--text-light);
            margin-bottom: 20px;
        }

        .feature-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 30px;
        }

        .feature-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
        }

        .feature-item i {
            color: var(--accent);
        }

        /* --- SERVICES SECTION --- */
        .services-bg {
            background-color: var(--bg-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--white);
            padding: 35px 25px;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.03);
            transition: var(--transition);
            border-bottom: 3px solid transparent;
        }

        .service-card:hover {
            transform: translateY(-8px);
            border-bottom: 3px solid var(--accent);
            box-shadow: var(--shadow);
        }

        .service-icon {
            width: 65px;
            height: 65px;
            background: rgba(0, 75, 147, 0.08);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .service-card h3 {
            font-size: 1.3rem;
            margin-bottom: 12px;
        }

        .service-card p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* --- PRODUCTS CATALOG SECTION --- */
        .product-filters {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 8px 20px;
            border-radius: 30px;
            border: 1px solid var(--border);
            background: var(--white);
            cursor: pointer;
            font-weight: 500;
            transition: var(--transition);
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--primary);
            color: var(--white);
            border-color: var(--primary);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 30px;
        }

        .product-card {
            border: 1px solid var(--border);
            border-radius: 12px;
            overflow: hidden;
            transition: var(--transition);
            background: var(--white);
        }

        .product-card:hover {
            box-shadow: var(--shadow);
            transform: translateY(-5px);
        }

        .product-img {
            height: 200px;
            background: #f1f5f9;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: var(--primary);
        }

        .product-info {
            padding: 20px;
        }

        .product-info h4 {
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .product-info p {
            color: var(--text-light);
            font-size: 0.85rem;
            margin-bottom: 15px;
        }

        .product-info .btn-sm {
            padding: 8px 16px;
            font-size: 0.85rem;
            width: 100%;
        }

        /* --- FAQ ACCORDION --- */
        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            background: var(--bg-light);
            border-radius: 8px;
            margin-bottom: 15px;
            overflow: hidden;
        }

        .faq-question {
            padding: 20px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .faq-answer {
            padding: 0 20px 20px 20px;
            color: var(--text-light);
            display: none;
            font-size: 0.95rem;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        .faq-item.active .faq-question i {
            transform: rotate(180deg);
        }

        /* --- CONTACT & QUOTE SECTION --- */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 50px;
        }

        .contact-info-card {
            background: var(--primary);
            color: var(--white);
            padding: 40px;
            border-radius: 12px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 30px;
        }

        .info-item i {
            font-size: 1.5rem;
            color: var(--accent);
            margin-top: 5px;
        }

        .contact-form {
            background: var(--white);
            padding: 40px;
            border-radius: 12px;
            border: 1px solid var(--border);
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            font-size: 0.9rem;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid var(--border);
            border-radius: 6px;
            font-size: 1rem;
            outline: none;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--primary);
        }

        textarea.form-control {
            resize: vertical;
            min-height: 120px;
        }

        /* --- FOOTER --- */
        footer {
            background: var(--primary-dark);
            color: var(--white);
            padding: 70px 5% 20px;
        }

        .footer-grid {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1.5fr;
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-col h4 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: var(--white);
            position: relative;
        }

        .footer-col h4::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -8px;
            width: 30px;
            height: 2px;
            background: var(--accent);
        }

        .footer-col p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            margin-bottom: 20px;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            transition: var(--transition);
            font-size: 0.9rem;
        }

        .footer-links a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.85rem;
            color: rgba(255, 255, 255, 0.5);
        }

        /* --- MODAL --- */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.6);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: var(--white);
            padding: 40px;
            border-radius: 12px;
            max-width: 500px;
            width: 90%;
            position: relative;
        }

        .close-modal {
            position: absolute;
            right: 20px;
            top: 20px;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-light);
        }

        /* --- RESPONSIVE DESIGN --- */
        @media (max-width: 992px) {
            .hero-container, .about-grid, .contact-grid {
                grid-template-columns: 1fr;
            }
            .hero-text h1 {
                font-size: 2.5rem;
            }
            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--white);
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 10px 10px rgba(0,0,0,0.1);
            }

            .nav-links.active {
                display: flex;
            }

            .mobile-menu-btn {
                display: block;
            }

            .top-bar {
                flex-direction: column;
                gap: 5px;
                text-align: center;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- TOP HEADER BAR -->
    <div class="top-bar">
        <div class="top-info">
            <span><i class="fa-solid fa-phone"></i> +91 98258 51819</span>
            <span><i class="fa-solid fa-envelope"></i> info@excelelctricals.co.in</span>
        </div>
        <div class="top-info">
            <span><i class="fa-solid fa-location-dot"></i> India</span>
            <span><i class="fa-solid fa-clock"></i> Mon - Sat: 9:00 AM - 7:00 PM</span>
        </div>
    </div>

    <!-- MAIN NAVIGATION -->
    <header>
        <nav class="navbar">
            <a href="#" class="logo">
                <i class="fa-solid fa-bolt"></i> Excel Electricals
            </a>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <button class="btn btn-primary" onclick="openModal()">Get Quote</button>
            <div class="mobile-menu-btn" onclick="toggleMenu()">
                <i class="fa-solid fa-bars"></i>
            </div>
        </nav>
    </header>

    <!-- HERO SECTION -->
    <section id="home" class="hero">
        <div class="hero-container">
            <div class="hero-text">
                <h1>Powering Excellence with <span>Reliable Electrical</span> Solutions</h1>
                <p>We provide industrial and commercial electrical infrastructure, high-grade motor components, earthing, transformer maintenance, and turn-key power setups.</p>
                <div class="hero-btns">
                    <a href="#products" class="btn btn-primary">Explore Products</a>
                    <a href="#contact" class="btn btn-outline">Contact Us</a>
                </div>
            </div>
            <div class="hero-stats">
                <div class="stat-card">
                    <h3>25+</h3>
                    <p>Years Experience</p>
                </div>
                <div class="stat-card">
                    <h3>1200+</h3>
                    <p>Projects Delivered</p>
                </div>
                <div class="stat-card">
                    <h3>100%</h3>
                    <p>ISO & Safety Compliant</p>
                </div>
                <div class="stat-card">
                    <h3>24/7</h3>
                    <p>Technical Support</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about">
        <div class="about-grid">
            <div class="about-img">
                <img src="https://images.unsplash.com/photo-1581092160607-ee22621dd758?auto=format&fit=crop&w=800&q=80" alt="Electrical Engineers">
                <div class="experience-badge">
                    <h4>25+</h4>
                    <p>Years of Trust</p>
                </div>
            </div>
            <div class="about-content">
                <div class="section-header" style="text-align: left; margin-bottom: 20px;">
                    <span>About Excel Electricals</span>
                    <h2>Engineered for Safety, Designed for Performance</h2>
                </div>
                <p>At <strong>excelelctricals.co.in</strong>, we are dedicated to setting high standards in electrical manufacturing, equipment distribution, and maintenance services. Serving both industrial setups and commercial infrastructure, our team ensures maximum operational uptime and complete safety.</p>
                <p>From complex panel fabrications and transformer overhauls to precision motor replacement components, our solutions comply with global quality standards.</p>
                <div class="feature-list">
                    <div class="feature-item"><i class="fa-solid fa-circle-check"></i> Certified Engineering</div>
                    <div class="feature-item"><i class="fa-solid fa-circle-check"></i> Turnkey Installation</div>
                    <div class="feature-item"><i class="fa-solid fa-circle-check"></i> Premium Equipment</div>
                    <div class="feature-item"><i class="fa-solid fa-circle-check"></i> Rapid Site Support</div>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <div class="services-bg">
        <section id="services">
            <div class="section-header">
                <span>Our Expertise</span>
                <h2>Comprehensive Electrical Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-plug"></i></div>
                    <h3>Turnkey Electrical Setup</h3>
                    <p>End-to-end electrical design, panel installation, and cabling infrastructure for factories and commercial facilities.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-car-battery"></i></div>
                    <h3>Transformer Maintenance</h3>
                    <p>Overhauling, oil filtration, and routine preventive inspection of oil-cooled distribution and special purpose transformers.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-shield-halved"></i></div>
                    <h3>Earthing & Surge Protection</h3>
                    <p>Advanced copper bonded earthing system designs and lightning arrestor setups protecting critical electrical infrastructure.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-industry"></i></div>
                    <h3>Motor Component Supply</h3>
                    <p>High-precision manufacturing and distribution of motor bodies, terminal plates, cooling fans, and fan covers.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-wrench"></i></div>
                    <h3>Facility Maintenance</h3>
                    <p>On-demand onsite repair, troubleshooting, load analysis, and power factor correction services.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fa-solid fa-fire-extinguisher"></i></div>
                    <h3>Fire & Alarm Systems</h3>
                    <p>Installation and integration of industrial fire protection panels, smoke sensors, and emergency cutoff controls.</p>
                </div>
            </div>
        </section>
    </div>

    <!-- PRODUCTS CATALOG SECTION -->
    <section id="products">
        <div class="section-header">
            <span>Our Catalog</span>
            <h2>Featured Products & Components</h2>
        </div>
        <div class="product-filters">
            <button class="filter-btn active" onclick="filterProducts('all')">All Products</button>
            <button class="filter-btn" onclick="filterProducts('motors')">Motor Parts</button>
            <button class="filter-btn" onclick="filterProducts('transformers')">Transformers</button>
            <button class="filter-btn" onclick="filterProducts('earthing')">Earthing Solutions</button>
        </div>

        <div class="product-grid">
            <div class="product-card" data-category="motors">
                <div class="product-img"><i class="fa-solid fa-gear"></i></div>
                <div class="product-info">
                    <h4>Bakelite Terminal Plate</h4>
                    <p>Heat-resistant terminal plates manufactured for heavy-duty electric motor connections.</p>
                    <button class="btn btn-primary btn-sm" onclick="openModal()">Inquire Now</button>
                </div>
            </div>
            <div class="product-card" data-category="motors">
                <div class="product-img"><i class="fa-solid fa-fan"></i></div>
                <div class="product-info">
                    <h4>Plastic & MS Cooling Fans</h4>
                    <p>Durable cooling fans and MS fan covers engineered for optimum motor airflow.</p>
                    <button class="btn btn-primary btn-sm" onclick="openModal()">Inquire Now</button>
                </div>
            </div>
            <div class="product-card" data-category="transformers">
                <div class="product-img"><i class="fa-solid fa-bolt-lightning"></i></div>
                <div class="product-info">
                    <h4>Distribution Transformer</h4>
                    <p>Standard and custom oil-cooled distribution transformers built to IS standards.</p>
                    <button class="btn btn-primary btn-sm" onclick="openModal()">Inquire Now</button>
                </div>
            </div>
            <div class="product-card" data-category="earthing">
                <div class="product-img"><i class="fa-solid fa-tower-cell"></i></div>
                <div class="product-info">
                    <h4>Copper Bonded Earth Rod</h4>
                    <p>High conductivity, corrosion-resistant rods engineered for fault dispersal.</p>
                    <button class="btn btn-primary btn-sm" onclick="openModal()">Inquire Now</button>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <div class="services-bg">
        <section id="faq">
            <div class="section-header">
                <span>Frequently Asked Questions</span>
                <h2>Got Questions? We Have Answers.</h2>
            </div>
            <div class="faq-container">
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        What services does Excel Electricals offer?
                        <i class="fa-solid fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        We specialize in manufacturing motor parts, site oil filtration for transformers, earthing/lightning protection installation, and complete electrical contracting for commercial and industrial projects.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        Do you offer custom product dimensions?
                        <i class="fa-solid fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        Yes! We produce special-sized terminal plates, motor bodies, and customized transformer units tailored specifically to your project requirements.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        How can I request an onsite inspection or quote?
                        <i class="fa-solid fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        You can fill out our "Get Quote" form on this website or call us directly. Our engineering staff will respond within 24 hours.
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- CONTACT & QUOTE SECTION -->
    <section id="contact">
        <div class="section-header">
            <span>Contact Us</span>
            <h2>Get In Touch With Our Technical Team</h2>
        </div>
        <div class="contact-grid">
            <div class="contact-info-card">
                <div>
                    <h3>Excel Electricals</h3>
                    <p style="margin-top: 10px; opacity: 0.8;">Partnering with you for high-performance power and electrical equipment solutions.</p>
                    <br><br>
                    <div class="info-item">
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <strong>Head Office & Works</strong>
                            <p>Industrial Estate Zone, India</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <i class="fa-solid fa-phone"></i>
                        <div>
                            <strong>Call Us</strong>
                            <p>+91 98258 51819 / (079) 22741006</p>
                        </div>
                    </div>
                    <div class="info-item">
                        <i class="fa-solid fa-envelope"></i>
                        <div>
                            <strong>Email</strong>
                            <p>info@excelelctricals.co.in</p>
                        </div>
                    </div>
                </div>
                <div style="font-size: 0.85rem; opacity: 0.7;">
                    www.excelelctricals.co.in &copy; All Rights Reserved.
                </div>
            </div>

            <div class="contact-form">
                <form id="mainContactForm" onsubmit="handleFormSubmit(event)">
                    <div class="form-group">
                        <label for="name">Your Name</label>
                        <input type="text" id="name" class="form-control" placeholder="John Doe" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" class="form-control" placeholder="john@example.com" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone Number</label>
                        <input type="tel" id="phone" class="form-control" placeholder="+91 00000 00000" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Project Details / Message</label>
                        <textarea id="message" class="form-control" placeholder="Describe your requirement..." required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <h4>Excel Electricals</h4>
                <p>Your trustworthy manufacturing & contracting partner for high-grade electrical equipment, specialized motor accessories, and earthing setups.</p>
            </div>
            <div class="footer-col">
                <h4>Quick Links</h4>
                <ul class="footer-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#contact">Contact Us</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Products</h4>
                <ul class="footer-links">
                    <li><a href="#products">Terminal Plates</a></li>
                    <li><a href="#products">Cooling Fans & Covers</a></li>
                    <li><a href="#products">Distribution Transformers</a></li>
                    <li><a href="#products">Earthing Systems</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4>Newsletter</h4>
                <p>Subscribe to receive product updates and company news.</p>
                <input type="email" class="form-control" placeholder="Enter your email" style="margin-bottom: 10px;">
                <button class="btn btn-primary" style="width:100%;">Subscribe</button>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2026 excelelctricals.co.in. All Rights Reserved.</p>
        </div>
    </footer>

    <!-- REQUEST QUOTE MODAL -->
    <div class="modal" id="quoteModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">&times;</span>
            <h3 style="margin-bottom: 15px; color: var(--primary);">Request a Fast Quote</h3>
            <form onsubmit="handleFormSubmit(event)">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" class="form-control" required>
                </div>
                <div class="form-group">
                    <label>Phone Number</label>
                    <input type="tel" class="form-control" required>
                </div>
                <div class="form-group">
                    <label>Product / Service Required</label>
                    <select class="form-control">
                        <option>Motor Parts</option>
                        <option>Transformers & Overhaul</option>
                        <option>Earthing & Protection</option>
                        <option>Turnkey Installation</option>
                    </select>
                </div>
                <button type="submit" class="btn btn-primary" style="width: 100%;">Submit Request</button>
            </form>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Mobile Navigation Menu Toggle
        function toggleMenu() {
            const navLinks = id('navLinks');
            navLinks.classList.toggle('active');
        }

        function id(e) { return document.getElementById(e); }

        // Product Category Filter Function
        function filterProducts(category) {
            const buttons = document.querySelectorAll('.filter-btn');
            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');

            const cards = document.querySelectorAll('.product-card');
            cards.forEach(card => {
                if(category === 'all' || card.getAttribute('data-category') === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Accordion functionality for FAQs
        function toggleFaq(element) {
            const parent = element.parentElement;
            parent.classList.toggle('active');
        }

        // Modal Handlers
        function openModal() {
            id('quoteModal').style.display = 'flex';
        }

        function closeModal() {
            id('quoteModal').style.display = 'none';
        }

        window.onclick = function(event) {
            const modal = id('quoteModal');
            if (event.target === modal) {
                closeModal();
            }
        }

        // Form Submission Handler
        function handleFormSubmit(event) {
            event.preventDefault();
            alert('Thank you for contacting Excel Electricals! We will get back to you shortly.');
            closeModal();
            if(event.target.id === 'mainContactForm') {
                event.target.reset();
            }
        }
    </script>
</body>
</html>
