<template>
  <div
    class="floating-drone"
    :class="`section-${currentSection}`"
    :style="droneStyle"
    v-show="showDrone"
  >
    <div class="drone-body">
      <div class="drone-center">
        <div class="drone-camera"></div>
        <div class="drone-led"></div>
      </div>

      <div class="drone-arm arm-1">
        <div class="propeller propeller-1">
          <div class="blade blade-1"></div>
          <div class="blade blade-2"></div>
        </div>
      </div>

      <div class="drone-arm arm-2">
        <div class="propeller propeller-2">
          <div class="blade blade-1"></div>
          <div class="blade blade-2"></div>
        </div>
      </div>

      <div class="drone-arm arm-3">
        <div class="propeller propeller-3">
          <div class="blade blade-1"></div>
          <div class="blade blade-2"></div>
        </div>
      </div>

      <div class="drone-arm arm-4">
        <div class="propeller propeller-4">
          <div class="blade blade-1"></div>
          <div class="blade blade-2"></div>
        </div>
      </div>
    </div>
    <div class="drone-shadow"></div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted, computed } from 'vue'

const scrollY = ref(0)
const windowHeight = ref(0)
const showDrone = ref(false)
const currentSection = ref('hero')

const updateScroll = () => {
  scrollY.value = window.scrollY
  windowHeight.value = window.innerHeight

  // Detectar seção atual baseada no scroll
  const scrollProgress = scrollY.value / (document.documentElement.scrollHeight - windowHeight.value)

  if (scrollProgress < 0.2) {
    currentSection.value = 'hero'
  } else if (scrollProgress < 0.4) {
    currentSection.value = 'skills'
  } else if (scrollProgress < 0.6) {
    currentSection.value = 'projects'
  } else if (scrollProgress < 0.8) {
    currentSection.value = 'experience'
  } else {
    currentSection.value = 'contact'
  }
}

const checkScreenSize = () => {
  showDrone.value = window.innerWidth > 1200
}

onMounted(() => {
  window.addEventListener('scroll', updateScroll)
  window.addEventListener('resize', checkScreenSize)
  updateScroll()
  checkScreenSize()
})

onUnmounted(() => {
  window.removeEventListener('scroll', updateScroll)
  window.removeEventListener('resize', checkScreenSize)
})

const droneStyle = computed(() => {
  const documentHeight = document.documentElement.scrollHeight
  const scrollProgress = scrollY.value / (documentHeight - windowHeight.value)

  // Posição vertical baseada no progresso do scroll
  const baseTop = 15 + (scrollProgress * 60) // Move de 15vh até 75vh

  // Movimento flutuante suave
  const time = Date.now() * 0.001
  const floatingY = Math.sin(time) * 8
  const floatingX = Math.cos(time * 0.7) * 5

  // Rotação baseada na velocidade do scroll
  const rotation = Math.sin(scrollY.value * 0.005) * 8

  // Movimento lateral baseado no scroll
  const lateralMovement = Math.sin(scrollProgress * Math.PI * 2) * 15

  return {
    top: `${Math.max(10, Math.min(85, baseTop + floatingY))}vh`,
    right: `${2 + lateralMovement}rem`,
    transform: `translateY(${floatingY}px) translateX(${floatingX}px) rotate(${rotation}deg)`,
    transition: scrollY.value === 0 ? 'all 0.3s ease-out' : 'none'
  }
})
</script>

<style scoped>
.floating-drone {
  position: fixed;
  z-index: 100;
  pointer-events: none;
  transition: all 0.3s ease-out;
}

.drone-body {
  position: relative;
  width: 80px;
  height: 80px;
  animation: hover 3s ease-in-out infinite;
}

.drone-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 30px;
  height: 20px;
  background: linear-gradient(135deg, #2d3748, #4a5568);
  border-radius: 8px;
  box-shadow: 
    0 2px 8px rgba(0, 0, 0, 0.3),
    inset 0 1px 2px rgba(255, 255, 255, 0.1);
}

.drone-camera {
  position: absolute;
  bottom: -3px;
  left: 50%;
  transform: translateX(-50%);
  width: 8px;
  height: 8px;
  background: linear-gradient(135deg, #1a202c, #2d3748);
  border-radius: 50%;
  border: 1px solid #4a5568;
}

.drone-led {
  position: absolute;
  top: 2px;
  right: 2px;
  width: 4px;
  height: 4px;
  background: #00d4ff;
  border-radius: 50%;
  animation: blink 2s ease-in-out infinite;
  box-shadow: 0 0 6px #00d4ff;
}

.drone-arm {
  position: absolute;
  width: 25px;
  height: 3px;
  background: linear-gradient(90deg, #4a5568, #2d3748);
  border-radius: 2px;
}

.arm-1 {
  top: 15px;
  left: -10px;
  transform: rotate(-45deg);
}

.arm-2 {
  top: 15px;
  right: -10px;
  transform: rotate(45deg);
}

.arm-3 {
  bottom: 15px;
  left: -10px;
  transform: rotate(45deg);
}

.arm-4 {
  bottom: 15px;
  right: -10px;
  transform: rotate(-45deg);
}

.propeller {
  position: absolute;
  width: 20px;
  height: 20px;
  top: -8px;
  right: -2px;
  animation: spin 0.1s linear infinite;
}

.propeller-1, .propeller-3 {
  animation-direction: normal;
}

.propeller-2, .propeller-4 {
  animation-direction: reverse;
}

.blade {
  position: absolute;
  background: rgba(0, 212, 255, 0.3);
  border-radius: 50%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.blade-1 {
  width: 18px;
  height: 2px;
}

.blade-2 {
  width: 2px;
  height: 18px;
}

.drone-shadow {
  position: absolute;
  bottom: -40px;
  left: 50%;
  transform: translateX(-50%);
  width: 60px;
  height: 20px;
  background: radial-gradient(ellipse, rgba(0, 0, 0, 0.2) 0%, transparent 70%);
  border-radius: 50%;
  animation: shadowPulse 3s ease-in-out infinite;
}

/* Animações */
@keyframes hover {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-8px);
  }
}

@keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

@keyframes blink {
  0%, 50% {
    opacity: 1;
    box-shadow: 0 0 6px #00d4ff;
  }
  51%, 100% {
    opacity: 0.3;
    box-shadow: 0 0 2px #00d4ff;
  }
}

@keyframes shadowPulse {
  0%, 100% {
    transform: translateX(-50%) scale(1);
    opacity: 0.2;
  }
  50% {
    transform: translateX(-50%) scale(1.1);
    opacity: 0.3;
  }
}

/* Efeitos especiais baseados no scroll */
.floating-drone:hover .drone-led {
  background: #ff6b6b;
  box-shadow: 0 0 8px #ff6b6b;
}

.floating-drone:hover .blade {
  background: rgba(255, 107, 107, 0.4);
}

/* Responsividade */
@media (max-width: 1200px) {
  .floating-drone {
    display: none;
  }
}

/* Efeitos especiais por seção */
.section-hero .drone-led {
  background: #00d4ff;
  box-shadow: 0 0 8px #00d4ff;
}

.section-hero .blade {
  background: rgba(0, 212, 255, 0.4);
}

.section-skills .drone-led {
  background: #10b981;
  box-shadow: 0 0 8px #10b981;
}

.section-skills .blade {
  background: rgba(16, 185, 129, 0.4);
}

.section-skills .propeller {
  animation-duration: 0.08s;
}

.section-projects .drone-led {
  background: #8b5cf6;
  box-shadow: 0 0 8px #8b5cf6;
}

.section-projects .blade {
  background: rgba(139, 92, 246, 0.4);
}

.section-projects .drone-body {
  animation-duration: 2s;
}

.section-experience .drone-led {
  background: #f59e0b;
  box-shadow: 0 0 8px #f59e0b;
}

.section-experience .blade {
  background: rgba(245, 158, 11, 0.4);
}

.section-contact .drone-led {
  background: #ff6b6b;
  box-shadow: 0 0 8px #ff6b6b;
}

.section-contact .blade {
  background: rgba(255, 107, 107, 0.4);
}

.section-contact .propeller {
  animation-duration: 0.12s;
}

/* Efeito de entrada */
.floating-drone {
  animation: droneEnter 2s ease-out;
}

@keyframes droneEnter {
  0% {
    transform: translateX(100px) translateY(-50px) rotate(15deg);
    opacity: 0;
  }
  100% {
    transform: translateX(0) translateY(0) rotate(0deg);
    opacity: 1;
  }
}

/* Efeito de trail/rastro */
.floating-drone::after {
  content: '';
  position: absolute;
  top: 50%;
  left: -20px;
  width: 15px;
  height: 2px;
  background: linear-gradient(90deg, transparent, rgba(0, 212, 255, 0.3));
  border-radius: 1px;
  animation: trail 0.5s ease-out infinite;
}

@keyframes trail {
  0% {
    opacity: 0;
    transform: translateX(0);
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translateX(-10px);
  }
}
</style>
