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
    padding: 2rem 1rem;
    gap: 0.25rem;
    border-bottom: 1px solid var(--border-color);
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
  }

  .nav-menu-active {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }

  .nav-menu-active .nav-link {
    animation: slideInFromLeft 0.4s cubic-bezier(0.4, 0, 0.2, 1) forwards;
  }

  .nav-menu-active .nav-link:nth-child(1) { animation-delay: 0.1s; }
  .nav-menu-active .nav-link:nth-child(2) { animation-delay: 0.15s; }
  .nav-menu-active .nav-link:nth-child(3) { animation-delay: 0.2s; }
  .nav-menu-active .nav-link:nth-child(4) { animation-delay: 0.25s; }
  .nav-menu-active .nav-link:nth-child(5) { animation-delay: 0.3s; }
  .nav-menu-active .nav-link:nth-child(6) { animation-delay: 0.35s; }

  .nav-link {
    padding: 1rem 1.5rem;
    text-align: center;
    border: none;
    border-radius: 0.75rem;
    margin: 0.125rem 0;
    background: transparent;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    font-size: 1.1rem;
    font-weight: 500;
  }

  .nav-link:hover {
    background: rgba(0, 212, 255, 0.08);
    color: var(--primary-color);
    text-shadow: 0 0 8px rgba(0, 212, 255, 0.5);
    transform: translateX(8px) scale(1.02);
  }

  .nav-link.router-link-active {
    background: rgba(0, 212, 255, 0.12);
    color: var(--primary-color);
    text-shadow: 0 0 10px rgba(0, 212, 255, 0.7);
    font-weight: 600;
    transform: translateX(4px);
  }

  .nav-link::after {
    display: none;
  }

  @keyframes slideInFromLeft {
    0% {
      opacity: 0;
      transform: translateX(-30px);
    }
    100% {
      opacity: 1;
      transform: translateX(0);
    }
  }
}
</style>
