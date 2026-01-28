<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prasad Shinde - QA Automation Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f1425 100%);
            color: #e0e0e0;
            overflow-x: hidden;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: rgba(0, 255, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Header Section */
        header {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.1) 0%, rgba(255, 0, 255, 0.1) 100%);
            border-radius: 20px;
            margin-bottom: 40px;
            border: 1px solid rgba(0, 255, 255, 0.2);
            box-shadow: 0 0 30px rgba(0, 255, 255, 0.1);
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .profile-image {
            width: 200px;
            height: 200px;
            margin: 0 auto 30px;
            position: relative;
        }

        .profile-image::before {
            content: '';
            position: absolute;
            width: 220px;
            height: 220px;
            top: -10px;
            left: -10px;
            border: 3px solid transparent;
            border-image: linear-gradient(45deg, #00ffff, #ff00ff, #00ffff);
            border-image-slice: 1;
            border-radius: 50%;
            animation: rotate 4s linear infinite;
        }

        @keyframes rotate {
            100% {
                transform: rotate(360deg);
            }
        }

        .avatar {
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, #1a1f3a, #0a0e27);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            border: 5px solid #00ffff;
            box-shadow: 0 0 40px rgba(0, 255, 255, 0.5);
        }

        h1 {
            font-size: 3.5em;
            background: linear-gradient(45deg, #00ffff, #ff00ff, #00ffff);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 3s ease infinite;
            margin-bottom: 15px;
        }

        @keyframes gradientShift {
            0%, 100% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
        }

        .title {
            font-size: 1.5em;
            color: #00ffff;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
        }

        .company {
            font-size: 1.2em;
            color: #ff00ff;
            margin-bottom: 20px;
        }

        .tagline {
            font-size: 1.1em;
            color: #b0b0b0;
            font-style: italic;
            max-width: 800px;
            margin: 0 auto;
        }

        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.05), rgba(255, 0, 255, 0.05));
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(0, 255, 255, 0.3);
            text-align: center;
            transition: all 0.3s ease;
            animation: fadeIn 0.8s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: scale(0.9);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 10px 40px rgba(0, 255, 255, 0.3);
            border-color: #00ffff;
        }

        .stat-number {
            font-size: 3em;
            font-weight: bold;
            background: linear-gradient(45deg, #00ffff, #ff00ff);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1.1em;
            color: #a0a0a0;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Skills Section */
        .section {
            background: linear-gradient(135deg, rgba(26, 31, 58, 0.6), rgba(10, 14, 39, 0.6));
            padding: 40px;
            border-radius: 20px;
            margin-bottom: 30px;
            border: 1px solid rgba(0, 255, 255, 0.2);
            backdrop-filter: blur(10px);
        }

        .section-title {
            font-size: 2.2em;
            margin-bottom: 30px;
            color: #00ffff;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title::before {
            content: '';
            width: 50px;
            height: 4px;
            background: linear-gradient(90deg, #00ffff, #ff00ff);
            border-radius: 2px;
        }

        /* Current Focus */
        .focus-grid {
            display: grid;
            gap: 15px;
        }

        .focus-item {
            background: linear-gradient(90deg, rgba(0, 255, 255, 0.1), rgba(255, 0, 255, 0.05));
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #00ffff;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: all 0.3s ease;
        }

        .focus-item:hover {
            transform: translateX(10px);
            background: linear-gradient(90deg, rgba(0, 255, 255, 0.2), rgba(255, 0, 255, 0.1));
            box-shadow: 0 5px 20px rgba(0, 255, 255, 0.2);
        }

        .check-icon {
            font-size: 1.5em;
            color: #00ff00;
            text-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .tech-item {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.08), rgba(255, 0, 255, 0.08));
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(0, 255, 255, 0.2);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-8px) rotate(2deg);
            border-color: #00ffff;
            box-shadow: 0 10px 30px rgba(0, 255, 255, 0.3);
        }

        .tech-icon {
            font-size: 3em;
            margin-bottom: 10px;
        }

        .tech-name {
            font-weight: bold;
            color: #00ffff;
            margin-bottom: 5px;
        }

        .tech-level {
            font-size: 0.9em;
            color: #808080;
        }

        /* Skills bars */
        .skills-list {
            display: grid;
            gap: 20px;
        }

        .skill {
            background: rgba(0, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            border: 1px solid rgba(0, 255, 255, 0.15);
        }

        .skill-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .skill-name {
            font-weight: bold;
            color: #00ffff;
            font-size: 1.1em;
        }

        .skill-level {
            color: #ff00ff;
            font-weight: bold;
        }

        .skill-bar {
            width: 100%;
            height: 10px;
            background: rgba(0, 255, 255, 0.1);
            border-radius: 5px;
            overflow: hidden;
            position: relative;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, #00ffff, #ff00ff);
            border-radius: 5px;
            transition: width 1.5s ease;
            box-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .contact-item {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.1), rgba(255, 0, 255, 0.1));
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(0, 255, 255, 0.3);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .contact-item:hover {
            transform: scale(1.08);
            box-shadow: 0 10px 30px rgba(0, 255, 255, 0.4);
        }

        .contact-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }

        .contact-label {
            font-weight: bold;
            color: #00ffff;
            margin-bottom: 8px;
        }

        .contact-value {
            color: #b0b0b0;
            font-size: 0.95em;
        }

        /* GitHub Activity */
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .github-stat {
            background: linear-gradient(135deg, rgba(0, 255, 255, 0.08), rgba(255, 0, 255, 0.08));
            padding: 25px;
            border-radius: 12px;
            border: 1px solid rgba(0, 255, 255, 0.2);
            text-align: center;
        }

        .github-stat-value {
            font-size: 2.5em;
            font-weight: bold;
            color: #00ffff;
            text-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
        }

        .github-stat-label {
            color: #a0a0a0;
            margin-top: 10px;
            font-size: 0.95em;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .section-title {
                font-size: 1.8em;
            }

            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            }
        }

        /* Glowing effect */
        .glow {
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% {
                filter: brightness(1);
            }
            50% {
                filter: brightness(1.3);
            }
        }

        /* Code effect */
        .code-rain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            opacity: 0.1;
            z-index: 0;
        }
    </style>
</head>
<body>
    <!-- Animated particles -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <!-- Header Section -->
        <header>
            <div class="profile-image">
                <div class="avatar">👨‍💻</div>
            </div>
            <h1>Hi 👋, I'm Prasad Shinde</h1>
            <div class="title">🚀 QA Automation Engineer</div>
            <div class="company">Reactore Private Limited</div>
            <div class="tagline">🔧 Let's build, break and test smarter. Quality is never an accident! 💡</div>
        </header>

        <!-- Stats Section -->
        <div class="stats-grid">
            <div class="stat-card">
                <div class="stat-number">234</div>
                <div class="stat-label">Profile Views</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">20</div>
                <div class="stat-label">Total Contributions</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">90.87%</div>
                <div class="stat-label">Java Expertise</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">2825</div>
                <div class="stat-label">Commits</div>
            </div>
        </div>

        <!-- Current Focus -->
        <section class="section">
            <h2 class="section-title">📚 Current Focus</h2>
            <div class="focus-grid">
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>Playwright with Java (Automation Framework)</strong>
                        <div style="color: #808080; font-size: 0.9em;">Building robust test automation frameworks</div>
                    </div>
                </div>
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>BDD (Cucumber), Page Object Model</strong>
                        <div style="color: #808080; font-size: 0.9em;">Implementing behavior-driven development practices</div>
                    </div>
                </div>
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>Excel Data-Driven Testing</strong>
                        <div style="color: #808080; font-size: 0.9em;">Advanced data management for test automation</div>
                    </div>
                </div>
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>Test Case Documentation & UI Testing Reports</strong>
                        <div style="color: #808080; font-size: 0.9em;">Comprehensive quality assurance documentation</div>
                    </div>
                </div>
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>Manual Testing, Selenium, and Playwright (Java)</strong>
                        <div style="color: #808080; font-size: 0.9em;">Multi-tool testing expertise</div>
                    </div>
                </div>
                <div class="focus-item">
                    <span class="check-icon">✅</span>
                    <div>
                        <strong>Linux Certification & Web Technologies</strong>
                        <div style="color: #808080; font-size: 0.9em;">Expanding technical knowledge base</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Core QA Skills -->
        <section class="section">
            <h2 class="section-title">🎯 Core QA & Automation Skills</h2>
            <div class="skills-list">
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Manual Testing & Test Case Design</span>
                        <span class="skill-level">Expert</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 95%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Selenium WebDriver (Java)</span>
                        <span class="skill-level">Advanced</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 90%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Playwright Automation Framework</span>
                        <span class="skill-level">Advanced</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 88%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">BDD with Cucumber</span>
                        <span class="skill-level">Advanced</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 85%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Page Object Model (POM)</span>
                        <span class="skill-level">Expert</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 92%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Test Reporting & Documentation</span>
                        <span class="skill-level">Expert</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 93%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">Data-Driven Testing (Excel)</span>
                        <span class="skill-level">Advanced</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 87%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">API Testing & Automation</span>
                        <span class="skill-level">Intermediate</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 75%"></div>
                    </div>
                </div>
                <div class="skill">
                    <div class="skill-header">
                        <span class="skill-name">CI/CD Integration</span>
                        <span class="skill-level">Intermediate</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-progress" style="width: 70%"></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Tech Stack -->
        <section class="section">
            <h2 class="section-title">🛠️ Technology Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">☕</div>
                    <div class="tech-name">Java</div>
                    <div class="tech-level">Core Language</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🎭</div>
                    <div class="tech-name">Playwright</div>
                    <div class="tech-level">Automation</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🌐</div>
                    <div class="tech-name">Selenium</div>
                    <div class="tech-level">WebDriver</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🥒</div>
                    <div class="tech-name">Cucumber</div>
                    <div class="tech-level">BDD Framework</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🧪</div>
                    <div class="tech-name">TestNG</div>
                    <div class="tech-level">Testing Framework</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📊</div>
                    <div class="tech-name">Excel</div>
                    <div class="tech-level">Data-Driven</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🔨</div>
                    <div class="tech-name">Maven</div>
                    <div class="tech-level">Build Tool</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">📝</div>
                    <div class="tech-name">Jira</div>
                    <div class="tech-level">Project Mgmt</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐙</div>
                    <div class="tech-name">Git</div>
                    <div class="tech-level">Version Control</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🗄️</div>
                    <div class="tech-name">SQL</div>
                    <div class="tech-level">Database</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐧</div>
                    <div class="tech-name">Linux</div>
                    <div class="tech-level">OS Platform</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🌍</div>
                    <div class="tech-name">HTML/CSS</div>
                    <div class="tech-level">Web Tech</div>
                </div>
            </div>
        </section>

        <!-- GitHub Stats -->
        <section class="section">
            <h2 class="section-title">📊 GitHub Activity</h2>
            <div class="github-stats">
                <div class="github-stat">
                    <div class="github-stat-value">Java</div>
                    <div class="github-stat-label">Primary Language<br>90.87%</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-value">2825</div>
                    <div class="github-stat-label">Total Commits</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-value">20</div>
                    <div class="github-stat-label">Contributions</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-value">2</div>
                    <div class="github-stat-label">Longest Streak<br>(Days)</div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="section">
            <h2 class="section-title">📧 Connect With Me</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <div class="contact-label">Email</div>
                    <div class="contact-value">prasadshinde9066@gmail.com</div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">💼</div>
                    <div class="contact-label">LinkedIn</div>
                    <div class="contact-value">Connect on LinkedIn</div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">📸</div>
                    <div class="contact-label">Instagram</div>
                    <div class="contact-value">Follow on Instagram</div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">🏢</div>
                    <div class="contact-label">Company</div>
                    <div class="contact-value">Reactore Private Limited</div>
                </div>
            </div>
        </section>
    </div>

    <script>
        // Create floating particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 15 + 's';
            particle.style.animationDuration = (10 + Math.random() * 10) + 's';
            particlesContainer.appendChild(particle);
        }

        // Animate skill bars on scroll
        const observerOptions = {
            threshold: 0.5
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const progressBars = entry.target.querySelectorAll('.skill-progress');
                    progressBars.forEach(bar => {
                        const width = bar.style.width;
                        bar.style.width = '0%';
                        setTimeout(() => {
                            bar.style.width = width;
                        }, 100);
                    });
                }
            });
        }, observerOptions);

        document.querySelectorAll('.skills-list').forEach(section => {
            observer.observe(section);
        });

        // Add hover effects to tech items
        document.querySelectorAll('.tech-item').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.background = 'linear-gradient(135deg, rgba(0, 255, 255, 0.15), rgba(255, 0, 255, 0.15))';
            });
            item.addEventListener('mouseleave', function() {
                this.style.background = 'linear-gradient(135deg, rgba(0, 255, 255, 0.08), rgba(255, 0, 255, 0.08))';
            });
        });

        // Animate stats on load
        window.addEventListener('load', () => {
            document.querySelectorAll('.stat-card').forEach((card, index) => {
                card.style.animationDelay = `${index * 0.1}s`;
            });
        });
    </script>
</body>
</html>
