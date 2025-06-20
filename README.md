# Roomie
Advertise Real Estate Projects
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Roomie - Global Real Estate Marketplace</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary: #4f46e5;
            --primary-dark: #4338ca;
            --secondary: #10b981;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #94a3b8;
            --danger: #ef4444;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f1f5f9;
            color: var(--dark);
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 1rem 2rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 0.5rem;
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .auth-buttons .btn {
            margin-left: 1rem;
        }
        
        .btn {
            padding: 0.5rem 1.5rem;
            border-radius: 0.375rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
        }
        
        .btn-primary {
            background-color: var(--secondary);
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #0d9e6e;
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1564013799919-ab600027ffc6?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 2rem;
        }
        
        .hero-content {
            max-width: 800px;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .search-bar {
            display: flex;
            max-width: 700px;
            margin: 0 auto;
            background-color: white;
            border-radius: 0.5rem;
            overflow: hidden;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .search-bar input {
            flex: 1;
            padding: 1rem;
            border: none;
            outline: none;
            font-size: 1rem;
        }
        
        .search-bar button {
            padding: 0 1.5rem;
            background-color: var(--secondary);
            color: white;
            border: none;
            cursor: pointer;
            font-weight: 600;
        }
        
        /* Features Section */
        .features {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 0.5rem;
            padding: 2rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .feature-card p {
            color: var(--gray);
            line-height: 1.6;
        }
        
        /* Properties Section */
        .properties {
            padding: 5rem 2rem;
            background-color: #f8fafc;
        }
        
        .properties-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .property-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .property-card {
            background-color: white;
            border-radius: 0.5rem;
            overflow: hidden;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .property-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .property-image {
            height: 250px;
            overflow: hidden;
        }
        
        .property-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .property-card:hover .property-image img {
            transform: scale(1.05);
        }
        
        .property-details {
            padding: 1.5rem;
        }
        
        .property-price {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .property-address {
            color: var(--gray);
            margin-bottom: 1rem;
        }
        
        .property-features {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .property-feature {
            display: flex;
            align-items: center;
            color: var(--dark);
        }
        
        .property-feature i {
            margin-right: 0.5rem;
            color: var(--primary);
        }
        
        .property-actions {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background-color: white;
            border-radius: 0.5rem;
            padding: 2rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .author-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .author-info h4 {
            font-size: 1.1rem;
            margin-bottom: 0.2rem;
        }
        
        .author-info p {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 5rem 2rem;
            text-align: center;
        }
        
        .cta-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }
        
        .cta p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 4rem 2rem 2rem;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        .footer-logo i {
            margin-right: 0.5rem;
            color: var(--secondary);
        }
        
        .footer-about p {
            color: var(--gray);
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
        }
        
        .social-links a {
            color: white;
            font-size: 1.2rem;
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--secondary);
        }
        
        .footer-links h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        .footer-links h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--secondary);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .footer-contact p {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            color: var(--gray);
        }
        
        .footer-contact i {
            margin-right: 0.8rem;
            color: var(--secondary);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .nav-links, .auth-buttons {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .search-bar {
                flex-direction: column;
                background-color: transparent;
            }
            
            .search-bar input {
                margin-bottom: 1rem;
                border-radius: 0.5rem;
                padding: 1rem;
            }
            
            .search-bar button {
                width: 100%;
                padding: 1rem;
                border-radius: 0.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-home"></i>
                <span>Roomie</span>
            </div>
            
            <div class="nav-links">
                <a href="#">Home</a>
                <a href="#properties">Properties</a>
                <a href="#agents">Agents</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </div>
            
            <div class="auth-buttons">
                <button class="btn btn-outline">Login</button>
                <button class="btn btn-primary">Sign Up</button>
            </div>
            
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </nav>
    </header>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Find Your Dream Property Anywhere in the World</h1>
            <p>Discover and book properties from global real estate agents with seamless transactions</p>
            
            <div class="search-bar">
                <input type="text" placeholder="Search by location, property type, or price...">
                <button>Search</button>
            </div>
        </div>
    </section>
    
    <!-- Features Section -->
    <section class="features">
        <div class="section-title">
            <h2>Why Choose Roomie?</h2>
            <p>We provide the best platform for property buyers and real estate agents to connect globally</p>
        </div>
        
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-globe"></i>
                </div>
                <h3>Global Reach</h3>
                <p>Access properties from around the world in one platform. No matter where you want to buy, we've got you covered.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-shield-alt"></i>
                </div>
                <h3>Secure Transactions</h3>
                <p>Our platform ensures all transactions are secure with escrow protection and verified agents.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-bolt"></i>
                </div>
                <h3>Fast Processing</h3>
                <p>Complete your property purchase or booking in minutes with our streamlined process.</p>
            </div>
        </div>
    </section>
    
    <!-- Properties Section -->
    <section class="properties" id="properties">
        <div class="properties-container">
            <div class="section-title">
                <h2>Featured Properties</h2>
                <p>Explore our curated selection of premium properties from around the world</p>
            </div>
            
            <div class="property-grid">
                <!-- Property 1 -->
                <div class="property-card">
                    <div class="property-image">
                        <img src="https://images.unsplash.com/photo-1580587771525-78b9dba3b914?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Luxury Villa">
                    </div>
                    <div class="property-details">
                        <div class="property-price">$1,250,000</div>
                        <div class="property-address">Beverly Hills, California, USA</div>
                        <div class="property-features">
                            <div class="property-feature">
                                <i class="fas fa-bed"></i>
                                <span>5 Beds</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-bath"></i>
                                <span>4 Baths</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-ruler-combined"></i>
                                <span>3,500 sqft</span>
                            </div>
                        </div>
                        <div class="property-actions">
                            <button class="btn btn-outline" style="color: var(--dark); border-color: var(--gray);">Details</button>
                            <button class="btn btn-primary">Book Viewing</button>
                        </div>
                    </div>
                </div>
                
                <!-- Property 2 -->
                <div class="property-card">
                    <div class="property-image">
                        <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Modern Apartment">
                    </div>
                    <div class="property-details">
                        <div class="property-price">€850,000</div>
                        <div class="property-address">Berlin, Germany</div>
                        <div class="property-features">
                            <div class="property-feature">
                                <i class="fas fa-bed"></i>
                                <span>3 Beds</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-bath"></i>
                                <span>2 Baths</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-ruler-combined"></i>
                                <span>1,200 sqft</span>
                            </div>
                        </div>
                        <div class="property-actions">
                            <button class="btn btn-outline" style="color: var(--dark); border-color: var(--gray);">Details</button>
                            <button class="btn btn-primary">Book Viewing</button>
                        </div>
                    </div>
                </div>
                
                <!-- Property 3 -->
                <div class="property-card">
                    <div class="property-image">
                        <img src="https://images.unsplash.com/photo-1493809842364-78817add7ffb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Beach House">
                    </div>
                    <div class="property-details">
                        <div class="property-price">¥45,000,000</div>
                        <div class="property-address">Bali, Indonesia</div>
                        <div class="property-features">
                            <div class="property-feature">
                                <i class="fas fa-bed"></i>
                                <span>4 Beds</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-bath"></i>
                                <span>3 Baths</span>
                            </div>
                            <div class="property-feature">
                                <i class="fas fa-ruler-combined"></i>
                                <span>2,800 sqft</span>
                            </div>
                        </div>
                        <div class="property-actions">
                            <button class="btn btn-outline" style="color: var(--dark); border-color: var(--gray);">Details</button>
                            <button class="btn btn-primary">Book Viewing</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Testimonials -->
    <section class="testimonials">
        <div class="section-title">
            <h2>What Our Clients Say</h2>
            <p>Hear from people who have found their dream properties through Roomie</p>
        </div>
        
        <div class="testimonial-grid">
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "Roomie made buying my apartment in Barcelona so easy. The agent was professional and the transaction was seamless. 10/10 would recommend!"
                </div>
                <div class="testimonial-author">
                    <div class="author-avatar">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah Johnson">
                    </div>
                    <div class="author-info">
                        <h4>Sarah Johnson</h4>
                        <p>Property Buyer</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "As a real estate agent, Roomie has helped me reach international clients I never could have accessed before. The platform is intuitive and the commission structure is fair."
                </div>
                <div class="testimonial-author">
                    <div class="author-avatar">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Michael Chen">
                    </div>
                    <div class="author-info">
                        <h4>Michael Chen</h4>
                        <p>Real Estate Agent</p>
                    </div>
                </div>
            </div>
            
            <div class="testimonial-card">
                <div class="testimonial-text">
                    "I was skeptical about buying property online, but Roomie's verification process and secure payment system gave me confidence. Now I own a vacation home in Portugal!"
                </div>
                <div class="testimonial-author">
                    <div class="author-avatar">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Aisha Mohammed">
                    </div>
                    <div class="author-info">
                        <h4>Aisha Mohammed</h4>
                        <p>Property Investor</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section class="cta">
        <div class="cta-container">
            <h2>Ready to Find Your Dream Property?</h2>
            <p>Join thousands of satisfied buyers and agents in our global real estate marketplace</p>
            <div style="display: flex; gap: 1rem; justify-content: center;">
                <button class="btn btn-primary" style="padding: 1rem 2rem;">Browse Properties</button>
                <button class="btn btn-outline" style="padding: 1rem 2rem;">List Your Property</button>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-about">
                <div class="footer-logo">
                    <i class="fas fa-home"></i>
                    <span>Roomie</span>
                </div>
                <p>The global platform connecting property buyers with real estate agents worldwide. Secure transactions, verified listings, and seamless experiences.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
            
            <div class="footer-links">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#properties">Properties</a></li>
                    <li><a href="#agents">Agents</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            
            <div class="footer-links">
                <h3>Categories</h3>
                <ul>
                    <li><a href="#">Residential</a></li>
                    <li><a href="#">Commercial</a></li>
                    <li><a href="#">Vacation Homes</a></li>
                    <li><a href="#">Luxury Properties</a></li>
                    <li><a href="#">Investment Properties</a></li>
                </ul>
            </div>
            
            <div class="footer-contact">
                <h3>Contact Us</h3>
                <p><i class="fas fa-map-marker-alt"></i> 123 Global Street, Suite 100, San Francisco, CA 94107</p>
                <p><i class="fas fa-phone-alt"></i> +1 (555) 123-4567</p>
                <p><i class="fas fa-envelope"></i> info@roomie.com</p>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 Roomie. All rights reserved. <a href="#" style="color: var(--secondary);">Terms & Conditions</a> | <a href="#" style="color: var(--secondary);">Privacy Policy</a></p>
        </div>
    </footer>
    
    <script>
        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        const authButtons = document.querySelector('.auth-buttons');
        
        mobileMenuBtn.addEventListener('click', () => {
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
            authButtons.style.display = authButtons.style.display === 'flex' ? 'none' : 'flex';
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Property card interaction
        document.querySelectorAll('.property-card').forEach(card => {
            card.addEventListener('click', (e) => {
                // Don't redirect if clicking on a button
                if (e.target.tagName === 'BUTTON' || e.target.parentElement.tagName === 'BUTTON') {
                    return;
                }
                
                // In a real app, this would redirect to property details page
                console.log('Redirecting to property details page');
            });
        });
    </script>
</body>
</html>
