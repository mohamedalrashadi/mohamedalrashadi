<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammed Al Rashadi - AI Engineer & Security Architect</title>
    <meta name="description" content="AI Engineer, Security Specialist, and Full-Stack Architect">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 100%);
            color: #fff;
            overflow-x: hidden;
        }

        /* Animated Background */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        /* Header Section */
        header {
            text-align: center;
            padding: 100px 20px 50px;
            background: linear-gradient(180deg, rgba(255,107,107,0.1) 0%, rgba(78,205,196,0.1) 100%);
        }

        h1 {
            font-size: 4rem;
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4, #FFD700);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 3s ease infinite;
            margin-bottom: 20px;
        }

        @keyframes gradient {
            0%, 100% { filter: hue-rotate(0deg); }
            50% { filter: hue-rotate(20deg); }
        }

        .subtitle {
            font-size: 1.5rem;
            color: #4ECDC4;
            margin-bottom: 30px;
        }

        .badges {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .badge {
            padding: 10px 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid #4ECDC4;
            border-radius: 25px;
            font-size: 0.9rem;
            transition: all 0.3s;
        }

        .badge:hover {
            background: #4ECDC4;
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(78, 205, 196, 0.3);
        }

        /* Stats Section */
        .stats-container {
            max-width: 1200px;
            margin: 50px auto;
            padding: 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(255, 107, 107, 0.2);
            border-color: #FF6B6B;
        }

        .stat-card img {
            width: 100%;
            border-radius: 10px;
        }

        /* Tech Stack Section */
        .tech-section {
            max-width: 1200px;
            margin: 80px auto;
            padding: 20px;
        }

        .tech-section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .tech-card {
            background: rgba(255, 255, 255, 0.05);
            border: 2px solid transparent;
            border-radius: 15px;
            padding: 30px;
            transition: all 0.3s;
            cursor: pointer;
        }

        .tech-card:hover {
            border-color: #4ECDC4;
            background: rgba(78, 205, 196, 0.1);
            transform: scale(1.05);
        }

        .tech-card h3 {
            color: #FFD700;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        .tech-list {
            list-style: none;
            padding: 0;
        }

        .tech-list li {
            padding: 8px 0;
            color: #4ECDC4;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .tech-list li:before {
            content: "▹ ";
            color: #FF6B6B;
            font-weight: bold;
        }

        /* Projects Section */
        .projects-section {
            max-width: 1200px;
            margin: 80px auto;
            padding: 20px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: #FF6B6B;
            box-shadow: 0 20px 40px rgba(255, 107, 107, 0.3);
        }

        .project-card img {
            width: 100%;
            height: auto;
        }

        /* Contact Section */
        .contact-section {
            max-width: 800px;
            margin: 80px auto;
            padding: 50px 20px;
            text-align: center;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
        }

        .contact-section h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
            color: #FFD700;
        }

        .social-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-btn {
            padding: 15px 30px;
            background: linear-gradient(45deg, #FF6B6B, #4ECDC4);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s;
            display: inline-block;
        }

        .social-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 10px 30px rgba(78, 205, 196, 0.5);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            background: rgba(0, 0, 0, 0.3);
            margin-top: 80px;
        }

        .view-counter {
            margin-top: 20px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            .subtitle {
                font-size: 1.2rem;
            }

            .stats-container {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 0.8s forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <!-- Animated Stars Background -->
    <div class="stars" id="stars"></div>

    <!-- Header Section -->
    <header>
        <h1>MOHAMMED AL RASHADI</h1>
        <p class="subtitle">AI Engineer | Security Specialist | Full-Stack Architect</p>
        
        <div class="badges">
            <span class="badge">⚡ Neural Networks Active</span>
            <span class="badge">🛡️ Security Hardened</span>
            <span class="badge">🚀 Quantum Ready</span>
            <span class="badge">🌐 Cloud Native</span>
        </div>
    </header>

    <!-- Stats Section -->
    <section class="stats-container">
        <div class="stat-card fade-in">
            <img src="https://github-readme-stats.vercel.app/api?username=mohamedalrashadi&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&icon_color=4ECDC4&text_color=00D9FF&ring_color=F7B731&count_private=true&include_all_commits=true&rank_icon=github" alt="GitHub Stats">
        </div>
        
        <div class="stat-card fade-in" style="animation-delay: 0.2s;">
            <img src="https://streak-stats.demolab.com/?user=mohamedalrashadi&theme=radical&hide_border=true&background=0D1117&ring=F7B731&fire=FF6B6B&currStreakLabel=4ECDC4" alt="Streak Stats">
        </div>
        
        <div class="stat-card fade-in" style="animation-delay: 0.4s;">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohamedalrashadi&layout=compact&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&text_color=00D9FF&langs_count=8" alt="Top Languages">
        </div>
    </section>

    <!-- Activity Graph -->
    <section class="stats-container">
        <div class="stat-card fade-in" style="grid-column: 1 / -1;">
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=mohamedalrashadi&theme=radical&hide_border=true&bg_color=0D1117&color=4ECDC4&line=FF6B6B&point=00D9FF&area=true" alt="Activity Graph">
        </div>
    </section>

    <!-- Tech Stack Section -->
    <section class="tech-section">
        <h2>🛸 Futuristic Arsenal</h2>
        
        <div class="tech-grid">
            <div class="tech-card fade-in">
                <h3>🤖 Artificial Intelligence</h3>
                <ul class="tech-list">
                    <li>TensorFlow & PyTorch</li>
                    <li>Computer Vision</li>
                    <li>Natural Language Processing</li>
                    <li>Generative AI & GANs</li>
                    <li>MLOps & Deployment</li>
                </ul>
            </div>

            <div class="tech-card fade-in" style="animation-delay: 0.2s;">
                <h3>🔐 Cybersecurity</h3>
                <ul class="tech-list">
                    <li>Penetration Testing</li>
                    <li>Ethical Hacking</li>
                    <li>Cryptography</li>
                    <li>Network Security</li>
                    <li>Zero-Trust Architecture</li>
                </ul>
            </div>

            <div class="tech-card fade-in" style="animation-delay: 0.4s;">
                <h3>☁️ Cloud & DevOps</h3>
                <ul class="tech-list">
                    <li>AWS / Azure / GCP</li>
                    <li>Docker & Kubernetes</li>
                    <li>CI/CD Pipelines</li>
                    <li>Infrastructure as Code</li>
                    <li>Serverless Computing</li>
                </ul>
            </div>

            <div class="tech-card fade-in" style="animation-delay: 0.6s;">
                <h3>🌐 Full-Stack</h3>
                <ul class="tech-list">
                    <li>React & Next.js</li>
                    <li>Node.js & GraphQL</li>
                    <li>TypeScript</li>
                    <li>Real-time WebSocket</li>
                    <li>Three.js & WebGL</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects-section">
        <h2 style="text-align: center; font-size: 2.5rem; margin-bottom: 20px; background: linear-gradient(45deg, #FF6B6B, #FFD700); -webkit-background-clip: text; -webkit-text-fill-color: transparent;">
            🚀 Featured Projects
        </h2>
        
        <div class="projects-grid">
            <div class="project-card fade-in">
                <img src="https://github-readme-stats.vercel.app/api/pin/?username=mohamedalrashadi&repo=Java&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&icon_color=4ECDC4&text_color=00D9FF" alt="Java Project">
            </div>
            
            <div class="project-card fade-in" style="animation-delay: 0.2s;">
                <img src="https://github-readme-stats.vercel.app/api/pin/?username=mohamedalrashadi&repo=Python&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&icon_color=4ECDC4&text_color=00D9FF" alt="Python Project">
            </div>
            
            <div class="project-card fade-in" style="animation-delay: 0.4s;">
                <img src="https://github-readme-stats.vercel.app/api/pin/?username=mohamedalrashadi&repo=Cpp&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&icon_color=4ECDC4&text_color=00D9FF" alt="C++ Project">
            </div>
            
            <div class="project-card fade-in" style="animation-delay: 0.6s;">
                <img src="https://github-readme-stats.vercel.app/api/pin/?username=mohamedalrashadi&repo=Javascript&theme=radical&hide_border=true&bg_color=0D1117&title_color=FF6B6B&icon_color=4ECDC4&text_color=00D9FF" alt="JavaScript Project">
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section fade-in">
        <h2>🌐 Connect With Me</h2>
        <p style="font-size: 1.2rem; color: #4ECDC4; margin-bottom: 30px;">
            Let's build the future together
        </p>
        
        <div class="social-links">
            <a href="https://github.com/mohamedalrashadi" class="social-btn" target="_blank">
                GitHub
            </a>
            <a href="https://linkedin.com/in/mohamedalrashadi" class="social-btn" target="_blank">
                LinkedIn
            </a>
            <a href="mailto:your.email@example.com" class="social-btn">
                Email
            </a>
            <a href="#" class="social-btn" target="_blank">
                Portfolio
            </a>
        </div>

        <p style="margin-top: 40px; font-size: 1.1rem; color: #FFD700;">
            💼 Available for: AI Consulting | System Architecture | Tech Speaking | Mentorship
        </p>
    </section>

    <!-- Footer -->
    <footer>
        <p style="font-size: 1.5rem; margin-bottom: 20px;">
            "Code the impossible. Engineer the unthinkable. Deploy the future."
        </p>
        
        <div class="view-counter">
            <img src="https://komarev.com/ghpvc/?username=mohamedalrashadi&label=Profile%20Views&color=FF6B6B&style=for-the-badge" alt="Profile Views">
        </div>
        
        <p style="margin-top: 30px; color: #4ECDC4;">
            ⭐ Star my repos if you find them useful!
        </p>
        
        <p style="margin-top: 20px; opacity: 0.7;">
            © 2025 Mohammed Al Rashadi | Engineered with 💙
        </p>
    </footer>

    <script>
        // Generate animated stars
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.animationDelay = Math.random() * 3 + 's';
            starsContainer.appendChild(star);
        }

        // Intersection Observer for fade-in animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.fade-in').forEach((el) => {
            observer.observe(el);
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
