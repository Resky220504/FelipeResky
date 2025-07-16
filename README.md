<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Felipe Resky | Desenvolvedor</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0f172a;
            --secondary: #0ea5e9;
            --accent: #8b5cf6;
            --terminal: #10b981;
            --dark: #1e293b;
            --light: #f1f5f9;
            --card-bg: rgba(30, 41, 59, 0.7);
            --glow: 0 0 15px rgba(14, 165, 233, 0.5);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'SF Pro Display', 'Segoe UI', sans-serif;
        }
        
        body {
            background: radial-gradient(circle at center, #0f172a, #020617);
            color: var(--light);
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header futurista */
        header {
            text-align: center;
            padding: 60px 20px;
            margin-bottom: 40px;
            background: var(--card-bg);
            border-radius: 20px;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            box-shadow: var(--glow);
            border: 1px solid rgba(14, 165, 233, 0.2);
        }
        
        .tech-grid-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                linear-gradient(90deg, transparent 50%, rgba(14, 165, 233, 0.05) 50%),
                linear-gradient(transparent 50%, rgba(14, 165, 233, 0.05) 50%);
            background-size: 30px 30px;
            opacity: 0.3;
            z-index: -1;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 25px;
            background: linear-gradient(135deg, var(--secondary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            box-shadow: 0 0 30px rgba(14, 165, 233, 0.7);
            border: 3px solid rgba(255, 255, 255, 0.1);
        }
        
        h1 {
            font-size: 3.2rem;
            margin-bottom: 15px;
            background: linear-gradient(to right, var(--light), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(14, 165, 233, 0.3);
        }
        
        .tagline {
            font-size: 1.4rem;
            font-weight: 300;
            max-width: 700px;
            margin: 0 auto 25px;
            color: var(--light);
        }
        
        .terminal {
            background: rgba(15, 23, 42, 0.9);
            border-radius: 15px;
            padding: 25px;
            margin: 40px auto;
            max-width: 800px;
            font-family: 'Fira Code', monospace;
            border: 1px solid rgba(14, 165, 233, 0.3);
            box-shadow: inset 0 0 20px rgba(0, 0, 0, 0.5);
        }
        
        .terminal-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(14, 165, 233, 0.2);
        }
        
        .terminal-dots {
            display: flex;
            gap: 8px;
            margin-right: 15px;
        }
        
        .dot {
            width: 15px;
            height: 15px;
            border-radius: 50%;
        }
        
        .dot-red { background: #ef4444; }
        .dot-yellow { background: #f59e0b; }
        .dot-green { background: var(--terminal); }
        
        .terminal-title {
            color: var(--secondary);
            font-size: 1.1rem;
        }
        
        .terminal-content {
            line-height: 1.8;
        }
        
        .terminal-prompt {
            color: var(--terminal);
        }
        
        .terminal-command {
            color: var(--secondary);
        }
        
        .terminal-output {
            color: var(--light);
            margin: 15px 0;
            padding-left: 20px;
            border-left: 2px solid rgba(14, 165, 233, 0.3);
        }
        
        .section {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 40px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(14, 165, 233, 0.2);
            box-shadow: var(--glow);
            position: relative;
            overflow: hidden;
        }
        
        .section-title {
            font-size: 2.2rem;
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 3px solid var(--secondary);
            display: flex;
            align-items: center;
            gap: 15px;
            color: var(--light);
        }
        
        .section-title i {
            color: var(--secondary);
            font-size: 1.8rem;
        }
        
        /* Grid de tecnologias */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 30px;
            text-align: center;
        }
        
        .tech-card {
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            padding: 30px 20px;
            transition: all 0.4s ease;
            border: 1px solid rgba(14, 165, 233, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .tech-card::before {
            content: "";
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--secondary), var(--accent), var(--terminal));
            z-index: -1;
            border-radius: 17px;
        }
        
        .tech-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .tech-icon {
            font-size: 60px;
            margin-bottom: 25px;
            transition: all 0.4s ease;
        }
        
        .tech-card:hover .tech-icon {
            transform: scale(1.2);
            text-shadow: 0 0 20px currentColor;
        }
        
        .tech-icon.html { color: #e34c26; }
        .tech-icon.css { color: #264de4; }
        .tech-icon.js { color: #f0db4f; }
        .tech-icon.java { color: #007396; }
        .tech-icon.cpp { color: #00599c; }
        .tech-icon.python { color: #306998; }
        
        .tech-name {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        .tech-desc {
            color: #94a3b8;
            font-size: 0.95rem;
        }
        
        /* Projetos */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.4s ease;
            border: 1px solid rgba(14, 165, 233, 0.1);
            position: relative;
        }
        
        .project-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }
        
        .project-header {
            padding: 25px;
        }
        
        .project-title {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .project-body {
            padding: 0 25px 25px;
        }
        
        .project-description {
            color: #cbd5e1;
            margin-bottom: 25px;
            line-height: 1.8;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 25px;
        }
        
        .tech-tag {
            background: rgba(14, 165, 233, 0.1);
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, var(--secondary), var(--accent));
            color: white;
            padding: 14px 28px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(14, 165, 233, 0.3);
        }
        
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(14, 165, 233, 0.5);
        }
        
        .links-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .link-card {
            background: rgba(15, 23, 42, 0.7);
            border-radius: 15px;
            padding: 35px;
            text-align: center;
            transition: all 0.4s ease;
            border: 1px solid rgba(14, 165, 233, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .link-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }
        
        .link-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--secondary), var(--terminal));
        }
        
        .link-icon {
            font-size: 50px;
            margin-bottom: 25px;
            color: var(--secondary);
        }
        
        .link-title {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: var(--light);
        }
        
        .link-desc {
            color: #94a3b8;
            margin-bottom: 25px;
        }
        
        .contact-section {
            text-align: center;
            padding: 50px 40px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: rgba(14, 165, 233, 0.1);
            color: var(--secondary);
            font-size: 28px;
            transition: all 0.4s ease;
            border: 2px solid rgba(14, 165, 233, 0.3);
        }
        
        .social-link:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(14, 165, 233, 0.4);
        }
        
        footer {
            text-align: center;
            padding: 40px;
            margin-top: 40px;
            color: #64748b;
            font-size: 1.1rem;
        }
        
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .particle {
            position: absolute;
            border-radius: 50%;
            background: var(--secondary);
            opacity: 0.3;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 30px 20px;
            }
            
            .tech-grid,
            .projects-grid,
            .links-grid {
                grid-template-columns: 1fr;
            }
            
            .terminal {
                padding: 20px 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="tech-grid-bg"></div>
            <div class="header-content">
                <div class="profile-pic">
                    <i class="fas fa-terminal"></i>
                </div>
                <h1>Resky220504</h1>
                <p class="tagline">Desenvolvedor Full Stack | Inovação através de código</p>
                
                <div class="terminal">
                    <div class="terminal-header">
                        <div class="terminal-dots">
                            <div class="dot dot-red"></div>
                            <div class="dot dot-yellow"></div>
                            <div class="dot dot-green"></div>
                        </div>
                        <div class="terminal-title">resky220504-profile</div>
                    </div>
                    <div class="terminal-content">
                        <div><span class="terminal-prompt">$ </span><span class="terminal-command">whoami</span></div>
                        <div class="terminal-output">Desenvolvedor Full Stack com foco em soluções inovadoras</div>
                        
                        <div><span class="terminal-prompt">$ </span><span class="terminal-command">cat localizacao.txt</span></div>
                        <div class="terminal-output">Porto Velho, Rondônia</div>
                        
                        <div><span class="terminal-prompt">$ </span><span class="terminal-command">contact --email</span></div>
                        <div class="terminal-output">feliperesky2004@gmail.com</div>
                    </div>
                </div>
            </div>
        </header>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-microchip"></i> Tecnologias</h2>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-icon html"><i class="fab fa-html5"></i></div>
                    <div class="tech-name">HTML5</div>
                    <div class="tech-desc">Estruturação semântica de aplicações web</div>
                </div>
                <div class="tech-card">
                    <div class="tech-icon css"><i class="fab fa-css3-alt"></i></div>
                    <div class="tech-name">CSS3</div>
                    <div class="tech-desc">Estilização avançada e responsiva</div>
                </div>
                <div class="tech-card">
                    <div class="tech-icon js"><i class="fab fa-js"></i></div>
                    <div class="tech-name">JavaScript</div>
                    <div class="tech-desc">Interatividade e aplicações modernas</div>
                </div>
                <div class="tech-card">
                    <div class="tech-icon java"><i class="fab fa-java"></i></div>
                    <div class="tech-name">Java</div>
                    <div class="tech-desc">Aplicações empresariais robustas</div>
                </div>
                <div class="tech-card">
                    <div class="tech-icon python"><i class="fab fa-python"></i></div>
                    <div class="tech-name">Python</div>
                    <div class="tech-desc">Automação e soluções de dados</div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-code-branch"></i> Projetos</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Trabalho-ADS</h3>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Sistema completo para gerenciamento e visualização de dados acadêmicos com dashboard interativo e relatórios personalizados.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">Java</span>
                            <span class="tech-tag">Spring Boot</span>
                            <span class="tech-tag">MySQL</span>
                        </div>
                        <a href="#" class="btn">
                            <i class="fas fa-external-link-alt"></i> Ver Projeto
                        </a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Pagina_Boletim</h3>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Plataforma meteorológica com atualizações em tempo real, gráficos interativos e alertas personalizados para diversas regiões.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">API Integration</span>
                            <span class="tech-tag">Chart.js</span>
                        </div>
                        <a href="#" class="btn">
                            <i class="fas fa-external-link-alt"></i> Ver Projeto
                        </a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">SistemaWeb</h3>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Aplicação web full-stack com autenticação de usuários, CRUD completo e integração com serviços externos via API REST.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                        </div>
                        <a href="#" class="btn">
                            <i class="fas fa-external-link-alt"></i> Ver Projeto
                        </a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">movbank_mobile</h3>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Aplicativo financeiro mobile com gerenciamento de contas, transferências, investimentos e análise de gastos.</p>
                        <div class="tech-stack">
                            <span class="tech-tag">React Native</span>
                            <span class="tech-tag">Firebase</span>
                            <span class="tech-tag">Redux</span>
                        </div>
                        <a href="#" class="btn">
                            <i class="fas fa-external-link-alt"></i> Ver Projeto
                        </a>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title"><i class="fas fa-network-wired"></i> Links</h2>
            <div class="links-grid">
                <div class="link-card">
                    <div class="link-icon"><i class="fab fa-linkedin"></i></div>
                    <h3 class="link-title">LinkedIn</h3>
                    <p class="link-desc">Conecte-se profissionalmente e veja minha trajetória</p>
                    <a href="#" class="btn">
                        <i class="fas fa-external-link-alt"></i> Acessar Perfil
                    </a>
                </div>
                <div class="link-card">
                    <div class="link-icon"><i class="fas fa-briefcase"></i></div>
                    <h3 class="link-title">Portfólio</h3>
                    <p class="link-desc">Explore meus projetos completos e cases de sucesso</p>
                    <a href="#" class="btn">
                        <i class="fas fa-external-link-alt"></i> Ver Portfólio
                    </a>
                </div>
            </div>
        </section>
        
        <section class="section contact-section">
            <h2 class="section-title"><i class="fas fa-satellite"></i> Conecte-se</h2>
            <p>Se você tem uma ideia inovadora, um projeto desafiador ou quer discutir tecnologia, estou disponível para conexões e novas oportunidades.</p>
            
            <div class="social-links">
                <a href="https://github.com/Resky220504" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="#" class="social-link">
                    <i class="fab fa-twitter"></i>
                </a>
                <a href="https://api.whatsapp.com/send/?phone=556992646823&text&type=phone_number&app_absent=0" class="social-link">
                    <i class="fab fa-whatsapp"></i>
                </a>
                <a href="feliperesky2004@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
            </div>
        </section>
        
        <footer>
            <p>Desenvolvido por Felipe Resky</p>
            <p>Código, inovação e performance</p>
        </footer>
    </div>

    <script>
        // Criar partículas animadas
        document.addEventListener('DOMContentLoaded', function() {
            const particlesContainer = document.createElement('div');
            particlesContainer.className = 'particles';
            document.body.appendChild(particlesContainer);
            
            const colors = ['#0ea5e9', '#8b5cf6', '#10b981'];
            
            for (let i = 0; i < 50; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Propriedades aleatórias
                const size = Math.random() * 5 + 1;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const color = colors[Math.floor(Math.random() * colors.length)];
                const delay = Math.random() * 5;
                const duration = 10 + Math.random() * 20;
                
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                particle.style.background = color;
                particle.style.animation = `float ${duration}s ${delay}s infinite linear`;
                
                particlesContainer.appendChild(particle);
            }
            
            // Adicionar animação de flutuação
            const style = document.createElement('style');
            style.textContent = `
                @keyframes float {
                    0% {
                        transform: translate(0, 0) rotate(0deg);
                        opacity: 0.3;
                    }
                    50% {
                        opacity: 0.6;
                    }
                    100% {
                        transform: translate(${Math.random() * 100 - 50}vw, ${Math.random() * 100 - 50}vh) rotate(360deg);
                        opacity: 0.3;
                    }
                }
            `;
            document.head.appendChild(style);
        });
    </script>
</body>
</html>
