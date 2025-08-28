<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdur Rahman Faisal - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0a0a1a 0%, #0d1b2a 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .glass-card {
            background: rgba(13, 27, 42, 0.7);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.18);
            box-shadow: 0 8px 32px 0 rgba(0, 4, 31, 0.37);
            padding: 30px;
            margin-bottom: 25px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .glass-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 40px 0 rgba(0, 12, 80, 0.5);
        }
        
        .header {
            text-align: center;
            padding: 30px 0;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid rgba(66, 153, 225, 0.5);
            margin: 0 auto 20px;
            box-shadow: 0 0 25px rgba(66, 153, 225, 0.5);
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #4299e1, #38b2ac);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(66, 153, 225, 0.3);
        }
        
        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #90cdf4;
        }
        
        h3 {
            font-size: 1.5rem;
            margin: 25px 0 15px;
            color: #63b3ed;
            border-left: 4px solid #4299e1;
            padding-left: 10px;
        }
        
        p {
            line-height: 1.6;
            margin-bottom: 15px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(41, 98, 255, 0.1);
            color: #90cdf4;
            text-decoration: none;
            padding: 12px 20px;
            border-radius: 50px;
            transition: all 0.3s ease;
            border: 1px solid rgba(66, 153, 225, 0.3);
        }
        
        .social-btn:hover {
            background: rgba(66, 153, 225, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(66, 153, 225, 0.2);
        }
        
        .social-btn i {
            margin-right: 8px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }
        
        .badge {
            background: rgba(66, 153, 225, 0.15);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(66, 153, 225, 0.3);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .skill-category {
            background: rgba(26, 54, 80, 0.4);
            padding: 20px;
            border-radius: 15px;
            border: 1px solid rgba(66, 153, 225, 0.2);
        }
        
        .project {
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(66, 153, 225, 0.2);
        }
        
        .project:last-child {
            border-bottom: none;
        }
        
        .project-title {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        .quote {
            text-align: center;
            font-style: italic;
            padding: 20px;
            margin: 30px 0;
            border-radius: 15px;
            background: rgba(26, 54, 80, 0.4);
            border-left: 4px solid rgba(66, 153, 225, 0.5);
        }
        
        .stats {
            display: flex;
            justify-content: space-around;
            text-align: center;
            margin: 30px 0;
        }
        
        .stat-item {
            padding: 15px;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            background: linear-gradient(90deg, #4299e1, #38b2ac);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        @media (max-width: 768px) {
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .stats {
                flex-direction: column;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
            
            .social-btn {
                width: 100%;
                max-width: 300px;
            }
        }
        
        .accent-blue {
            color: #63b3ed;
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(66, 153, 225, 0); }
            100% { box-shadow: 0 0 0 0 rgba(66, 153, 225, 0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="glass-card header">
            <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80" alt="Profile Photo" class="profile-img">
            <h1>Abdur Rahman Faisal</h1>
            <h2>Aspiring Software & Data Engineer | CSE Undergrad @ Southeast University</h2>
            
            <div class="social-links">
                <a href="mailto:arfaisal463@gmail.com" class="social-btn">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://www.linkedin.com/in/abdur-rahman-faisal" class="social-btn">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="https://arfaisal043.github.io/faisal.com" class="social-btn">
                    <i class="fas fa-globe"></i> Portfolio
                </a>
                <a href="https://leetcode.com/u/AR_Faisal/" class="social-btn">
                    <i class="fas fa-code"></i> LeetCode
                </a>
            </div>
        </div>
        
        <!-- Technical Skills -->
        <div class="glass-card">
            <h3>🛠️ Technical Toolkit</h3>
            
            <h3>Programming Languages</h3>
            <div class="badges">
                <span class="badge">Python</span>
                <span class="badge">Java</span>
                <span class="badge">C</span>
                <span class="badge">C++</span>
                <span class="badge">JavaScript</span>
                <span class="badge">SQL</span>
            </div>
            
            <h3>Frameworks & Tools</h3>
            <div class="badges">
                <span class="badge">Git</span>
                <span class="badge">Pandas</span>
                <span class="badge">NumPy</span>
                <span class="badge">MongoDB</span>
                <span class="badge">Power BI</span>
                <span class="badge">Matplotlib</span>
            </div>
        </div>
        
        <!-- Core Skills -->
        <div class="glass-card">
            <h3>📊 Core Competencies</h3>
            
            <div class="skills-grid">
                <div class="skill-category">
                    <h4>☕ Programming Languages</h4>
                    <p>Java, Python, C, C++, JavaScript</p>
                </div>
                
                <div class="skill-category">
                    <h4>🧠 Data Structures & Algorithms</h4>
                    <p>LeetCode 50+ problems (Easy-Medium-Hard)</p>
                </div>
                
                <div class="skill-category">
                    <h4>📊 Data Analytics</h4>
                    <p>Python, SQL, Statistics, Pandas, NumPy, Matplotlib, Power BI, Excel</p>
                </div>
                
                <div class="skill-category">
                    <h4>🗃️ Database Systems</h4>
                    <p>MongoDB, SQL, ETL Pipelines</p>
                </div>
                
                <div class="skill-category">
                    <h4>⚙️ System Design</h4>
                    <p>Microservices, REST APIs</p>
                </div>
                
                <div class="skill-category">
                    <h4>🖥️ Engineering Math</h4>
                    <p>Calculus, Linear Algebra, Statistics</p>
                </div>
            </div>
        </div>
        
        <!-- Projects -->
        <div class="glass-card">
            <h3>🚀 Featured Projects</h3>
            
            <div class="project">
                <div class="project-title">
                    <i class="fas fa-folder accent-blue"></i>
                    <h4>Python File Manager</h4>
                </div>
                <p>A terminal-based file management system with CRUD operations, error-resistant design, and modern pathlib implementation.</p>
                <div class="badges">
                    <span class="badge">Python</span>
                    <span class="badge">CRUD Operations</span>
                    <span class="badge">File Management</span>
                </div>
            </div>
            
            <div class="project">
                <div class="project-title">
                    <i class="fas fa-chart-bar accent-blue"></i>
                    <h4>Data Analysis Projects</h4>
                </div>
                <p>Multiple data analysis projects using Python, Pandas, and NumPy with interactive Power BI dashboards and ETL pipelines.</p>
                <div class="badges">
                    <span class="badge">Python</span>
                    <span class="badge">Pandas</span>
                    <span class="badge">Power BI</span>
                    <span class="badge">ETL</span>
                </div>
            </div>
        </div>
        
        <!-- Stats & Goals -->
        <div class="glass-card">
            <h3>📈 Coding Activity & Goals</h3>
            
            <div class="stats">
                <div class="stat-item">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">LeetCode Problems</div>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number">40+</div>
                    <div class="stat-label">Days Streak</div>
                </div>
                
                <div class="stat-item">
                    <div class="stat-number">5</div>
                    <div class="stat-label">Projects</div>
                </div>
            </div>
            
            <p>🌱 <span class="accent-blue">Currently Learning:</span> Advanced Python & SQL for Data Science</p>
            <p>💻 <span class="accent-blue">Daily Coding Streak on LeetCode:</span> 40+ days and counting</p>
            
            <h3>🎯 Goals for 2024</h3>
            <ul>
                <li>Master Data Engineering concepts and tools</li>
                <li>Contribute to open-source projects</li>
                <li>Build a comprehensive data pipeline project</li>
                <li>Solve 200+ LeetCode problems</li>
            </ul>
        </div>
        
        <!-- Quote -->
        <div class="quote">
            <p>"Turning coffee into code, one bug at a time." ☕💻</p>
        </div>
    </div>

    <script>
        // Simple animation for badges
        document.querySelectorAll('.badge').forEach(badge => {
            badge.addEventListener('mouseover', () => {
                badge.style.transform = 'scale(1.1)';
                badge.style.transition = 'transform 0.2s ease';
            });
            
            badge.addEventListener('mouseout', () => {
                badge.style.transform = 'scale(1)';
            });
        });
    </script>
</body>
</html>
