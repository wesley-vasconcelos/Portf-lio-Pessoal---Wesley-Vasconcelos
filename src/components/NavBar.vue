<template>
  <nav class="navbar">
    <div class="container">
      <div class="nav-content">
        <div class="nav-brand">
          <RouterLink to="/" class="brand-link">
            <span class="brand-text">Wesley Vasconcelos</span>
          </RouterLink>
        </div>
        
        <div class="nav-menu" :class="{ 'nav-menu-active': isMenuOpen }">
          <RouterLink to="/" class="nav-link" @click="closeMenu">Início</RouterLink>
          <RouterLink to="/about" class="nav-link" @click="closeMenu">Sobre</RouterLink>
          <RouterLink to="/experience" class="nav-link" @click="closeMenu">Experiência</RouterLink>
          <RouterLink to="/skills" class="nav-link" @click="closeMenu">Habilidades</RouterLink>
          <RouterLink to="/projects" class="nav-link" @click="closeMenu">Projetos</RouterLink>
          <RouterLink to="/contact" class="nav-link" @click="closeMenu">Contato</RouterLink>
        </div>
        
        <button 
          class="nav-toggle"
          @click="toggleMenu"
          :aria-expanded="isMenuOpen"
          aria-label="Toggle navigation menu"
        >
          <span class="hamburger-line" :class="{ 'active': isMenuOpen }"></span>
          <span class="hamburger-line" :class="{ 'active': isMenuOpen }"></span>
          <span class="hamburger-line" :class="{ 'active': isMenuOpen }"></span>
        </button>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink } from 'vue-router'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: rgba(15, 15, 35, 0.95);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--border-color);
  z-index: 1000;
  transition: var(--transition);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
}

.nav-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 0;
}

.brand-link {
  text-decoration: none;
  color: var(--text-primary);
  font-weight: 700;
  font-size: 1.25rem;
  transition: var(--transition);
}

.brand-link:hover {
  color: var(--primary-color);
}

.brand-text {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
}

.nav-menu {
  display: flex;
  align-items: center;
  gap: 2rem;
}

.nav-link {
  text-decoration: none;
  color: var(--text-secondary);
  font-weight: 500;
  padding: 0.75rem 1rem;
  position: relative;
  transition: var(--transition);
  border-radius: var(--border-radius);
}

.nav-link:hover {
  color: var(--primary-color);
  background: var(--background-glass);
  text-shadow: 0 0 10px var(--primary-color);
}

.nav-link.router-link-active {
  color: var(--primary-color);
  background: var(--background-glass);
  text-shadow: 0 0 10px var(--primary-color);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  transition: width 0.3s ease;
}

.nav-link:hover::after,
.nav-link.router-link-active::after {
  width: 100%;
}

.nav-toggle {
  display: none;
  flex-direction: column;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
  gap: 0.25rem;
}

.hamburger-line {
  width: 25px;
  height: 3px;
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  transition: var(--transition);
  transform-origin: center;
  box-shadow: 0 0 5px var(--primary-color);
}

.hamburger-line.active:nth-child(1) {
  transform: rotate(45deg) translate(6px, 6px);
}

.hamburger-line.active:nth-child(2) {
  opacity: 0;
}

.hamburger-line.active:nth-child(3) {
  transform: rotate(-45deg) translate(6px, -6px);
}

/* Mobile Styles */
@media (max-width: 768px) {
  .nav-toggle {
    display: flex;
  }
  
  .nav-menu {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: rgba(15, 15, 35, 0.98);
    backdrop-filter: blur(20px);
    flex-direction: column;
    padding: 1rem;
    gap: 1rem;
    border-bottom: 1px solid var(--border-color);
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: var(--transition);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
  }
  
  .nav-menu-active {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  
  .nav-link {
    padding: 0.75rem 0;
    text-align: center;
    border-bottom: 1px solid var(--border-color);
  }
  
  .nav-link:last-child {
    border-bottom: none;
  }
}
</style>
