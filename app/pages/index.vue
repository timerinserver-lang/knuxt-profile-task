<template>
  <div class="relative overflow-hidden py-10 md:py-16">
    <!-- Background Ambient Glow & Watermark -->
    <div class="absolute -top-20 -left-20 w-96 h-96 bg-[#ff4655]/10 rounded-full blur-3xl pointer-events-none -z-10"></div>
    <div class="absolute top-1/2 -right-20 w-96 h-96 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none -z-10"></div>
    <div class="absolute top-20 right-10 text-[#ffffff]/3 text-[180px] font-black select-none pointer-events-none -z-10 leading-none">
      VAL//JJ
    </div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-20">
      
      <!-- Top HUD Coordinates Bar -->
      <div class="flex flex-wrap items-center justify-between gap-2 border-b border-[#2c3e50] pb-3 text-[10px] sm:text-xs font-mono text-[#8b97a5]">
        <div class="flex items-center gap-2">
          <span class="inline-block w-2 h-2 bg-[#ff4655] animate-ping"></span>
          <span class="text-white font-bold tracking-widest">// SECTOR: APAC</span>
          <span class="text-[#ff4655]">|</span>
          <span>GRID: 121.02°E, 14.59°N</span>
        </div>
        <div class="flex items-center gap-3">
          <span>PROTOCOL: NUXT_4_ACTIVE</span>
          <span class="text-emerald-400 font-bold">● ONLINE</span>
        </div>
      </div>

      <!-- HERO SECTION -->
      <section class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        
        <!-- Left: Agent Title & Intel -->
        <div class="lg:col-span-7 space-y-6 text-left">
          
          <!-- Agent Tag Badge -->
          <div class="inline-flex items-center gap-2.5 px-3.5 py-1.5 bg-[#15222e] border-l-4 border-[#ff4655] text-xs font-mono tracking-widest text-[#ece8e1] uppercase shadow-[0_0_15px_rgba(255,70,85,0.2)]">
            <span class="w-1.5 h-1.5 bg-[#ff4655]"></span>
            <span>AGENT CALLSIGN: JOBERT JAN</span>
            <span class="text-[#ff4655]">// 01</span>
          </div>

          <!-- Hero Headline -->
          <div class="space-y-2">
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black text-white tracking-tight uppercase leading-none font-sans">
              DEFEAT THE BUGS.<br />
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#ff4655] via-[#ff6b78] to-[#ffd166]">
                CLUTCH THE CODE.
              </span>
            </h1>
            <p class="text-lg sm:text-xl font-mono font-bold text-[#8b97a5] uppercase tracking-wider">
              // SENIOR WEB DEVELOPER &amp; FULL-STACK RADIANT
            </p>
          </div>

          <!-- Welcome Message & Short Intro -->
          <div class="p-4 bg-[#15222e]/80 border-l-2 border-[#ff4655] backdrop-blur-xs">
            <p class="text-sm sm:text-base text-[#ece8e1] font-sans leading-relaxed">
              Welcome to my digital headquarters! I build mission-critical, high-performance web applications using modern weapons of choice: <strong>Nuxt 4</strong>, <strong>Vue 3</strong>, and <strong>Tailwind CSS</strong>. Engineered for lightning speed, tactical responsiveness, and unstoppable user experience.
            </p>
          </div>

          <!-- Action Buttons / CTA -->
          <div class="flex flex-wrap items-center gap-3.5 pt-2">
            <!-- View Profile CTA -->
            <NuxtLink 
              to="/profile"
              class="px-6 py-3.5 bg-[#ff4655] hover:bg-[#e03746] text-white font-mono text-xs font-black tracking-widest uppercase val-cut-btn transition-all duration-200 shadow-[0_0_25px_rgba(255,70,85,0.45)] hover:shadow-[0_0_35px_rgba(255,70,85,0.7)] hover:-translate-y-0.5 flex items-center gap-2 cursor-pointer"
            >
              <span>VIEW DOSSIER // PROFILE</span>
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </NuxtLink>

            <!-- Open Comms CTA -->
            <button 
              @click="openContact"
              type="button"
              class="px-6 py-3.5 bg-[#15222e] hover:bg-[#1f2d3d] text-white border-2 border-[#2c3e50] hover:border-[#ff4655] font-mono text-xs font-bold tracking-widest uppercase transition-all duration-200 shadow-sm flex items-center gap-2 cursor-pointer group"
            >
              <span class="w-2 h-2 rounded-full bg-[#ff4655] group-hover:animate-ping"></span>
              <span>OPEN COMMS</span>
              <span class="text-[10px] text-[#8b97a5] font-mono">(09383808212)</span>
            </button>

            <!-- GitHub Link -->
            <a 
              href="https://github.com/timerinserver-lang" 
              target="_blank" 
              rel="noopener noreferrer"
              class="px-4 py-3.5 bg-[#0f1923] hover:bg-[#15222e] text-cyan-400 border border-cyan-500/40 hover:border-cyan-400 font-mono text-xs font-bold tracking-widest uppercase transition-colors flex items-center gap-2"
            >
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.53 1.032 1.53 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" />
              </svg>
              <span>GITHUB</span>
            </a>
          </div>

          <!-- Combat / Career Stats Grid -->
          <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 pt-6 border-t border-[#2c3e50]">
            <div class="p-3 bg-[#15222e] border-l-2 border-[#ffd166]">
              <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">RANK TIER</span>
              <span class="text-lg font-black text-[#ffd166] font-mono tracking-wider flex items-center gap-1">
                RADIANT ★
              </span>
            </div>

            <div class="p-3 bg-[#15222e] border-l-2 border-[#ff4655]">
              <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">XP / KDA</span>
              <span class="text-lg font-black text-white font-mono tracking-wider">
                5.0+ YRS
              </span>
            </div>

            <div class="p-3 bg-[#15222e] border-l-2 border-emerald-400">
              <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">WIN RATE</span>
              <span class="text-lg font-black text-emerald-400 font-mono tracking-wider">
                100% CLEAN
              </span>
            </div>

            <div class="p-3 bg-[#15222e] border-l-2 border-cyan-400">
              <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">MAIN AGENT</span>
              <span class="text-lg font-black text-cyan-400 font-mono tracking-wider">
                NUXT 4
              </span>
            </div>
          </div>

        </div>

        <!-- Right: Tactical Valorant Agent Card -->
        <div class="lg:col-span-5 flex justify-center">
          <div class="relative w-full max-w-md group">
            
            <!-- Red tactical outer glow -->
            <div class="absolute -inset-2 bg-gradient-to-r from-[#ff4655]/40 to-cyan-500/20 blur-xl opacity-60 group-hover:opacity-100 transition duration-500"></div>

            <!-- Agent Card Container -->
            <div class="relative bg-[#15222e] border-2 border-[#ff4655] shadow-[0_0_35px_rgba(255,70,85,0.3)] val-cut-corner p-5 sm:p-6 overflow-hidden">
              
              <!-- Card Top Header -->
              <div class="flex items-center justify-between pb-3 border-b border-[#2c3e50] mb-4 text-xs font-mono">
                <span class="text-[#ff4655] font-bold tracking-widest uppercase">
                  // AGENT DOSSIER #01
                </span>
                <span class="px-2 py-0.5 bg-emerald-500/20 text-emerald-400 border border-emerald-500/40 text-[10px] font-bold">
                  ● READY TO DEPLOY
                </span>
              </div>

              <!-- Avatar Image Box with Target Crosshairs -->
              <div class="relative w-full aspect-square bg-[#0f1923] border border-[#2c3e50] overflow-hidden val-cut-corner group-hover:border-[#ff4655] transition-colors">
                <img 
                  src="/berto1.jpg" 
                  alt="Jobert Jan - Valorant Agent" 
                  class="w-full h-full object-cover object-top filter contrast-110 group-hover:scale-105 transition-transform duration-500"
                  onerror="this.src='https://ui-avatars.com/api/?name=Jobert+Jan&background=ff4655&color=fff&size=512';"
                />

                <!-- Scanline tactical overlay -->
                <div class="absolute inset-0 bg-gradient-to-b from-transparent via-black/10 to-[#0f1923]/80 pointer-events-none"></div>

                <!-- HUD target brackets on corners -->
                <div class="absolute top-2 left-2 w-4 h-4 border-t-2 border-l-2 border-[#ff4655] pointer-events-none"></div>
                <div class="absolute top-2 right-2 w-4 h-4 border-t-2 border-r-2 border-[#ff4655] pointer-events-none"></div>
                <div class="absolute bottom-2 left-2 w-4 h-4 border-b-2 border-l-2 border-[#ff4655] pointer-events-none"></div>
                <div class="absolute bottom-2 right-2 w-4 h-4 border-b-2 border-r-2 border-[#ff4655] pointer-events-none"></div>

                <!-- Floating Role Tag -->
                <div class="absolute bottom-3 left-3 bg-[#0f1923]/90 border border-[#ff4655] px-2.5 py-1 text-[10px] font-mono font-bold text-white uppercase tracking-wider flex items-center gap-1.5 shadow-md">
                  <span class="w-1.5 h-1.5 bg-[#ff4655]"></span>
                  <span>ROLE: FRONTEND ARCHITECT</span>
                </div>
              </div>

              <!-- Card Metadata Info -->
              <div class="mt-4 pt-3 border-t border-[#2c3e50] space-y-2">
                <div class="flex items-center justify-between">
                  <div>
                    <h3 class="text-xl font-black text-white uppercase tracking-wider font-sans">
                      Jobert Jan
                    </h3>
                    <p class="text-xs text-[#8b97a5] font-mono">
                      CODE SENTINEL // PHILIPPINES
                    </p>
                  </div>
                  <div class="text-right">
                    <span class="text-[10px] text-[#ff4655] font-mono font-bold block">HOTLINE</span>
                    <a href="tel:09383808212" class="text-xs font-mono font-bold text-white hover:text-[#ff4655]">
                      09383808212
                    </a>
                  </div>
                </div>

                <div class="pt-2 flex items-center justify-between text-[11px] font-mono text-[#8b97a5] border-t border-[#1f2d3d]">
                  <span class="truncate">timerinserver@gmail.com</span>
                  <button 
                    @click="openContact"
                    class="text-xs text-[#ff4655] font-bold hover:underline shrink-0"
                  >
                    [ COMMS ]
                  </button>
                </div>
              </div>

            </div>
          </div>
        </div>

      </section>

      <!-- SIGNATURE ABILITIES // COMBAT ARSENAL -->
      <section class="space-y-8 pt-8">
        
        <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4 border-b-2 border-[#2c3e50] pb-4">
          <div>
            <div class="flex items-center gap-2 text-xs font-mono font-bold tracking-widest text-[#ff4655] uppercase">
              <span class="w-2 h-2 bg-[#ff4655]"></span>
              <span>AGENT LOADOUT // CORE ABILITIES</span>
            </div>
            <h2 class="text-3xl sm:text-4xl font-black text-white tracking-tight uppercase font-sans mt-1">
              Tactical Combat Abilities
            </h2>
          </div>
          <span class="text-xs font-mono text-[#8b97a5]">
            KEYBINDINGS: [C] [Q] [E] [X]
          </span>
        </div>

        <!-- Ability Grid (C, Q, E, X) -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          
          <!-- Ability 1: [C] -->
          <div class="p-6 bg-[#15222e] border border-[#2c3e50] hover:border-[#ff4655] val-cut-top-right transition-all duration-300 group hover:-translate-y-1">
            <div class="flex items-center justify-between mb-4">
              <span class="w-8 h-8 flex items-center justify-center bg-[#0f1923] border border-[#ff4655] font-mono font-black text-[#ff4655] text-sm group-hover:bg-[#ff4655] group-hover:text-white transition-colors">
                C
              </span>
              <span class="text-[10px] font-mono text-cyan-400 tracking-wider">BASIC // REACTIVITY</span>
            </div>
            <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans mb-2">
              Vue 3 Reflex
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Instantaneous reactive state synchronization using Vue 3 Composition API, custom composables, and Pinia stores.
            </p>
          </div>

          <!-- Ability 2: [Q] -->
          <div class="p-6 bg-[#15222e] border border-[#2c3e50] hover:border-[#ff4655] val-cut-top-right transition-all duration-300 group hover:-translate-y-1">
            <div class="flex items-center justify-between mb-4">
              <span class="w-8 h-8 flex items-center justify-center bg-[#0f1923] border border-[#ff4655] font-mono font-black text-[#ff4655] text-sm group-hover:bg-[#ff4655] group-hover:text-white transition-colors">
                Q
              </span>
              <span class="text-[10px] font-mono text-cyan-400 tracking-wider">UTILITY // STYLING</span>
            </div>
            <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans mb-2">
              Tailwind Precision
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Zero-bloat utility architecture, pixel-perfect tactical responsive breakpoints, and custom gaming design tokens.
            </p>
          </div>

          <!-- Ability 3: [E] Signature -->
          <div class="p-6 bg-[#15222e] border-2 border-[#ff4655] shadow-[0_0_20px_rgba(255,70,85,0.2)] val-cut-top-right transition-all duration-300 group hover:-translate-y-1 relative">
            <div class="absolute -top-3 right-4 px-2 py-0.5 bg-[#ff4655] text-white font-mono text-[9px] font-black uppercase tracking-widest">
              SIGNATURE
            </div>
            <div class="flex items-center justify-between mb-4">
              <span class="w-8 h-8 flex items-center justify-center bg-[#ff4655] font-mono font-black text-white text-sm">
                E
              </span>
              <span class="text-[10px] font-mono text-[#ff4655] tracking-wider">FRAMEWORK // MATRIX</span>
            </div>
            <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans mb-2">
              Nuxt 4 Velocity
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              High-speed SSR pre-rendering, automatic routing, Nitro engine endpoints, and effortless static deployment pipelines.
            </p>
          </div>

          <!-- Ability 4: [X] Ultimate -->
          <div class="p-6 bg-[#15222e] border border-[#ffd166] hover:shadow-[0_0_20px_rgba(255,209,102,0.3)] val-cut-top-right transition-all duration-300 group hover:-translate-y-1 relative">
            <div class="absolute -top-3 right-4 px-2 py-0.5 bg-[#ffd166] text-black font-mono text-[9px] font-black uppercase tracking-widest">
              ULTIMATE
            </div>
            <div class="flex items-center justify-between mb-4">
              <span class="w-8 h-8 flex items-center justify-center bg-[#0f1923] border border-[#ffd166] font-mono font-black text-[#ffd166] text-sm group-hover:bg-[#ffd166] group-hover:text-black transition-colors">
                X
              </span>
              <span class="text-[10px] font-mono text-[#ffd166] tracking-wider">CLUTCH // FULL STACK</span>
            </div>
            <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans mb-2">
              Full-Stack Victory
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              End-to-end TypeScript safety, rock-solid REST API integrations, and resilient architecture that cluthes under pressure.
            </p>
          </div>

        </div>

      </section>

      <!-- Bottom Dossier Callout Banner -->
      <section class="p-8 bg-[#15222e] border-2 border-[#2c3e50] val-cut-corner flex flex-col md:flex-row items-center justify-between gap-6">
        <div class="space-y-1 text-left">
          <span class="text-[11px] font-mono font-bold tracking-widest text-[#ff4655] uppercase">
            // INTEL ARCHIVE UNLOCKED
          </span>
          <h3 class="text-2xl font-black text-white uppercase font-sans">
            Ready to Inspect the Full Dossier?
          </h3>
          <p class="text-xs sm:text-sm text-[#8b97a5]">
            Review detailed personal records, academic credentials, combat equipment, and off-duty hobbies.
          </p>
        </div>

        <div class="flex items-center gap-3 shrink-0">
          <NuxtLink 
            to="/profile"
            class="px-6 py-3 bg-[#ff4655] hover:bg-[#e03746] text-white font-mono text-xs font-black tracking-widest uppercase val-cut-btn transition-all shadow-[0_0_20px_rgba(255,70,85,0.4)]"
          >
            ENTER DOSSIER &rarr;
          </NuxtLink>
        </div>
      </section>

    </div>
  </div>
</template>

<script setup>
const contactModal = useState('contactModal', () => false)
const openContact = () => {
  contactModal.value = true
}

useHead({
  title: 'Jobert Jan // Radiant Web Developer [Valorant Edition]',
  meta: [
    { name: 'description', content: 'Gaming-inspired personal portfolio of Jobert Jan, Senior Web Developer specialized in Nuxt 4, Vue 3, and Tailwind CSS.' }
  ]
})
</script>
