<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dur-e-Maknoon Nisar - AI Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 25%, #16213e  50%, #0f0f23 100%);
            color: #ffffff;
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
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: linear-gradient(45deg, #ff6b9d, #4ecdc4);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.3; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 1; }
        }

        /* Glass morphism container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Hero section with gradient and glow effects */
        .hero {
            background: linear-gradient(135deg, rgba(255, 107, 157, 0.1) 0%, rgba(78, 205, 196, 0.1) 100%);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 30px;
            padding: 60px 40px;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 107, 157, 0.05), transparent);
            animation: rotate 10s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .profile-avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            font-weight: bold;
            box-shadow: 0 0 50px rgba(255, 107, 157, 0.5);
            animation: pulse 3s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); box-shadow: 0 0 50px rgba(255, 107, 157, 0.5); }
            50% { transform: scale(1.05); box-shadow: 0 0 80px rgba(78, 205, 196, 0.7); }
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4, #ffe66d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(255, 107, 157, 0.3)); }
            to { filter: drop-shadow(0 0 30px rgba(78, 205, 196, 0.5)); }
        }

        .hero-subtitle {
            font-size: 1.5rem;
            color: #b0b0b0;
            margin-bottom: 30px;
        }

        .typing-animation {
            border-right: 2px solid #ff6b9d;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { border-color: transparent; }
            51%, 100% { border-color: #ff6b9d; }
        }

        /* Stats cards with hover effects */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.6s;
        }

        .stat-card:hover::before {
            left: 100%;
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 25px 80px rgba(255, 107, 157, 0.2);
            border-color: rgba(255, 107, 157, 0.3);
        }

        .stat-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: #ff6b9d;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #b0b0b0;
            font-weight: 500;
        }

        /* Project showcase with advanced animations */
        .projects-section {
            margin-bottom: 50px;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 50px;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 40px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 25px;
            padding: 40px;
            position: relative;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #ff6b9d, #4ecdc4, #ffe66d, #ff6b9d);
            border-radius: 25px;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.5s;
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 100px rgba(0, 0, 0, 0.4);
        }

        .project-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .project-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 700;
            color: #ffffff;
        }

        .project-description {
            color: #b0b0b0;
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 25px;
        }

        .tech-tag {
            background: rgba(255, 107, 157, 0.2);
            border: 1px solid rgba(255, 107, 157, 0.3);
            color: #ff6b9d;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .tech-tag:hover {
            background: rgba(255, 107, 157, 0.3);
            transform: scale(1.05);
        }

        /* Skills section with animated progress bars */
        .skills-section {
            margin-bottom: 50px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 30px;
        }

        .skill-category h3 {
            color: #ff6b9d;
            margin-bottom: 25px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-item {
            margin-bottom: 20px;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, #ff6b9d, #4ecdc4);
            border-radius: 4px;
            transition: width 2s ease-in-out;
            position: relative;
        }

        .skill-progress::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        /* Contact section with social links */
        .contact-section {
            text-align: center;
            padding: 60px 40px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 30px;
            margin-bottom: 40px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: white;
            font-size: 24px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            transition: all 0.4s ease;
            transform: translate(-50%, -50%);
        }

        .social-link:hover::before {
            width: 100%;
            height: 100%;
        }

        .social-link:hover {
            transform: translateY(-10px) scale(1.1);
            box-shadow: 0 20px 40px rgba(255, 107, 157, 0.4);
        }

        /* Floating action button */
        .fab {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #ff6b9d, #4ecdc4);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(255, 107, 157, 0.3);
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .fab:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 40px rgba(255, 107, 157, 0.5);
        }

        /* Responsive design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero {
                padding: 40px 20px;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-grid {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
        }

        /* Scroll animations */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .animate-on-scroll.animated {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Animated background particles -->
    <div class="particles"></div>

    <div class="container">
        <!-- Hero Section -->
        <section class="hero animate-on-scroll">
            <div class="hero-content">
                <div class="profile-avatar">D</div>
                <h1>Dur-e-Maknoon Nisar</h1>
                <p class="hero-subtitle">
                    <span class="typing-animation">AI Engineer | Disaster Management Innovator | Tech Visionary</span>
                </p>
                <p style="color: #b0b0b0; max-width: 600px; margin: 0 auto;">
                    Transforming complex challenges into innovative, data-driven solutions. Building AI-powered disaster prediction systems and creating geospatial intelligence for emergency response.
                </p>
            </div>
        </section>

        <!-- Stats Section -->
        <section class="stats-grid">
            <div class="stat-card animate-on-scroll">
                <div class="stat-icon">🚀</div>
                <div class="stat-number">5+</div>
                <div class="stat-label">Years Experience</div>
            </div>
            <div class="stat-card animate-on-scroll">
                <div class="stat-icon">🏆</div>
                <div class="stat-number">3</div>
                <div class="stat-label">Hackathon Wins</div>
            </div>
            <div class="stat-card animate-on-scroll">
                <div class="stat-icon">📊</div>
                <div class="stat-number">220M+</div>
                <div class="stat-label">Citizens Served</div>
            </div>
            <div class="stat-card animate-on-scroll">
                <div class="stat-icon">🎯</div>
                <div class="stat-number">95%</div>
                <div class="stat-label">Prediction Accuracy</div>
            </div>
        </section>

        <!-- Featured Projects -->
        <section class="projects-section">
            <h2 class="section-title animate-on-scroll">🚀 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card animate-on-scroll">
                    <div class="project-header">
                        <div class="project-icon">🌪️</div>
                        <div class="project-title">Climate Prediction System</div>
                    </div>
                    <p class="project-description">
                        Revolutionary AI-powered platform providing real-time smog and temperature forecasting for Pakistan's major cities with 95% prediction accuracy.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Prophet ML</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">PostgreSQL</span>
                    </div>
                </div>

                <div class="project-card animate-on-scroll">
                    <div class="project-header">
                        <div class="project-icon">🤖</div>
                        <div class="project-title">Multi-Agent AI HR Platform</div>
                    </div>
                    <p class="project-description">
                        Enterprise-grade AI platform revolutionizing HR operations through intelligent automation and conversational AI with voice-enabled interface.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">LangChain</span>
                        <span class="tech-tag">GPT-4</span>
                        <span class="tech-tag">ChromaDB</span>
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">FastAPI</span>
                    </div>
                </div>

                <div class="project-card animate-on-scroll">
                    <div class="project-header">
                        <div class="project-icon">🗺️</div>
                        <div class="project-title">Geospatial AI Anomaly Detection</div>
                    </div>
                    <p class="project-description">
                        Advanced geospatial intelligence system analyzing subsurface magnetic anomalies for disaster risk assessment using Google Earth Engine.
                    </p>
                    <div class="tech-stack">
                        <span class="tech-tag">Google Earth Engine</span>
                        <span class="tech-tag">Python ML</span>
                        <span class="tech-tag">QGIS</span>
                        <span class="tech-tag">JavaScript</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section class="skills-section">
            <h2 class="section-title animate-on-scroll">💻 Technical Expertise</h2>
            <div class="skills-grid">
                <div class="skill-category animate-on-scroll">
                    <h3>🧠 AI & Machine Learning</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Computer Vision</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Generative AI</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Time Series Analysis</span>
                            <span>92%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 92%"></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category animate-on-scroll">
                    <h3>💻 Development</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Python</span>
                            <span>98%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 98%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>React/JavaScript</span>
                            <span>88%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 88%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>FastAPI/Django</span>
                            <span>94%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 94%"></div>
                        </div>
                    </div>
                </div>

                <div class="skill-category animate-on-scroll">
                    <h3>🌍 Geospatial & Cloud</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Google Earth Engine</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>QGIS/ArcMap</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>AWS/Docker</span>
                            <span>82%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 82%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="contact-section animate-on-scroll">
            <h2 style="margin-bottom: 20px; background: linear-gradient(135deg, #ff6b9d, #4ecdc4); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">Let's Connect & Build the Future Together</h2>
            <p style="color: #b0b0b0; max-width: 500px; margin: 0 auto;">
                Ready to collaborate on AI solutions that change the world? Let's transform ideas into impact!
            </p>
            <div class="social-links">
                <a href="mailto:duremaknoonnisar@gmail.com" class="social-link" title="Email">📧</a>
                <a href="https://www.linkedin.com/in/maknoonnisar" class="social-link" title="LinkedIn">💼</a>
                <a href="https://github.com/maknoonisar" class="social-link" title="GitHub">👨‍💻</a>
                <a href="https://leetcode.com/duremaknoon" class="social-link" title="LeetCode">💻</a>
            </div>
        </section>
    </div>

    <!-- Floating Action Button -->
    <div class="fab" onclick="scrollToTop()">↑</div>

    <script>
        // Create animated particles
        function createParticles() {
            const particlesContainer = document.querySelector('.particles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 4 + 4) + 's';
                particlesContainer.appendChild(particle);
            }
        }

        // Scroll animations
        function handleScrollAnimations() {
            const elements = document.querySelectorAll('.animate-on-scroll');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animated');
                    }
                });
            }, {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            });

            elements.forEach(element => {
                observer.observe(element);
            });
        }

        // Scroll to top function
        function scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }

        // Typing animation
        function initTypingAnimation() {
            const text = "AI Engineer | Disaster Management Innovator | Tech Visionary";
            const element = document.querySelector('.typing-animation');
            let index = 0;

            function type() {
                if (index < text.length) {
                    element.textContent = text.slice(0, index + 1);
                    index++;
                    setTimeout(type, 50);
                } else {
                    setTimeout(() => {
                        index = 0;
                        element.textContent = '';
                        type();
                    }, 3000);
                }
            }

            type();
        }

        // Skill bar animations
        function animateSkillBars() {
            const skillBars = document.querySelectorAll('.skill-progress');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const width = entry.target.style.width;
                        entry.target.style.width = '0%';
                        setTimeout(() => {
                            entry.target.style.width = width;
                        }, 200);
                    }
                });
            }, {
                threshold: 0.5
            });

            skillBars.forEach(bar => {
                observer.observe(bar);
            });
        }

        // Initialize everything
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            handleScrollAnimations();
            initTypingAnimation();
            animateSkillBars();
        });

        // Smooth scrolling for internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Dynamic gradient on mouse move
        document.addEventListener('mousemove', (e) => {
            const hero = document.querySelector('.hero');
            const rect = hero.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            if (x >= 0 && x <= rect.width && y >= 0 && y <= rect.height) {
                const xPercent = (x / rect.width) * 100;
                const yPercent = (y / rect.height) * 100;
                hero.style.background = `radial-gradient(circle at ${xPercent}% ${yPercent}%, rgba(255, 107, 157, 0.15) 0%, rgba(78, 205, 196, 0.05) 50%, transparent 100%)`;
            }
        });
