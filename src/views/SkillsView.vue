<template>
  <div class="skills">
    
    <section class="skills-hero section">
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
          <div class="hero-badge floating">
            <span>⚡ Stack Tecnológico</span>
          </div>
          <h1 class="hero-title gradient-text glow-text">Habilidades & Tecnologias</h1>
          <p class="hero-description">
            Expertise em <strong>tecnologias modernas</strong> de desenvolvimento front-end e <strong>ferramentas essenciais</strong>
            para criar experiências digitais excepcionais e performáticas.
          </p>
          <div class="hero-stats">
            <div class="stat-item">
              <span class="stat-number gradient-text">10+</span>
              <span class="stat-label">Tecnologias</span>
            </div>
            <div class="stat-item">
              <span class="stat-number gradient-text">6+</span>
              <span class="stat-label">Anos Vue.js</span>
            </div>
            <div class="stat-item">
              <span class="stat-number gradient-text">4+</span>
              <span class="stat-label">Anos React</span>
            </div>
            <div class="stat-item">
              <span class="stat-number gradient-text">95%</span>
              <span class="stat-label">Proficiência</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    
    <section class="main-skills section">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title gradient-text">Principais Tecnologias</h2>
          <p class="section-subtitle">
            Domínio avançado nas tecnologias mais utilizadas no desenvolvimento front-end moderno
          </p>
        </div>
        <div class="skills-grid">
          <div class="skill-card featured">
            <div class="skill-icon vue">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M2,3L5.09,12L2,21H6.09L8.5,15L10.91,21H15L12,3H8L5.09,12L2,3Z"/>
              </svg>
            </div>
            <h3>Vue.js</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 95%"></div>
              </div>
              <span class="level-text">Especialista</span>
            </div>
            <p>Vue 2 & 3, Composition API, Vuex, Pinia, Vue Router</p>
            <div class="experience-years">6+ anos</div>
          </div>

          <div class="skill-card featured">
            <div class="skill-icon react">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12,10.11C13.03,10.11 13.87,10.95 13.87,12C13.87,13.05 13.03,13.89 12,13.89C10.97,13.89 10.13,13.05 10.13,12C10.13,10.95 10.97,10.11 12,10.11M7.37,20C8,20.38 9.38,19.8 10.97,18.3C10.45,17.71 9.94,17.07 9.46,16.4C8.64,16.32 7.83,16.2 7.06,16.04C6.55,18.18 6.74,19.65 7.37,20M8.08,14.26L7.79,13.75C7.68,14.04 7.57,14.33 7.5,14.61C7.77,14.67 8.07,14.72 8.38,14.77C8.28,14.6 8.18,14.43 8.08,14.26M14.62,13.5L15.43,12L14.62,10.5C14.32,9.97 14,9.5 13.71,9.03C13.17,9 12.6,9 12,9C11.4,9 10.83,9 10.29,9.03C10,9.5 9.68,9.97 9.38,10.5L8.57,12L9.38,13.5C9.68,14.03 10,14.5 10.29,14.97C10.83,15 11.4,15 12,15C12.6,15 13.17,15 13.71,14.97C14,14.5 14.32,14.03 14.62,13.5M12,6.78C11.81,7 11.61,7.23 11.41,7.5C11.61,7.5 11.8,7.5 12,7.5C12.2,7.5 12.39,7.5 12.59,7.5C12.39,7.23 12.19,7 12,6.78M12,17.22C12.19,17 12.39,16.77 12.59,16.5C12.39,16.5 12.2,16.5 12,16.5C11.8,16.5 11.61,16.5 11.41,16.5C11.61,16.77 11.81,17 12,17.22M16.62,4C16,3.62 14.62,4.2 13.03,5.7C13.55,6.29 14.06,6.93 14.54,7.6C15.36,7.68 16.17,7.8 16.94,7.96C17.45,5.82 17.26,4.35 16.62,4M15.92,9.74L16.21,10.25C16.32,9.96 16.43,9.67 16.5,9.39C16.23,9.33 15.93,9.28 15.62,9.23C15.72,9.4 15.82,9.57 15.92,9.74M17.37,2.69C18.84,3.53 19,5.74 18.38,8.32C20.92,9.07 22.75,10.31 22.75,12C22.75,13.69 20.92,14.93 18.38,15.68C19,18.26 18.84,20.47 17.37,21.31C15.91,22.15 13.92,21.19 12,19.36C10.08,21.19 8.09,22.15 6.62,21.31C5.16,20.47 5,18.26 5.62,15.68C3.08,14.93 1.25,13.69 1.25,12C1.25,10.31 3.08,9.07 5.62,8.32C5,5.74 5.16,3.53 6.62,2.69C8.09,1.85 10.08,2.81 12,4.64C13.92,2.81 15.91,1.85 17.37,2.69M17.08,12C17.42,12.75 17.72,13.5 17.97,14.26C20.07,13.63 21.25,12.73 21.25,12C21.25,11.27 20.07,10.37 17.97,9.74C17.72,10.5 17.42,11.25 17.08,12M6.92,12C6.58,11.25 6.28,10.5 6.03,9.74C3.93,10.37 2.75,11.27 2.75,12C2.75,12.73 3.93,13.63 6.03,14.26C6.28,13.5 6.58,12.75 6.92,12M15.92,14.26C15.82,14.43 15.72,14.6 15.62,14.77C15.93,14.72 16.23,14.67 16.5,14.61C16.43,14.33 16.32,14.04 16.21,13.75L15.92,14.26M8.08,9.74L7.79,10.25C7.68,9.96 7.57,9.67 7.5,9.39C7.77,9.33 8.07,9.28 8.38,9.23C8.28,9.4 8.18,9.57 8.08,9.74Z"/>
              </svg>
            </div>
            <h3>React.js</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 90%"></div>
              </div>
              <span class="level-text">Avançado</span>
            </div>
            <p>React Hooks, Context API, Next.js, Styled Components</p>
            <div class="experience-years">4+ anos</div>
          </div>

          <div class="skill-card">
            <div class="skill-icon js">JS</div>
            <h3>JavaScript</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 95%"></div>
              </div>
              <span class="level-text">Especialista</span>
            </div>
            <p>ES6+, Async/Await, Promises, Functional Programming</p>
            <div class="experience-years">6+ anos</div>
          </div>

          <div class="skill-card">
            <div class="skill-icon ts">TS</div>
            <h3>TypeScript</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 85%"></div>
              </div>
              <span class="level-text">Avançado</span>
            </div>
            <p>Tipagem estática, Interfaces, Generics, Decorators</p>
            <div class="experience-years">3+ anos</div>
          </div>

          <div class="skill-card">
            <div class="skill-icon css">CSS</div>
            <h3>CSS/SASS</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 90%"></div>
              </div>
              <span class="level-text">Avançado</span>
            </div>
            <p>Flexbox, Grid, Animations, Responsive Design</p>
            <div class="experience-years">6+ anos</div>
          </div>

          <div class="skill-card">
            <div class="skill-icon html">HTML</div>
            <h3>HTML5</h3>
            <div class="skill-level">
              <div class="level-bar">
                <div class="level-fill" style="width: 95%"></div>
              </div>
              <span class="level-text">Especialista</span>
            </div>
            <p>Semantic HTML, Accessibility, SEO, Web Standards</p>
            <div class="experience-years">6+ anos</div>
          </div>
        </div>
      </div>
    </section>

    
    <section class="tools-section section">
      <div class="container">
        <h2 class="section-title">Ferramentas & Outras Tecnologias</h2>
        <div class="tools-grid">
          <div class="tool-category">
            <h3>Build Tools & Bundlers</h3>
            <div class="tool-tags">
              <span class="tool-tag">Vite</span>
              <span class="tool-tag">Webpack</span>
              <span class="tool-tag">Parcel</span>
              <span class="tool-tag">Rollup</span>
            </div>
          </div>
          
          <div class="tool-category">
            <h3>Testing</h3>
            <div class="tool-tags">
              <span class="tool-tag">Jest</span>
              <span class="tool-tag">Vitest</span>
              <span class="tool-tag">Testing Library</span>
              <span class="tool-tag">Cypress</span>
            </div>
          </div>
          
          <div class="tool-category">
            <h3>Version Control</h3>
            <div class="tool-tags">
              <span class="tool-tag">Git</span>
              <span class="tool-tag">GitHub</span>
              <span class="tool-tag">GitLab</span>
              <span class="tool-tag">Bitbucket</span>
            </div>
          </div>
          
          <div class="tool-category">
            <h3>Package Managers</h3>
            <div class="tool-tags">
              <span class="tool-tag">npm</span>
              <span class="tool-tag">yarn</span>
              <span class="tool-tag">pnpm</span>
            </div>
          </div>
          
          <div class="tool-category">
            <h3>APIs & HTTP</h3>
            <div class="tool-tags">
              <span class="tool-tag">Axios</span>
              <span class="tool-tag">Fetch API</span>
              <span class="tool-tag">REST</span>
              <span class="tool-tag">GraphQL</span>
            </div>
          </div>
          
          <div class="tool-category">
            <h3>Design & UI</h3>
            <div class="tool-tags">
              <span class="tool-tag">Figma</span>
              <span class="tool-tag">Adobe XD</span>
              <span class="tool-tag">Tailwind CSS</span>
              <span class="tool-tag">Bootstrap</span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.skills-hero {
  position: relative;
  min-height: 80vh;
  display: flex;
  align-items: center;
  overflow: hidden;
  background: transparent;
  text-align: center;
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
  width: 100%;
  z-index: 1;
}

.hero-badge {
  display: inline-block;
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  border: 1px solid var(--border-color);
  border-radius: 2rem;
  padding: 0.75rem 1.5rem;
  margin-bottom: 2rem;
  font-size: 1rem;
  color: var(--primary-color);
  font-weight: 600;
}

.hero-title {
  font-size: 4.5rem;
  font-weight: 900;
  margin-bottom: 2rem;
  text-shadow: 0 0 30px rgba(0, 212, 255, 0.3);
}

.hero-description {
  font-size: 1.5rem;
  color: var(--text-secondary);
  max-width: 800px;
  margin: 0 auto 3rem;
  line-height: 1.7;
}

.hero-description strong {
  color: var(--primary-color);
  font-weight: 700;
}

.hero-stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.stat-item {
  text-align: center;
  padding: 2rem;
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
  transition: var(--transition);
}

.stat-item:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-glow);
  border-color: var(--primary-color);
}

.stat-number {
  display: block;
  font-size: 2.5rem;
  font-weight: 900;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 1rem;
  color: var(--text-secondary);
  font-weight: 600;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 3.5rem;
  font-weight: 900;
  margin-bottom: 1rem;
  text-shadow: 0 0 30px rgba(0, 212, 255, 0.3);
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
  gap: 3rem;
}

.skill-card {
  background: var(--background-card);
  backdrop-filter: blur(20px);
  border-radius: var(--border-radius);
  padding: 3rem;
  text-align: center;
  box-shadow: var(--shadow-md);
  border: 1px solid var(--border-color);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.skill-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
}

.skill-card:hover {
  transform: translateY(-10px);
  box-shadow: var(--shadow-glow);
  border-color: var(--primary-color);
}

.skill-card.featured {
  border: 2px solid var(--primary-color);
  background: var(--background-card);
  box-shadow: var(--shadow-glow);
}

.skill-card.featured::before {
  height: 6px;
  background: linear-gradient(90deg, var(--primary-color), var(--accent-color), var(--primary-color));
}

.skill-card.featured::after {
  content: '⭐';
  position: absolute;
  top: 1.5rem;
  right: 1.5rem;
  font-size: 1.5rem;
  color: var(--primary-color);
}

.skill-icon {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 2rem;
  font-weight: 700;
  font-size: 2rem;
  color: white;
  position: relative;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
}

.skill-icon svg {
  width: 40px;
  height: 40px;
}

.skill-icon.vue {
  background: linear-gradient(135deg, #4fc08d, #42b883);
}

.skill-icon.react {
  background: linear-gradient(135deg, #61dafb, #21a9c7);
}

.skill-icon.js {
  background: linear-gradient(135deg, #f7df1e, #e6c200);
  color: #333;
}

.skill-icon.ts {
  background: linear-gradient(135deg, #3178c6, #235a97);
}

.skill-icon.css {
  background: linear-gradient(135deg, #1572b6, #33a9dc);
}

.skill-icon.html {
  background: linear-gradient(135deg, #e34f26, #f06529);
}

.skill-card h3 {
  font-size: 2rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  color: var(--text-primary);
}

.skill-level {
  margin-bottom: 1.5rem;
}

.level-bar {
  width: 100%;
  height: 12px;
  background: var(--background-dark);
  border-radius: 6px;
  overflow: hidden;
  margin-bottom: 0.75rem;
  border: 1px solid var(--border-color);
}

.level-fill {
  height: 100%;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  border-radius: 6px;
  transition: width 1s ease-in-out;
  position: relative;
}

.level-fill::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
  animation: shimmer 2s infinite;
}

@keyframes shimmer {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

.level-text {
  font-size: 1rem;
  font-weight: 700;
  color: var(--primary-color);
}

.skill-card p {
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1.5rem;
  font-size: 1rem;
}

.experience-years {
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  color: var(--primary-color);
  border: 1px solid var(--border-color);
  padding: 0.75rem 1.5rem;
  border-radius: 1.5rem;
  font-size: 1rem;
  font-weight: 700;
  display: inline-block;
  transition: var(--transition);
}

.experience-years:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  transform: translateY(-2px);
}

.tools-section {
  background: rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(10px);
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 3rem;
}

.tool-category {
  background: var(--background-card);
  backdrop-filter: blur(20px);
  border-radius: var(--border-radius);
  padding: 3rem;
  box-shadow: var(--shadow-md);
  border: 1px solid var(--border-color);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.tool-category::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
}

.tool-category:hover {
  box-shadow: var(--shadow-glow);
  transform: translateY(-10px);
  border-color: var(--primary-color);
}

.tool-category h3 {
  font-size: 1.75rem;
  font-weight: 700;
  margin-bottom: 2rem;
  color: var(--text-primary);
  text-align: center;
}

.tool-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  justify-content: center;
}

.tool-tag {
  background: var(--background-glass);
  backdrop-filter: blur(10px);
  color: var(--primary-color);
  padding: 0.75rem 1.25rem;
  border-radius: 1.5rem;
  font-size: 0.875rem;
  font-weight: 600;
  border: 1px solid var(--border-color);
  transition: var(--transition);
}

.tool-tag:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  transform: translateY(-2px);
  box-shadow: var(--shadow-glow);
}

@keyframes floating {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

@media (max-width: 1024px) {
  .hero-stats {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }

  .skills-grid {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }

  .tools-grid {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 3rem;
  }

  .section-title {
    font-size: 2.5rem;
  }

  .hero-stats {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .skills-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .tools-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .skill-card {
    padding: 2rem;
  }

  .tool-category {
    padding: 2rem;
  }

  .skill-icon {
    width: 80px;
    height: 80px;
    font-size: 1.5rem;
  }

  .floating-element {
    display: none;
  }
}

@media (max-width: 480px) {
  .hero-title {
    font-size: 2rem;
  }

  .section-title {
    font-size: 2rem;
  }

  .skill-card {
    padding: 1.5rem;
  }

  .tool-category {
    padding: 1.5rem;
  }

  .skill-icon {
    width: 60px;
    height: 60px;
    font-size: 1.25rem;
  }

  .tool-tags {
    gap: 0.5rem;
  }

  .tool-tag {
    font-size: 0.75rem;
    padding: 0.5rem 1rem;
  }
}
</style>
