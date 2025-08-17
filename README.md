<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alfred Gabriel - Full-Stack & Blockchain Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #e5e7eb;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .profile-header {
            text-align: center;
            margin-bottom: 4rem;
            position: relative;
        }

        .profile-header::before {
            content: '';
            position: absolute;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 200px;
            background: radial-gradient(circle, rgba(147, 51, 234, 0.3) 0%, transparent 70%);
            border-radius: 50%;
            z-index: -1;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #9333ea, #3b82f6, #06b6d4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(147, 51, 234, 0.5)); }
            to { filter: drop-shadow(0 0 30px rgba(59, 130, 246, 0.8)); }
        }

        .tagline {
            font-size: 1.4rem;
            color: #94a3b8;
            margin-bottom: 2rem;
            font-weight: 300;
        }

        .role-badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .badge {
            background: linear-gradient(135deg, rgba(147, 51, 234, 0.2), rgba(59, 130, 246, 0.2));
            border: 1px solid rgba(147, 51, 234, 0.3);
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(147, 51, 234, 0.3);
            border-color: rgba(147, 51, 234, 0.6);
        }

        .about-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .section-icon {
            width: 32px;
            height: 32px;
            background: linear-gradient(135deg, #9333ea, #3b82f6);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .about-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .about-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(147, 51, 234, 0.2);
            border-color: rgba(147, 51, 234, 0.3);
        }

        .about-item-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            display: block;
        }

        .about-item h3 {
            font-size: 1.3rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 1rem;
        }

        .about-item p {
            color: #94a3b8;
            line-height: 1.7;
        }

        .tech-stack {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .tech-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 28px rgba(59, 130, 246, 0.15);
        }

        .tech-category h3 {
            font-size: 1.2rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .tech-tag {
            background: rgba(147, 51, 234, 0.2);
            border: 1px solid rgba(147, 51, 234, 0.3);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #e5e7eb;
            transition: all 0.3s ease;
        }

        .tech-tag:hover {
            background: rgba(147, 51, 234, 0.4);
            transform: scale(1.05);
        }

        .stats-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            text-align: center;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(6, 182, 212, 0.2);
        }

        .stat-card img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            transition: all 0.3s ease;
            filter: brightness(1.1) contrast(1.05);
        }

        .stat-card:hover img {
            transform: scale(1.02);
            filter: brightness(1.2) contrast(1.1);
            box-shadow: 0 8px 25px rgba(147, 51, 234, 0.3);
        }

        .connect-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, rgba(147, 51, 234, 0.2), rgba(59, 130, 246, 0.2));
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 50%;
            font-size: 1.5rem;
            color: #e5e7eb;
            text-decoration: none;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 15px 35px rgba(147, 51, 234, 0.4);
            border-color: rgba(147, 51, 234, 0.6);
        }

        .quote {
            font-size: 1.2rem;
            font-style: italic;
            color: #94a3b8;
            margin-top: 2rem;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            border-left: 4px solid #9333ea;
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .name {
                font-size: 2.5rem;
            }
            
            .role-badges {
                flex-direction: column;
                align-items: center;
            }
            
            .social-links {
                gap: 1rem;
            }
        }

        .floating-particles {
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
            width: 4px;
            height: 4px;
            background: rgba(147, 51, 234, 0.6);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
    </style>
</head>
<body>
    <div class="floating-particles">
        <div class="particle" style="left: 10%; top: 20%; animation-delay: 0s;"></div>
        <div class="particle" style="left: 20%; top: 80%; animation-delay: 2s;"></div>
        <div class="particle" style="left: 60%; top: 30%; animation-delay: 4s;"></div>
        <div class="particle" style="left: 80%; top: 70%; animation-delay: 1s;"></div>
        <div class="particle" style="left: 90%; top: 10%; animation-delay: 3s;"></div>
    </div>

    <div class="container">
        <header class="profile-header">
            <h1 class="name">Alfred Gabriel</h1>
            <p class="tagline">Building the future with code, blockchain, and innovation</p>
            
            <div class="role-badges">
                <span class="badge">🚀 Solana Developer</span>
                <span class="badge">💻 Full-Stack Engineer</span>
                <span class="badge">🔗 Blockchain Specialist</span>
                <span class="badge">🎮 Gaming Enthusiast</span>
            </div>
        </header>

        <section class="about-section">
            <h2 class="section-title">
                <div class="section-icon">🌟</div>
                About Me
            </h2>
            
            <div class="about-grid">
                <div class="about-item">
                    <span class="about-item-icon">💻</span>
                    <h3>Full-Stack Excellence</h3>
                    <p>Crafting modern, high-performance applications with cutting-edge technologies like Next.js, Laravel, and Node.js. I focus on creating scalable solutions that deliver exceptional user experiences.</p>
                </div>
                
                <div class="about-item">
                    <span class="about-item-icon">⛓️</span>
                    <h3>Blockchain Innovation</h3>
                    <p>Specialized in Solidity, Web3.js, and Solana development. I build secure DeFi protocols, NFT marketplaces, and innovative crypto solutions that push the boundaries of decentralized technology.</p>
                </div>
                
                <div class="about-item">
                    <span class="about-item-icon">🎯</span>
                    <h3>Strategic Gaming</h3>
                    <p>Competitive FPS and strategy gaming isn't just a hobby—it's a source of creativity and strategic thinking that enhances my problem-solving abilities in development projects.</p>
                </div>
                
                <div class="about-item">
                    <span class="about-item-icon">🚀</span>
                    <h3>Builder's Mentality</h3>
                    <p>Always experimenting with emerging technologies, shipping side projects, and staying ahead of the curve. I believe in continuous learning and turning ideas into reality.</p>
                </div>
            </div>
        </section>

        <section class="tech-stack">
            <h2 class="section-title">
                <div class="section-icon">🛠️</div>
                Technical Expertise
            </h2>
            
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>🎨 Frontend</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">TypeScript</span>
                        <span class="tech-tag">Tailwind CSS</span>
                        <span class="tech-tag">Vue.js</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>⚙️ Backend</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">Laravel</span>
                        <span class="tech-tag">Express.js</span>
                        <span class="tech-tag">PHP</span>
                        <span class="tech-tag">Python</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>🔗 Blockchain</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Solidity</span>
                        <span class="tech-tag">Web3.js</span>
                        <span class="tech-tag">Solana</span>
                        <span class="tech-tag">Rust</span>
                        <span class="tech-tag">Ethereum</span>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3>🔧 DevOps & Tools</h3>
                    <div class="tech-tags">
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">GitHub Actions</span>
                        <span class="tech-tag">Vercel</span>
                        <span class="tech-tag">AWS</span>
                        <span class="tech-tag">Git</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="stats-section">
            <h2 class="section-title">
                <div class="section-icon">📊</div>
                GitHub Analytics
            </h2>
            
            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=XaidenLabs&show_icons=true&theme=radical&hide_border=true&bg_color=0d1117&title_color=9333ea&icon_color=3b82f6&text_color=e5e7eb" alt="Alfred's GitHub stats" style="width: 100%; height: auto; border-radius: 10px;" />
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 1rem;">Activity and contribution metrics</p>
                </div>
                
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=XaidenLabs&theme=radical&hide_border=true&background=0d1117&stroke=9333ea&ring=3b82f6&fire=06b6d4&currStreakLabel=e5e7eb" alt="Alfred's GitHub streak" style="width: 100%; height: auto; border-radius: 10px;" />
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 1rem;">Consistency in daily development</p>
                </div>
                
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=XaidenLabs&layout=compact&theme=radical&hide_border=true&bg_color=0d1117&title_color=9333ea&text_color=e5e7eb" alt="Top languages" style="width: 100%; height: auto; border-radius: 10px;" />
                    <p style="color: #94a3b8; font-size: 0.9rem; margin-top: 1rem;">Most used programming languages</p>
                </div>
            </div>
        </section>

        <section class="connect-section">
            <h2 class="section-title">
                <div class="section-icon">🌐</div>
                Let's Connect
            </h2>
            
            <p style="color: #94a3b8; font-size: 1.1rem; margin-bottom: 1rem;">
                Ready to collaborate on your next project? Let's build something amazing together.
            </p>
            
            <div class="social-links">
                <a href="https://twitter.com/xaidenlabs" target="_blank" class="social-link" title="Twitter">
                    🐦
                </a>
                <a href="https://linkedin.com/in/alfred-gabriel-5529a926a" target="_blank" class="social-link" title="LinkedIn">
                    💼
                </a>
                <a href="https://xaidenlabs.com.ng" target="_blank" class="social-link" title="Portfolio">
                    🌐
                </a>
                <a href="https://github.com/XaidenLabs" target="_blank" class="social-link" title="GitHub">
                    🐱
                </a>
            </div>
            
            <div class="quote">
                "Code is my craft, blockchain is my battlefield, and gaming is my grind."
            </div>
        </section>
    </div>

    <script>
        // Add subtle animations and interactions
        document.addEventListener('DOMContentLoaded', function() {
            // Smooth scrolling for any internal links
            const links = document.querySelectorAll('a[href^="#"]');
            links.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({ behavior: 'smooth' });
                    }
                });
            });

            // Add intersection observer for animations
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.1 });

            // Observe all major sections
            document.querySelectorAll('.about-section, .tech-stack, .stats-section, .connect-section').forEach(section => {
                section.style.opacity = '0';
                section.style.transform = 'translateY(30px)';
                section.style.transition = 'all 0.6s ease';
                observer.observe(section);
            });

            // Add dynamic particles
            function createParticle() {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                document.querySelector('.floating-particles').appendChild(particle);
                
                setTimeout(() => {
                    particle.remove();
                }, 6000);
            }

            // Create particles periodically
            setInterval(createParticle, 3000);
        });
    </script>
</body>
</html>
