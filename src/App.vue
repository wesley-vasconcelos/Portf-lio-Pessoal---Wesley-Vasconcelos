<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
import FloatingDrone from './components/FloatingDrone.vue'
</script>

<template>
  <div id="app">
    <NavBar />
    <main>
      <RouterView />
    </main>
    <FloatingDrone />
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  line-height: 1.6;
  color: #e2e8f0;
  background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 25%, #16213e 50%, #0f3460 75%, #533483 100%);
  background-attachment: fixed;
  min-height: 100vh;
}

#app {
  min-height: 100vh;
  width: 100%;
}

main {
  padding-top: 80px;
  width: 100%;
}

:root {
  --primary-color: #00d4ff;
  --secondary-color: #0099cc;
  --accent-color: #ff6b6b;
  --accent-secondary: #4ecdc4;
  --text-primary: #ffffff;
  --text-secondary: #cbd5e1;
  --text-muted: #94a3b8;
  --background-dark: #0f0f23;
  --background-card: rgba(30, 41, 59, 0.8);
  --background-card-hover: rgba(30, 41, 59, 0.95);
  --background-glass: rgba(255, 255, 255, 0.1);
  --border-color: rgba(148, 163, 184, 0.2);
  --border-color-light: rgba(203, 213, 225, 0.1);
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.3);
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.4), 0 2px 4px -2px rgb(0 0 0 / 0.3);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.5), 0 4px 6px -4px rgb(0 0 0 / 0.4);
  --shadow-glow: 0 0 20px rgba(0, 212, 255, 0.3);
  --border-radius: 0.75rem;
  --transition: all 0.3s ease;
}

.container {
  max-width: 1600px;
  margin: 0 auto;
  padding: 0 3rem;
  width: 100%;
}

.section {
  padding: 6rem 0;
  width: 100%;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 1rem 2rem;
  border: none;
  border-radius: var(--border-radius);
  font-weight: 600;
  text-decoration: none;
  transition: var(--transition);
  cursor: pointer;
  position: relative;
  overflow: hidden;
}

.btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s;
}

.btn:hover::before {
  left: 100%;
}

.btn-primary {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  font-weight: 700;
  box-shadow: var(--shadow-glow);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-lg), var(--shadow-glow);
}

.btn-outline {
  background: transparent;
  color: var(--primary-color);
  border: 2px solid var(--primary-color);
  backdrop-filter: blur(10px);
}

.btn-outline:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  color: var(--background-dark);
  transform: translateY(-3px);
  box-shadow: var(--shadow-glow);
}

.card {
  background: var(--background-card);
  backdrop-filter: blur(20px);
  border-radius: var(--border-radius);
  padding: 2rem;
  box-shadow: var(--shadow-md);
  border: 1px solid var(--border-color);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--primary-color), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.card:hover::before {
  opacity: 1;
}

.card:hover {
  background: var(--background-card-hover);
  box-shadow: var(--shadow-lg);
  transform: translateY(-5px);
  border-color: var(--primary-color);
}

.glow-text {
  text-shadow: 0 0 10px var(--primary-color);
}

.gradient-text {
  background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.floating {
  animation: floating 3s ease-in-out infinite;
}

@keyframes floating {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.pulse-glow {
  animation: pulseGlow 2s ease-in-out infinite alternate;
}

@keyframes pulseGlow {
  from { box-shadow: 0 0 20px rgba(0, 212, 255, 0.3); }
  to { box-shadow: 0 0 30px rgba(0, 212, 255, 0.6); }
}

@media (max-width: 1024px) {
  .container {
    padding: 0 2rem;
  }
}

@media (max-width: 768px) {
  .container {
    padding: 0 1rem;
  }

  .section {
    padding: 3rem 0;
  }

  .btn {
    padding: 0.75rem 1.5rem;
  }

  .card {
    padding: 1.5rem;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0 0.5rem;
  }

  .card {
    padding: 1.25rem;
  }

  .section {
    padding: 2rem 0;
  }

  .btn {
    padding: 0.625rem 1.25rem;
    font-size: 0.875rem;
  }
}
</style>
