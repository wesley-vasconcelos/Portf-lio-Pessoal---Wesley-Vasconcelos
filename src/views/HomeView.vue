<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="home">
    
    <section class="hero section">
      <div class="hero-background">
        <div class="floating-elements">
          <div class="floating-element element-1"></div>
          <div class="floating-element element-2"></div>
          <div class="floating-element element-3"></div>
          <div class="floating-element element-4"></div>
        </div>
      </div>
      <div class="container">
        <div class="hero-content">
          <div class="hero-text">
            <div class="hero-badge floating">
              <span>👋 Disponível para novos projetos</span>
            </div>
            <h1 class="hero-title">
              Olá, eu sou
              <span class="highlight gradient-text glow-text">Wesley Vasconcelos</span>
            </h1>
            <h2 class="hero-subtitle">
              <span class="typing-effect">Desenvolvedor Front-end Sênior</span>
            </h2>
            <p class="hero-description">
              Focado em <strong>Vue.js</strong>, <strong>React.js</strong> e tecnologias modernas de desenvolvimento web.
              Com mais de <strong>6 anos de experiência</strong>, transformo ideias em interfaces incríveis e funcionais
              que proporcionam experiências digitais memoráveis.
            </p>
            <div class="hero-stats">
              <div class="stat-item">
                <span class="stat-number gradient-text">6+</span>
                <span class="stat-label">Anos de Experiência</span>
              </div>
              <div class="stat-item">
                <span class="stat-number gradient-text">20+</span>
                <span class="stat-label">Projetos Entregues</span>
              </div>
              <div class="stat-item">
                <span class="stat-number gradient-text">5</span>
                <span class="stat-label">Empresas</span>
              </div>
            </div>
            <div class="hero-actions">
              <RouterLink to="/contact" class="btn btn-primary pulse-glow">
                <span>💬</span>
                Entre em Contato
              </RouterLink>
              <RouterLink to="/experience" class="btn btn-outline">
                <span>🚀</span>
                Ver Experiência
              </RouterLink>
            </div>
          </div>
          <div class="hero-visual">
            <div class="profile-card floating">
              <div class="profile-avatar pulse-glow">
                <span class="avatar-text gradient-text">WV</span>
                <div class="avatar-ring"></div>
                <div class="avatar-ring-2"></div>
              </div>
              <div class="profile-info">
                <h3>Wesley Vasconcelos</h3>
                <p class="role-text">Front-end Senior Developer</p>
                <div class="tech-stack">
                  <span class="tech-badge vue">Vue.js</span>
                  <span class="tech-badge react">React</span>
                  <span class="tech-badge ts">TypeScript</span>
                </div>
                <div class="profile-stats">
                  <div class="stat">
                    <span class="stat-number">31</span>
                    <span class="stat-label">Anos</span>
                  </div>
                  <div class="stat">
                    <span class="stat-number">SP</span>
                    <span class="stat-label">Brasil</span>
                  </div>
                </div>
              </div>
            </div>
            <div class="code-snippet floating">
              <div class="code-header">
                <div class="code-dots">
                  <span class="dot red"></span>
                  <span class="dot yellow"></span>
                  <span class="dot green"></span>
                </div>
                <span class="code-title">wesley.vue</span>
              </div>
              <div class="code-content">
                <div class="code-line">
                  <span class="code-tag">&lt;template&gt;</span>
                </div>
                <div class="code-line">
                  <span class="code-indent">  &lt;div class="</span><span class="code-string">developer</span><span class="code-indent">"&gt;</span>
                </div>
                <div class="code-line">
                  <span class="code-indent">    &#123;&#123; </span><span class="code-variable">skills</span><span class="code-indent"> &#125;&#125;</span>
                </div>
                <div class="code-line">
                  <span class="code-indent">  &lt;/div&gt;</span>
                </div>
                <div class="code-line">
                  <span class="code-tag">&lt;/template&gt;</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    
    <section class="skills-preview section">
      <div class="container">
        <div class="skills-header">
          <h2 class="section-title gradient-text">Principais Tecnologias</h2>
          <p class="section-subtitle">
            Domínio completo das tecnologias mais modernas do mercado
          </p>
        </div>
        <div class="skills-grid">
          <div class="skill-card card floating">
            <div class="skill-icon vue pulse-glow">
              <span>Vue</span>
              <div class="skill-particles">
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
              </div>
            </div>
            <h3>Vue.js</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill vue-fill" style="width: 95%"></div>
              </div>
              <span class="level-text">Especialista - 6+ anos</span>
            </div>
            <p>Framework principal com expertise em Vue 2 e Vue 3, Composition API, Pinia</p>
            <div class="skill-tags">
              <span class="tag">Vue 3</span>
              <span class="tag">Composition API</span>
              <span class="tag">Pinia</span>
            </div>
          </div>

          <div class="skill-card card floating">
            <div class="skill-icon react pulse-glow">
              <span>React</span>
              <div class="skill-particles">
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
              </div>
            </div>
            <h3>React.js</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill react-fill" style="width: 90%"></div>
              </div>
              <span class="level-text">Avançado - 4+ anos</span>
            </div>
            <p>Desenvolvimento de SPAs, hooks, context API, Next.js</p>
            <div class="skill-tags">
              <span class="tag">Hooks</span>
              <span class="tag">Next.js</span>
              <span class="tag">Context API</span>
            </div>
          </div>

          <div class="skill-card card floating">
            <div class="skill-icon ts pulse-glow">
              <span>TS</span>
              <div class="skill-particles">
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
              </div>
            </div>
            <h3>TypeScript</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill ts-fill" style="width: 85%"></div>
              </div>
              <span class="level-text">Avançado - 3+ anos</span>
            </div>
            <p>Tipagem estática, interfaces, generics, decorators</p>
            <div class="skill-tags">
              <span class="tag">Interfaces</span>
              <span class="tag">Generics</span>
              <span class="tag">Types</span>
            </div>
          </div>

          <div class="skill-card card floating">
            <div class="skill-icon js pulse-glow">
              <span>JS</span>
              <div class="skill-particles">
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
              </div>
            </div>
            <h3>JavaScript</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill js-fill" style="width: 95%"></div>
              </div>
              <span class="level-text">Especialista - 6+ anos</span>
            </div>
            <p>ES6+, async/await, functional programming, DOM manipulation</p>
            <div class="skill-tags">
              <span class="tag">ES6+</span>
              <span class="tag">Async/Await</span>
              <span class="tag">Functional</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    
    <section class="projects-preview section">
      <div class="container">
        <h2 class="section-title">Projetos em Destaque</h2>
        <p class="section-subtitle">
          Alguns dos projetos reais em que trabalhei durante minha carreira
        </p>
        <div class="projects-grid">
          <div class="project-card card floating">
            <div class="project-icon fintech">💼</div>
            <h3>Conube</h3>
            <p class="project-type">Plataforma Contábil</p>
            <p class="project-description">
              Sistema completo para gestão contábil com foco em automação e eficiência.
            </p>
            <div class="project-tech">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">JavaScript</span>
            </div>
            <a href="https://conube.com.br/" target="_blank" class="project-link">
              Ver Projeto
            </a>
          </div>

          <div class="project-card card floating">
            <div class="project-icon banking">🏦</div>
            <h3>Banco Arbi</h3>
            <p class="project-type">Sistema Bancário</p>
            <p class="project-description">
              Interface para sistema bancário com foco em segurança e UX.
            </p>
            <div class="project-tech">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">TypeScript</span>
            </div>
            <a href="https://www.bancoarbi.com.br/" target="_blank" class="project-link">
              Ver Projeto
            </a>
          </div>

          <div class="project-card card floating">
            <div class="project-icon petcare">🐾</div>
            <h3>Petz</h3>
            <p class="project-type">Pet Care Platform</p>
            <p class="project-description">
              Plataforma de adoção de pets e aplicativo mobile.
            </p>
            <div class="project-tech">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Mobile</span>
            </div>
            <a href="https://www.adotepetz.com.br/quero-adotar" target="_blank" class="project-link">
              Ver Projeto
            </a>
          </div>
        </div>
        <div class="projects-cta">
          <RouterLink to="/projects" class="cta-button">
            Ver Todos os Projetos
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z"/>
            </svg>
          </RouterLink>
        </div>
      </div>
    </section>

    
    <section class="experience-preview section">
      <div class="container">
        <h2 class="section-title">Experiência Recente</h2>
        <div class="experience-cards">
          <div class="experience-card">
            <div class="company-logo">ISH</div>
            <div class="experience-content">
              <h3>Desenvolvedor Front-end Sênior</h3>
              <p class="company">ISH Tecnologia</p>
              <p class="period">Dezembro 2024 - Presente</p>
              <p class="description">
                Desenvolvimento e manutenção de sistemas de coleta de dados,
                migração de Vue.js 2 para Vue.js 3.
              </p>
            </div>
          </div>
          <div class="experience-card">
            <div class="company-logo">ARBI</div>
            <div class="experience-content">
              <h3>Desenvolvedor Front-end</h3>
              <p class="company">Banco Arbi S/A</p>
              <p class="period">Jun 2021 - Mai 2022</p>
              <p class="description">
                Sistema de antecipação de FGTS com Vue.js e Vuex,
                implementação de criptografia para proteção de dados.
              </p>
            </div>
          </div>
        </div>
        <div class="experience-actions">
          <RouterLink to="/experience" class="btn btn-outline">
            Ver Experiência Completa
          </RouterLink>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  overflow: hidden;
  background: transparent;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;
}

.floating-elements {
  position: absolute;
  width: 100%;
  height: 100%;
}

.floating-element {
  position: absolute;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  opacity: 0.1;
  animation: floating 6s ease-in-out infinite;
}

.element-1 {
  width: 100px;
  height: 100px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.element-2 {
  width: 150px;
  height: 150px;
  top: 60%;
  right: 15%;
  animation-delay: 2s;
}

.element-3 {
  width: 80px;
  height: 80px;
  bottom: 30%;
  left: 20%;
  animation-delay: 4s;
}

.element-4 {
  width: 120px;
  height: 120px;
  top: 10%;
  right: 30%;
  animation-delay: 1s;
}

.hero-content {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 6rem;
  align-items: center;
  width: 100%;
  z-index: 1;
}

.hero-badge {
  display: inline-block;
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  border: 1px solid var(--border-color);
  border-radius: 2rem;
  padding: 0.5rem 1rem;
  margin-bottom: 2rem;
  font-size: 0.875rem;
  color: var(--primary-color);
  font-weight: 600;
}

.hero-title {
  font-size: 4rem;
  font-weight: 900;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  color: var(--text-primary);
}

.hero-subtitle {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 2rem;
  color: var(--text-secondary);
}

.typing-effect {
  position: relative;
}

.typing-effect::after {
  content: '|';
  color: var(--primary-color);
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

.hero-description {
  font-size: 1.25rem;
  line-height: 1.8;
  margin-bottom: 3rem;
  color: var(--text-secondary);
}

.hero-description strong {
  color: var(--primary-color);
  font-weight: 700;
}

.hero-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

.stat-item {
  text-align: center;
  padding: 1.5rem;
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
}

.stat-number {
  display: block;
  font-size: 2.5rem;
  font-weight: 900;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 0.875rem;
  color: var(--text-secondary);
  font-weight: 600;
}

.hero-actions {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.hero-visual {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
}

.profile-card {
  background: var(--background-card);
  backdrop-filter: blur(20px);
  border-radius: var(--border-radius);
  padding: 2.5rem;
  text-align: center;
  border: 1px solid var(--border-color);
  position: relative;
  overflow: hidden;
  width: 100%;
  max-width: 350px;
}

.profile-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
}

.profile-avatar {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  background: var(--background-dark);
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 2rem;
  font-size: 2.5rem;
  font-weight: 900;
  position: relative;
  border: 3px solid var(--primary-color);
}

.avatar-ring {
  position: absolute;
  width: 160px;
  height: 160px;
  border: 2px solid var(--primary-color);
  border-radius: 50%;
  border-top-color: transparent;
  animation: spin 3s linear infinite;
}

.avatar-ring-2 {
  position: absolute;
  width: 180px;
  height: 180px;
  border: 1px solid var(--accent-color);
  border-radius: 50%;
  border-bottom-color: transparent;
  animation: spin 4s linear infinite reverse;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.profile-info h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
  font-weight: 700;
}

.role-text {
  color: var(--primary-color);
  margin-bottom: 1.5rem;
  font-weight: 600;
  font-size: 1.1rem;
}

.tech-stack {
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
  flex-wrap: wrap;
}

.tech-badge {
  padding: 0.25rem 0.75rem;
  border-radius: 1rem;
  font-size: 0.75rem;
  font-weight: 600;
  color: white;
}

.tech-badge.vue {
  background: linear-gradient(135deg, #4fc08d, #42b883);
}

.tech-badge.react {
  background: linear-gradient(135deg, #61dafb, #21a9c7);
}

.tech-badge.ts {
  background: linear-gradient(135deg, #3178c6, #235a97);
}

.profile-stats {
  display: flex;
  justify-content: space-around;
  gap: 1rem;
}

.stat {
  text-align: center;
  padding: 1rem;
  background: var(--background-glass);
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
  flex: 1;
}

.stat-number {
  display: block;
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: 0.25rem;
}

.stat-label {
  font-size: 0.75rem;
  color: var(--text-secondary);
}

.code-snippet {
  background: var(--background-card);
  backdrop-filter: blur(20px);
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
  overflow: hidden;
  width: 100%;
  max-width: 300px;
  font-family: 'Fira Code', 'Consolas', monospace;
}

.code-header {
  background: rgba(0, 0, 0, 0.3);
  padding: 0.75rem 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid var(--border-color);
}

.code-dots {
  display: flex;
  gap: 0.5rem;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.dot.red { background: #ff5f56; }
.dot.yellow { background: #ffbd2e; }
.dot.green { background: #27ca3f; }

.code-title {
  font-size: 0.875rem;
  color: var(--text-secondary);
}

.code-content {
  padding: 1rem;
  font-size: 0.875rem;
  line-height: 1.6;
}

.code-line {
  margin-bottom: 0.25rem;
}

.code-tag { color: #ff6b6b; }
.code-string { color: #4ecdc4; }
.code-variable { color: var(--primary-color); }
.code-indent { color: var(--text-secondary); }

.skills-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 3.5rem;
  font-weight: 900;
  margin-bottom: 1rem;
}

.section-subtitle {
  font-size: 1.25rem;
  color: var(--text-secondary);
  max-width: 600px;
  margin: 0 auto;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.skill-card {
  position: relative;
  text-align: center;
  transition: var(--transition);
}

.skill-card:hover {
  transform: translateY(-10px) scale(1.02);
}

.skill-icon {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1.5rem;
  font-weight: 900;
  font-size: 1.5rem;
  color: white;
  position: relative;
  overflow: hidden;
}

.skill-particles {
  position: absolute;
  width: 100%;
  height: 100%;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: white;
  border-radius: 50%;
  animation: particle-float 3s ease-in-out infinite;
}

.particle:nth-child(1) {
  top: 20%;
  left: 20%;
  animation-delay: 0s;
}

.particle:nth-child(2) {
  top: 60%;
  right: 20%;
  animation-delay: 1s;
}

.particle:nth-child(3) {
  bottom: 20%;
  left: 50%;
  animation-delay: 2s;
}

@keyframes particle-float {
  0%, 100% { transform: translateY(0px) scale(1); opacity: 0.7; }
  50% { transform: translateY(-10px) scale(1.2); opacity: 1; }
}

.skill-icon.vue {
  background: linear-gradient(135deg, #4fc08d, #42b883);
}

.skill-icon.react {
  background: linear-gradient(135deg, #61dafb, #21a9c7);
}

.skill-icon.ts {
  background: linear-gradient(135deg, #3178c6, #235a97);
}

.skill-icon.js {
  background: linear-gradient(135deg, #f7df1e, #e6c200);
  color: #333;
}

.skill-card h3 {
  font-size: 1.75rem;
  margin-bottom: 1rem;
  color: var(--text-primary);
  font-weight: 700;
}

.skill-level {
  margin-bottom: 1.5rem;
}

.level-bar {
  width: 100%;
  height: 8px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 4px;
  overflow: hidden;
  margin-bottom: 0.5rem;
}

.level-fill {
  height: 100%;
  border-radius: 4px;
  transition: width 2s ease-in-out;
}

.vue-fill {
  background: linear-gradient(135deg, #4fc08d, #42b883);
}

.react-fill {
  background: linear-gradient(135deg, #61dafb, #21a9c7);
}

.ts-fill {
  background: linear-gradient(135deg, #3178c6, #235a97);
}

.js-fill {
  background: linear-gradient(135deg, #f7df1e, #e6c200);
}

.level-text {
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--primary-color);
}

.skill-card p {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 1.5rem;
  font-size: 1rem;
}

.skill-tags {
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.tag {
  background: var(--background-glass);
  color: var(--primary-color);
  padding: 0.25rem 0.75rem;
  border-radius: 1rem;
  font-size: 0.75rem;
  font-weight: 600;
  border: 1px solid var(--border-color);
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 3rem;
  color: var(--text-primary);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.skill-card {
  background: var(--background-white);
  padding: 2rem;
  border-radius: var(--border-radius);
  text-align: center;
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--border-color);
  transition: var(--transition);
}

.skill-card:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-lg);
}

.skill-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
  font-weight: 700;
  font-size: 1.25rem;
  color: white;
}

.skill-icon.vue {
  background: linear-gradient(135deg, #4fc08d, #42b883);
}

.skill-icon.react {
  background: linear-gradient(135deg, #61dafb, #21a9c7);
}

.skill-icon.ts {
  background: linear-gradient(135deg, #3178c6, #235a97);
}

.skill-icon.js {
  background: linear-gradient(135deg, #f7df1e, #e6c200);
  color: #333;
}

.skill-card h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
}

.skill-card p {
  color: var(--text-secondary);
  line-height: 1.6;
}

.projects-preview {
  background: rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.project-card {
  position: relative;
  transition: var(--transition);
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-icon {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
  font-size: 1.5rem;
  color: white;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
}

.project-icon.fintech {
  background: linear-gradient(135deg, #667eea, #764ba2);
}

.project-icon.banking {
  background: linear-gradient(135deg, #f093fb, #f5576c);
}

.project-icon.petcare {
  background: linear-gradient(135deg, #43e97b, #38f9d7);
}

.project-card h3 {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
}

.project-type {
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: 1rem;
  font-size: 0.875rem;
}

.project-description {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 1rem;
  font-size: 0.875rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.tech-tag {
  background: var(--background-glass);
  color: var(--primary-color);
  padding: 0.25rem 0.75rem;
  border-radius: 1rem;
  font-size: 0.75rem;
  font-weight: 600;
  border: 1px solid var(--border-color);
  transition: var(--transition);
}

.tech-tag:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  transform: translateY(-2px);
}

.project-link {
  display: inline-block;
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  color: var(--primary-color);
  border: 1px solid var(--border-color);
  padding: 0.5rem 1rem;
  border-radius: var(--border-radius);
  text-decoration: none;
  font-weight: 600;
  font-size: 0.875rem;
  transition: var(--transition);
}

.project-link:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  transform: translateY(-2px);
}

.projects-cta {
  text-align: center;
}

.cta-button {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: white;
  padding: 1rem 2rem;
  border-radius: var(--border-radius);
  text-decoration: none;
  font-weight: 700;
  font-size: 1rem;
  transition: var(--transition);
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-glow);
}

.cta-button svg {
  width: 20px;
  height: 20px;
}

.experience-preview {
  background: rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(10px);
}

.experience-cards {
  display: grid;
  gap: 2rem;
  margin-bottom: 3rem;
}

.experience-card {
  display: flex;
  gap: 2rem;
  background: var(--background-card);
  backdrop-filter: blur(20px);
  padding: 2.5rem;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow-md);
  border: 1px solid var(--border-color);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.experience-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
}

.experience-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
  border-color: var(--primary-color);
}

.company-logo {
  width: 80px;
  height: 80px;
  border-radius: var(--border-radius);
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--background-dark);
  font-weight: 900;
  font-size: 1rem;
  flex-shrink: 0;
  box-shadow: var(--shadow-glow);
}

.experience-content h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
  font-weight: 700;
}

.company {
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: 0.25rem;
  font-size: 1.1rem;
}

.period {
  font-size: 0.875rem;
  color: var(--text-muted);
  margin-bottom: 1rem;
  font-weight: 600;
}

.description {
  color: var(--text-secondary);
  line-height: 1.7;
  font-size: 1rem;
}

.experience-actions {
  text-align: center;
}

@media (max-width: 1024px) {
  .hero-content {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
  }

  .hero-stats {
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }

  .skills-grid {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }

  .projects-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2.5rem;
  }

  .hero-subtitle {
    font-size: 1.5rem;
  }

  .hero-stats {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .skills-grid {
    grid-template-columns: 1fr;
  }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .project-card {
    max-width: 100%;
  }

  .project-card.card {
    padding: 1.5rem;
  }

  .project-card h3 {
    font-size: 1.25rem;
  }

  .project-description {
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .experience-card {
    flex-direction: column;
    text-align: center;
    gap: 1.5rem;
  }

  .hero-actions {
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }

  .code-snippet {
    max-width: 100%;
  }

  .profile-card {
    max-width: 100%;
  }

  .floating-element {
    display: none;
  }
}

@media (max-width: 480px) {
  .hero-title {
    font-size: 2rem;
  }

  .hero-subtitle {
    font-size: 1.25rem;
  }

  .section-title {
    font-size: 2rem;
  }

  .projects-grid {
    gap: 1.25rem;
  }

  .project-card.card {
    padding: 1.25rem;
  }

  .project-card h3 {
    font-size: 1.1rem;
    margin-bottom: 0.75rem;
  }

  .project-type {
    font-size: 0.85rem;
    margin-bottom: 0.75rem;
  }

  .project-description {
    font-size: 0.85rem;
    margin-bottom: 1.25rem;
  }

  .project-icon {
    width: 50px;
    height: 50px;
    font-size: 1.25rem;
    margin-bottom: 1rem;
  }

  .project-link {
    padding: 0.6rem 1.25rem;
    font-size: 0.85rem;
  }

  .tech-tag {
    font-size: 0.7rem;
    padding: 0.2rem 0.6rem;
  }

  .skill-icon {
    width: 80px;
    height: 80px;
  }

  .profile-avatar {
    width: 120px;
    height: 120px;
  }

  .avatar-ring {
    width: 140px;
    height: 140px;
  }

  .avatar-ring-2 {
    width: 160px;
    height: 160px;
  }
}
</style>
