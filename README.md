<div align="center">
  
  <!-- Animated Hero Section -->
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 50%, #0f2847 100%);
      color: #e0e0e0;
      min-height: 100vh;
      padding: 20px;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
    }

    /* Animated Background */
    .bg-animation {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      overflow: hidden;
    }

    .blob {
      position: absolute;
      opacity: 0.1;
      border-radius: 50%;
      animation: float 20s infinite ease-in-out;
    }

    .blob1 {
      width: 300px;
      height: 300px;
      background: linear-gradient(45deg, #00d4ff, #7c3aed);
      top: -50px;
      left: -50px;
      animation-delay: 0s;
    }

    .blob2 {
      width: 250px;
      height: 250px;
      background: linear-gradient(45deg, #a855f7, #06b6d4);
      bottom: 100px;
      right: -50px;
      animation-delay: 2s;
    }

    .blob3 {
      width: 200px;
      height: 200px;
      background: linear-gradient(45deg, #3b82f6, #10b981);
      top: 50%;
      right: 10%;
      animation-delay: 4s;
    }

    @keyframes float {
      0%, 100% {
        transform: translate(0, 0) scale(1);
      }
      50% {
        transform: translate(30px, -30px) scale(1.1);
      }
    }

    /* Hero Title */
    .hero {
      text-align: center;
      margin-bottom: 60px;
      animation: fadeInDown 1s ease-out;
    }

    .hero-emoji {
      font-size: 80px;
      margin-bottom: 20px;
      animation: bounce 2s infinite;
    }

    .hero-title {
      font-size: 3.5em;
      font-weight: 800;
      margin-bottom: 15px;
      background: linear-gradient(135deg, #00d4ff, #7c3aed, #ec4899);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: slideInUp 0.8s ease-out;
    }

    .hero-subtitle {
      font-size: 1.3em;
      color: #a0aec0;
      animation: slideInUp 0.8s ease-out 0.2s both;
    }

    /* Cards Section */
    .section {
      margin-bottom: 50px;
      animation: fadeIn 1s ease-out;
    }

    .section-title {
      font-size: 2em;
      font-weight: 700;
      margin-bottom: 30px;
      color: #00d4ff;
      text-transform: uppercase;
      letter-spacing: 2px;
      position: relative;
      padding-bottom: 15px;
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, #00d4ff, #7c3aed);
      animation: expandWidth 0.6s ease-out;
    }

    /* About Me Section */
    .about-box {
      background: rgba(30, 41, 59, 0.8);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(0, 212, 255, 0.2);
      border-radius: 15px;
      padding: 40px;
      margin-bottom: 30px;
      animation: slideInUp 0.8s ease-out;
      transition: all 0.3s ease;
    }

    .about-box:hover {
      border-color: rgba(0, 212, 255, 0.5);
      background: rgba(30, 41, 59, 1);
      box-shadow: 0 0 30px rgba(0, 212, 255, 0.2);
      transform: translateY(-5px);
    }

    .about-box p {
      font-size: 1.1em;
      line-height: 1.8;
      color: #cbd5e1;
    }

    /* Interest Items */
    .interests {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .interest-card {
      background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(124, 58, 237, 0.1));
      border: 1px solid rgba(0, 212, 255, 0.3);
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      cursor: pointer;
      transition: all 0.3s ease;
      animation: fadeIn 0.8s ease-out;
    }

    .interest-card:nth-child(1) { animation-delay: 0.1s; }
    .interest-card:nth-child(2) { animation-delay: 0.2s; }
    .interest-card:nth-child(3) { animation-delay: 0.3s; }
    .interest-card:nth-child(4) { animation-delay: 0.4s; }
    .interest-card:nth-child(5) { animation-delay: 0.5s; }

    .interest-card:hover {
      background: linear-gradient(135deg, rgba(0, 212, 255, 0.2), rgba(124, 58, 237, 0.2));
      border-color: rgba(0, 212, 255, 0.8);
      transform: translateY(-10px);
      box-shadow: 0 10px 40px rgba(0, 212, 255, 0.2);
    }

    .interest-icon {
      font-size: 2.5em;
      margin-bottom: 10px;
      animation: rotateIn 0.6s ease-out;
    }

    .interest-card:hover .interest-icon {
      animation: spin 0.6s ease-in-out;
    }

    /* Tech Stack */
    .tech-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
      margin-top: 30px;
    }

    .tech-badge {
      background: rgba(15, 40, 71, 0.8);
      border: 2px solid rgba(0, 212, 255, 0.3);
      border-radius: 8px;
      padding: 12px 20px;
      text-align: center;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      animation: fadeIn 0.8s ease-out;
    }

    .tech-badge:nth-child(1) { animation-delay: 0.1s; }
    .tech-badge:nth-child(2) { animation-delay: 0.2s; }
    .tech-badge:nth-child(3) { animation-delay: 0.3s; }
    .tech-badge:nth-child(4) { animation-delay: 0.4s; }
    .tech-badge:nth-child(5) { animation-delay: 0.5s; }
    .tech-badge:nth-child(6) { animation-delay: 0.6s; }

    .tech-badge:hover {
      background: linear-gradient(135deg, rgba(0, 212, 255, 0.2), rgba(124, 58, 237, 0.2));
      border-color: rgba(0, 212, 255, 0.8);
      color: #00d4ff;
      transform: translateY(-5px);
      box-shadow: 0 8px 25px rgba(0, 212, 255, 0.3);
    }

    /* Fun Fact */
    .fun-fact {
      background: linear-gradient(135deg, rgba(0, 212, 255, 0.15), rgba(124, 58, 237, 0.15));
      border-left: 4px solid rgba(0, 212, 255, 0.8);
      border-radius: 8px;
      padding: 25px;
      margin: 40px 0;
      font-size: 1.2em;
      font-style: italic;
      animation: slideInLeft 0.8s ease-out;
      position: relative;
    }

    .fun-fact::before {
      content: '✨';
      position: absolute;
      top: -15px;
      left: 20px;
      font-size: 2em;
      animation: bounce 2s infinite;
    }

    /* Stats Section */
    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
      margin-top: 40px;
    }

    .stat-box {
      text-align: center;
      padding: 25px;
      background: rgba(30, 41, 59, 0.6);
      border: 1px solid rgba(0, 212, 255, 0.2);
      border-radius: 12px;
      animation: fadeIn 0.8s ease-out;
    }

    .stat-number {
      font-size: 2.5em;
      font-weight: 800;
      color: #00d4ff;
      margin-bottom: 10px;
    }

    .stat-label {
      color: #a0aec0;
      font-size: 0.9em;
    }

    /* Footer */
    .footer {
      text-align: center;
      margin-top: 80px;
      padding-top: 30px;
      border-top: 1px solid rgba(0, 212, 255, 0.2);
      animation: fadeIn 1.2s ease-out;
    }

    .footer-text {
      color: #64748b;
      font-size: 0.9em;
      margin-bottom: 20px;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 25px;
      margin-bottom: 20px;
    }

    .social-link {
      width: 45px;
      height: 45px;
      border: 2px solid rgba(0, 212, 255, 0.5);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: all 0.3s ease;
      font-size: 1.5em;
    }

    .social-link:hover {
      border-color: #00d4ff;
      background: rgba(0, 212, 255, 0.2);
      transform: translateY(-5px);
    }

    /* Animations */
    @keyframes fadeIn {
      from {
        opacity: 0;
      }
      to {
        opacity: 1;
      }
    }

    @keyframes fadeInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-30px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    @keyframes expandWidth {
      from {
        width: 0;
      }
      to {
        width: 60px;
      }
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-15px);
      }
    }

    @keyframes spin {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    @keyframes rotateIn {
      from {
        opacity: 0;
        transform: rotate(-30deg);
      }
      to {
        opacity: 1;
        transform: rotate(0deg);
      }
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero-title {
        font-size: 2.5em;
      }

      .hero-emoji {
        font-size: 60px;
      }

      .section-title {
        font-size: 1.5em;
      }

      .interests {
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      }
    }
  </style>

  <div class="bg-animation">
    <div class="blob blob1"></div>
    <div class="blob blob2"></div>
    <div class="blob blob3"></div>
  </div>

  <div class="container">
    <!-- Hero Section -->
    <div class="hero">
      <div class="hero-emoji">👋</div>
      <h1 class="hero-title">Hi, I'm Samarth</h1>
      <p class="hero-subtitle">Full Stack Developer | AI/ML Enthusiast | Problem Solver</p>
    </div>

    <!-- About Section -->
    <div class="section">
      <h2 class="section-title">About Me</h2>
      <div class="about-box">
        <p>I'm passionate about building innovative solutions at the intersection of AI, machine learning, and modern software development. I love transforming ideas into working projects and constantly pushing the boundaries of what's possible with code.</p>
      </div>

      <h3 style="font-size: 1.3em; margin: 30px 0 20px 0; color: #00d4ff;">🎯 My Passions</h3>
      <div class="interests">
        <div class="interest-card">
          <div class="interest-icon">🤖</div>
          <p><strong>AI & Machine Learning</strong></p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">💡</div>
          <p><strong>Innovation</strong></p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">🛠️</div>
          <p><strong>Full Stack Dev</strong></p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">📱</div>
          <p><strong>Android Apps</strong></p>
        </div>
        <div class="interest-card">
          <div class="interest-icon">⚡</div>
          <p><strong>Competitive Coding</strong></p>
        </div>
      </div>
    </div>

    <!-- What I'm Working On -->
    <div class="section">
      <h2 class="section-title">Currently Working On</h2>
      <div class="about-box">
        <ul style="list-style: none; padding: 0;">
          <li style="margin-bottom: 15px; display: flex; align-items: center;">
            <span style="color: #00d4ff; margin-right: 10px; font-size: 1.3em;">▶</span>
            Improving my coding skills with advanced algorithms
          </li>
          <li style="margin-bottom: 15px; display: flex; align-items: center;">
            <span style="color: #00d4ff; margin-right: 10px; font-size: 1.3em;">▶</span>
            Building real-world projects that solve actual problems
          </li>
          <li style="display: flex; align-items: center;">
            <span style="color: #00d4ff; margin-right: 10px; font-size: 1.3em;">▶</span>
            Learning cutting-edge tools and modern frameworks
          </li>
        </ul>
      </div>
    </div>

    <!-- Tech Stack -->
    <div class="section">
      <h2 class="section-title">Tech Stack</h2>
      <div class="tech-grid">
        <div class="tech-badge">Python</div>
        <div class="tech-badge">JavaScript</div>
        <div class="tech-badge">React</div>
        <div class="tech-badge">Machine Learning</div>
        <div class="tech-badge">Firebase</div>
        <div class="tech-badge">Android</div>
      </div>
    </div>

    <!-- Fun Fact -->
    <div class="fun-fact">
      <strong>Fun Fact:</strong> I believe the best way to learn is by doing. I love turning creative ideas into functional, working projects!
    </div>

    <!-- Stats Section -->
    <div class="stats">
      <div class="stat-box">
        <div class="stat-number">10+</div>
        <div class="stat-label">Projects</div>
      </div>
      <div class="stat-box">
        <div class="stat-number">5+</div>
        <div class="stat-label">Tech Stacks</div>
      </div>
      <div class="stat-box">
        <div class="stat-number">∞</div>
        <div class="stat-label">Passion Level</div>
      </div>
    </div>

    <!-- Footer -->
    <div class="footer">
      <div class="social-links">
        <div class="social-link" title="GitHub">📘 https://github.com/Samarth6840/Samarth6840/</div>
        <div class="social-link" title="LinkedIn">💼 https://www.linkedin.com/in/samarth-joshi-9383112aa/</div>
        <div class="social-link" title="Email">✉️ samarth54922@gmail.com</div>
      </div>
      <p class="footer-text">Made with 💜 | Always open to collaborations</p>
    </div>
  </div>
</div>
