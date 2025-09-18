<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NIYIBIZI Maximilien - Software Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #e2e8f0;
            line-height: 1.6;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }
        
        @media (max-width: 900px) {
            .container {
                grid-template-columns: 1fr;
            }
        }
        
        header {
            grid-column: 1 / -1;
            text-align: center;
            margin-bottom: 2rem;
            padding: 2rem;
            background: rgba(30, 41, 59, 0.5);
            border-radius: 16px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(90deg, #4c6ef5 0%, #3bc9db 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
        }
        
        h2 {
            font-size: 1.8rem;
            margin: 1.5rem 0 1rem;
            color: #4c6ef5;
            border-bottom: 2px solid #334155;
            padding-bottom: 0.5rem;
        }
        
        h3 {
            font-size: 1.4rem;
            margin: 1.2rem 0 0.8rem;
            color: #3bc9db;
        }
        
        .tagline {
            font-size: 1.4rem;
            color: #94a3b8;
            margin-bottom: 1rem;
        }
        
        .card {
            background: rgba(30, 41, 59, 0.5);
            border-radius: 16px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .section-title {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            margin-bottom: 1rem;
        }
        
        .section-title i {
            font-size: 1.5rem;
            color: #4c6ef5;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .tech-item {
            background: rgba(15, 23, 42, 0.7);
            padding: 0.8rem;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .tech-item:hover {
            background: rgba(51, 65, 85, 0.7);
            transform: scale(1.05);
        }
        
        .project {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #334155;
        }
        
        .project:last-child {
            border-bottom: none;
        }
        
        .project-title {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.8rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 0.8rem 0;
        }
        
        .tech-badge {
            background: rgba(76, 110, 245, 0.2);
            color: #4c6ef5;
            padding: 0.3rem 0.6rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        
        .stats-container {
            display: flex;
            justify-content: space-around;
            text-align: center;
            margin: 1.5rem 0;
        }
        
        .stat {
            padding: 1rem;
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: #3bc9db;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: #94a3b8;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #e2e8f0;
            text-decoration: none;
            padding: 0.8rem 1.2rem;
            background: rgba(76, 110, 245, 0.2);
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .contact-link:hover {
            background: rgba(76, 110, 245, 0.4);
            transform: translateY(-2px);
        }
        
        .language-bar {
            background: rgba(15, 23, 42, 0.7);
            height: 24px;
            border-radius: 12px;
            margin: 0.8rem 0;
            overflow: hidden;
            position: relative;
        }
        
        .language-fill {
            height: 100%;
            border-radius: 12px;
            display: flex;
            align-items: center;
            padding: 0 1rem;
            color: #0f172a;
            font-weight: 600;
            font-size: 0.9rem;
            white-space: nowrap;
        }
        
        .python { width: 25%; background: linear-gradient(90deg, #3776ab 0%, #5a9fd4 100%); }
        .typescript { width: 15%; background: linear-gradient(90deg, #3178c6 0%, #5a9fd4 100%); }
        .java { width: 12.5%; background: linear-gradient(90deg, #007396 0%, #4c9feb 100%); }
        .javascript { width: 8.75%; background: linear-gradient(90deg, #f7df1e 0%, #ffeb6e 100%); color: #000; }
        .cpp { width: 6.25%; background: linear-gradient(90deg, #00599c 0%, #4c9feb 100%); }
        .html { width: 3.75%; background: linear-gradient(90deg, #e34f26 0%, #ff7b54 100%); }
        
        footer {
            grid-column: 1 / -1;
            text-align: center;
            margin-top: 2rem;
            padding: 1.5rem;
            color: #94a3b8;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>NIYIBIZI Maximilien</h1>
        <p class="tagline">Software Engineer | Industrial Designer | ML Enthusiast</p>
        <p>Backend Developer & DevOps Engineer with passion for creating efficient, scalable systems</p>
    </header>

    <div class="container">
        <div class="left-column">
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-code"></i>
                    <h2>Technical Skills</h2>
                </div>
                
                <h3>Programming Languages</h3>
                <div class="tech-grid">
                    <div class="tech-item">C++</div>
                    <div class="tech-item">Python</div>
                    <div class="tech-item">JavaScript</div>
                    <div class="tech-item">TypeScript</div>
                    <div class="tech-item">Rust</div>
                    <div class="tech-item">Go</div>
                    <div class="tech-item">Java</div>
                </div>
                
                <h3>Frameworks & Libraries</h3>
                <div class="tech-grid">
                    <div class="tech-item">React</div>
                    <div class="tech-item">Node.js</div>
                    <div class="tech-item">Express.js</div>
                    <div class="tech-item">NestJS</div>
                    <div class="tech-item">Vue.js</div>
                    <div class="tech-item">TensorFlow</div>
                </div>
                
                <h3>Databases</h3>
                <div class="tech-grid">
                    <div class="tech-item">MongoDB</div>
                    <div class="tech-item">MySQL</div>
                    <div class="tech-item">PostgreSQL</div>
                    <div class="tech-item">Redis</div>
                </div>
                
                <h3>DevOps & Cloud</h3>
                <div class="tech-grid">
                    <div class="tech-item">Docker</div>
                    <div class="tech-item">Kubernetes</div>
                    <div class="tech-item">AWS</div>
                    <div class="tech-item">Git</div>
                    <div class="tech-item">Jenkins</div>
                </div>
            </div>
            
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-graduation-cap"></i>
                    <h2>Currently Learning</h2>
                </div>
                <div class="tech-grid">
                    <div class="tech-item">AWS Advanced</div>
                    <div class="tech-item">GraphQL</div>
                    <div class="tech-item">Flutter</div>
                    <div class="tech-item">Kubernetes</div>
                    <div class="tech-item">React Native</div>
                </div>
            </div>
            
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-chart-bar"></i>
                    <h2>Language Proficiency</h2>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill python">Python 25%</div>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill typescript">TypeScript 15%</div>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill java">Java 12.5%</div>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill javascript">JavaScript 8.75%</div>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill cpp">C++ 6.25%</div>
                </div>
                
                <div class="language-bar">
                    <div class="language-fill html">HTML/CSS 3.75%</div>
                </div>
            </div>
        </div>
        
        <div class="right-column">
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-rocket"></i>
                    <h2>Current Project</h2>
                </div>
                
                <div class="project">
                    <div class="project-title">
                        <h3>Cadastre Land Management System</h3>
                    </div>
                    <p>A comprehensive land management system for cadastral mapping, property registration, and digital land records management with geospatial capabilities.</p>
                    
                    <div class="project-tech">
                        <span class="tech-badge">NestJS</span>
                        <span class="tech-badge">Vue.js</span>
                        <span class="tech-badge">TypeScript</span>
                        <span class="tech-badge">PostgreSQL</span>
                        <span class="tech-badge">PostGIS</span>
                        <span class="tech-badge">Docker</span>
                    </div>
                </div>
            </div>
            
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-medal"></i>
                    <h2>GitHub Statistics</h2>
                </div>
                
                <div class="stats-container">
                    <div class="stat">
                        <div class="stat-number">127</div>
                        <div class="stat-label">Contributions</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">19</div>
                        <div class="stat-label">Repositories</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">14</div>
                        <div class="stat-label">Projects</div>
                    </div>
                </div>
                
                <div class="project">
                    <div class="project-title">
                        <h3>Commit Activity</h3>
                    </div>
                    <p>Consistent contributor with focus on backend development, DevOps automation, and machine learning projects.</p>
                </div>
            </div>
            
            <div class="card">
                <div class="section-title">
                    <i class="fas fa-envelope"></i>
                    <h2>Contact</h2>
                </div>
                
                <div class="contact-links">
                    <a href="https://x.com/wamukapo" class="contact-link">
                        <i class="fab fa-twitter"></i>
                        Twitter
                    </a>
                    <a href="mailto:niyibizimaximilien" class="contact-link">
                        <i class="fas fa-envelope"></i>
                        Email
                    </a>
                    <a href="https://discord.gg/maximmilien_69102" class="contact-link">
                        <i class="fab fa-discord"></i>
                        Discord
                    </a>
                </div>
                
                <div class="contact-links">
                    <a href="https://linkedin.com/in/maximilien-niyibizi" class="contact-link">
                        <i class="fab fa-linkedin"></i>
                        LinkedIn
                    </a>
                    <a href="https://github.com/niyibizimaximilien" class="contact-link">
                        <i class="fab fa-github"></i>
                        GitHub
                    </a>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>Built with ❤️ by NIYIBIZI Maximilien | © 2023</p>
    </footer>
</body>
</html>
