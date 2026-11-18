<template>
  <header class="sticky top-0 z-40 bg-[#0f1923]/95 backdrop-blur-md border-b-2 border-[#2c3e50] shadow-[0_4px_25px_rgba(0,0,0,0.6)]">
    <!-- Top thin accent line in Valorant Red -->
    <div class="h-0.5 w-full bg-gradient-to-r from-transparent via-[#ff4655] to-transparent"></div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-18">
        
        <!-- Brand / Agent Identity -->
        <NuxtLink to="/" class="flex items-center gap-3.5 group focus:outline-none">
          <!-- Valorant-styled Agent Avatar Box with Cut Corners -->
          <div class="relative w-11 h-11 bg-[#15222e] border-2 border-[#ff4655] shadow-[0_0_15px_rgba(255,70,85,0.4)] val-cut-corner p-0.5 flex items-center justify-center group-hover:scale-105 transition-all duration-300">
            <img 
              src="/berto1.jpg" 
              alt="Jobert Jan" 
              class="w-full h-full object-cover object-top filter contrast-110"
              onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';"
            />
            <span class="hidden font-mono font-black text-sm text-[#ff4655]">JJ</span>
            <!-- Corner red accent dot -->
            <div class="absolute -top-1 -right-1 w-2 h-2 bg-[#ff4655]"></div>
          </div>

          <div class="flex flex-col">
            <div class="flex items-center gap-1.5">
              <span class="text-[10px] font-mono tracking-widest text-[#ff4655] font-bold uppercase">
                // AGENT PROTOCOL
              </span>
              <span class="inline-block w-1.5 h-1.5 rounded-full bg-emerald-400 animate-pulse"></span>
            </div>
            <div class="flex items-baseline gap-2">
              <span class="font-black text-white text-lg tracking-wider uppercase group-hover:text-[#ff4655] transition-colors font-sans">
                Jobert Jan
              </span>
              <span class="hidden sm:inline-block text-[11px] font-mono font-semibold text-[#8b97a5] uppercase">
                [ RADIANT DEV ]
              </span>
            </div>
          </div>
        </NuxtLink>

        <!-- Desktop Navigation Menu -->
        <nav class="hidden md:flex items-center space-x-2 lg:space-x-4">
          <!-- 01 // HOME -->
          <NuxtLink 
            to="/" 
            class="relative px-4 py-2 font-mono text-xs font-bold tracking-widest uppercase transition-all duration-200 group flex items-center gap-2"
            :class="route.path === '/' ? 'text-white bg-[#15222e] border-b-2 border-[#ff4655] shadow-[0_0_15px_rgba(255,70,85,0.25)]' : 'text-[#8b97a5] hover:text-white hover:bg-[#15222e]/60'"
          >
            <span class="text-[10px] text-[#ff4655]">01</span>
            <span>// HOME</span>
            <div v-if="route.path === '/'" class="absolute -top-1 right-1 w-1.5 h-1.5 bg-[#ff4655]"></div>
          </NuxtLink>

          <!-- 02 // DOSSIER (PROFILE) -->
          <NuxtLink 
            to="/profile" 
            class="relative px-4 py-2 font-mono text-xs font-bold tracking-widest uppercase transition-all duration-200 group flex items-center gap-2"
            :class="route.path === '/profile' ? 'text-white bg-[#15222e] border-b-2 border-[#ff4655] shadow-[0_0_15px_rgba(255,70,85,0.25)]' : 'text-[#8b97a5] hover:text-white hover:bg-[#15222e]/60'"
          >
            <span class="text-[10px] text-[#ff4655]">02</span>
            <span>// DOSSIER</span>
            <div v-if="route.path === '/profile'" class="absolute -top-1 right-1 w-1.5 h-1.5 bg-[#ff4655]"></div>
          </NuxtLink>

          <!-- Divider -->
          <div class="h-6 w-px bg-[#2c3e50] mx-1"></div>

          <!-- 03 // CONTACT / COMMS BUTTON -->
          <button 
            @click="openContact"
            type="button"
            class="relative px-5 py-2.5 bg-[#ff4655] hover:bg-[#e03746] text-white font-mono text-xs font-black tracking-widest uppercase val-cut-btn transition-all duration-200 shadow-[0_0_20px_rgba(255,70,85,0.4)] hover:shadow-[0_0_30px_rgba(255,70,85,0.65)] hover:-translate-y-0.5 flex items-center gap-2 group cursor-pointer"
          >
            <span class="w-2 h-2 rounded-full bg-white group-hover:animate-ping"></span>
            <span>COMMS // CONTACT</span>
            <svg class="w-3.5 h-3.5 ml-1 transition-transform group-hover:translate-x-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M14 5l7 7m0 0l-7 7m7-7H3" />
            </svg>
          </button>
        </nav>

        <!-- Mobile Menu Toggle Button -->
        <div class="flex md:hidden">
          <button 
            @click="isMobileMenuOpen = !isMobileMenuOpen"
            type="button" 
            class="p-2.5 bg-[#15222e] border border-[#ff4655]/50 text-white hover:bg-[#ff4655] transition-colors"
            aria-label="Toggle navigation"
          >
            <svg v-if="!isMobileMenuOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <svg v-else class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation Drawer -->
      <div v-show="isMobileMenuOpen" class="md:hidden py-4 border-t border-[#2c3e50] space-y-2 bg-[#0f1923]">
        <NuxtLink 
          to="/" 
          @click="isMobileMenuOpen = false"
          class="flex items-center justify-between px-4 py-3 font-mono text-sm tracking-widest uppercase transition-colors"
          :class="route.path === '/' ? 'text-white bg-[#15222e] border-l-4 border-[#ff4655]' : 'text-[#8b97a5] hover:bg-[#15222e] hover:text-white'"
        >
          <span>01 // HOME</span>
          <span class="text-xs text-[#ff4655]">&rarr;</span>
        </NuxtLink>

        <NuxtLink 
          to="/profile" 
          @click="isMobileMenuOpen = false"
          class="flex items-center justify-between px-4 py-3 font-mono text-sm tracking-widest uppercase transition-colors"
          :class="route.path === '/profile' ? 'text-white bg-[#15222e] border-l-4 border-[#ff4655]' : 'text-[#8b97a5] hover:bg-[#15222e] hover:text-white'"
        >
          <span>02 // DOSSIER</span>
          <span class="text-xs text-[#ff4655]">&rarr;</span>
        </NuxtLink>

        <div class="pt-2 px-2">
          <button 
            @click="openContact(); isMobileMenuOpen = false;"
            class="w-full py-3 bg-[#ff4655] text-white font-mono text-xs font-black tracking-widest uppercase flex items-center justify-center gap-2 shadow-[0_0_20px_rgba(255,70,85,0.4)]"
          >
            <span>OPEN COMMS // 09383808212</span>
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const isMobileMenuOpen = ref(false)
const contactModal = useState('contactModal', () => false)

const openContact = () => {
  contactModal.value = true
}
</script>
