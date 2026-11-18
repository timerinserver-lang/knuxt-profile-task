<template>
  <div class="relative py-12 md:py-16">
    <!-- Ambient Lighting Effects -->
    <div class="absolute top-0 right-1/4 w-96 h-96 bg-[#ff4655]/10 rounded-full blur-3xl pointer-events-none -z-10"></div>
    <div class="absolute bottom-10 left-10 w-96 h-96 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none -z-10"></div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
      
      <!-- Top Dossier Navigation & Header Bar -->
      <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4 pb-6 border-b-2 border-[#2c3e50]">
        <div>
          <div class="flex items-center gap-2 text-xs font-mono font-bold text-[#8b97a5] mb-1.5 uppercase">
            <NuxtLink to="/" class="hover:text-[#ff4655] transition-colors">// HOME</NuxtLink>
            <span class="text-[#ff4655]">/</span>
            <span class="text-white">AGENT DOSSIER</span>
            <span class="text-[#ff4655]">// 02</span>
          </div>
          <h1 class="text-3xl sm:text-4xl lg:text-5xl font-black text-white uppercase tracking-tight font-sans">
            Classified Agent Dossier
          </h1>
          <p class="text-xs sm:text-sm font-mono text-[#8b97a5] mt-1">
            RECORD ID: #JJ-2026-VAL // AGENT: JOBERT JAN // SECURITY CLEARANCE: LEVEL 5
          </p>
        </div>

        <div class="flex flex-wrap items-center gap-3">
          <!-- Back Button -->
          <NuxtLink 
            to="/"
            class="px-4 py-2 bg-[#15222e] hover:bg-[#1f2d3d] text-white border border-[#2c3e50] hover:border-[#ff4655] text-xs font-mono font-bold tracking-wider uppercase transition-colors flex items-center gap-2"
          >
            <svg class="w-3.5 h-3.5 text-[#ff4655]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M10 19l-7-7m0 0l7-7m-7 7h18" />
            </svg>
            <span>[ ESC // HOME ]</span>
          </NuxtLink>

          <!-- Comms Button -->
          <button 
            @click="openContact"
            type="button"
            class="px-5 py-2 bg-[#ff4655] hover:bg-[#e03746] text-white text-xs font-mono font-black tracking-widest uppercase val-cut-btn transition-all shadow-[0_0_20px_rgba(255,70,85,0.4)] flex items-center gap-2 cursor-pointer"
          >
            <span class="w-2 h-2 rounded-full bg-white animate-ping"></span>
            <span>OPEN COMMS</span>
          </button>
        </div>
      </div>

      <!-- SECTION 01: AGENT INTEL // PERSONAL DATA -->
      <section class="bg-[#15222e] border-2 border-[#2c3e50] hover:border-[#ff4655]/60 val-cut-corner p-6 sm:p-8 transition-colors relative overflow-hidden">
        
        <div class="flex items-center justify-between pb-4 border-b border-[#2c3e50] mb-6">
          <div class="flex items-center gap-3">
            <span class="w-3 h-3 bg-[#ff4655] rotate-45 inline-block"></span>
            <div>
              <h2 class="text-xl sm:text-2xl font-black text-white uppercase font-sans tracking-wide">
                Section 01 // Agent Intelligence &amp; Personal Data
              </h2>
              <p class="text-xs font-mono text-[#8b97a5]">OPERATIONAL IDENTITY &amp; DIRECT SECURE CHANNELS</p>
            </div>
          </div>
          <span class="hidden sm:inline-block px-2.5 py-1 bg-[#ff4655]/20 text-[#ff4655] border border-[#ff4655]/40 text-[10px] font-mono font-bold uppercase">
            STATUS: ACTIVE DEPLOYMENT
          </span>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
          
          <!-- Agent Card Profile Box -->
          <div class="lg:col-span-4 flex flex-col items-center p-5 bg-[#0f1923] border border-[#2c3e50] val-cut-corner text-center relative group">
            <div class="relative w-44 h-44 bg-[#15222e] border-2 border-[#ff4655] shadow-[0_0_25px_rgba(255,70,85,0.3)] val-cut-corner mb-4 overflow-hidden">
              <img 
                src="/berto1.jpg" 
                alt="Jobert Jan" 
                class="w-full h-full object-cover object-top filter contrast-110"
                onerror="this.src='https://ui-avatars.com/api/?name=Jobert+Jan&background=ff4655&color=fff&size=512';"
              />
              <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent pointer-events-none"></div>
              
              <!-- Crosshair brackets -->
              <div class="absolute top-1.5 left-1.5 w-3 h-3 border-t-2 border-l-2 border-[#ff4655]"></div>
              <div class="absolute bottom-1.5 right-1.5 w-3 h-3 border-b-2 border-r-2 border-[#ff4655]"></div>
            </div>

            <h3 class="text-xl font-black text-white uppercase font-sans tracking-wider">
              Jobert Jan
            </h3>
            <p class="text-xs font-mono font-bold text-[#ff4655] uppercase mt-0.5">
              SENIOR WEB DEVELOPER // SENTINEL
            </p>

            <div class="mt-4 w-full pt-3 border-t border-[#2c3e50] space-y-2 text-left text-xs font-mono">
              <div class="flex items-center justify-between text-[#8b97a5]">
                <span>HOTLINE:</span>
                <a href="tel:09383808212" class="text-white hover:text-[#ff4655] font-bold">09383808212</a>
              </div>
              <div class="flex items-center justify-between text-[#8b97a5]">
                <span>DISPATCH:</span>
                <a href="mailto:timerinserver@gmail.com" class="text-white hover:text-[#ff4655] font-bold truncate max-w-[170px]" title="timerinserver@gmail.com">timerinserver@gmail.com</a>
              </div>
              <div class="flex items-center justify-between text-[#8b97a5]">
                <span>GITHUB:</span>
                <a href="https://github.com/timerinserver-lang" target="_blank" rel="noopener noreferrer" class="text-cyan-400 hover:underline font-bold truncate max-w-[170px]">
                  timerinserver-lang
                </a>
              </div>
            </div>

            <button 
              @click="openContact"
              class="mt-4 w-full py-2 bg-[#ff4655] hover:bg-[#e03746] text-white text-xs font-mono font-black tracking-widest uppercase val-cut-btn transition-colors cursor-pointer"
            >
              TRANSMIT MESSAGE
            </button>
          </div>

          <!-- Tactical Narrative & Information Grid -->
          <div class="lg:col-span-8 space-y-6">
            
            <!-- Agent Operational Brief -->
            <div class="p-4 bg-[#0f1923] border-l-4 border-[#ff4655]">
              <span class="text-[10px] font-mono text-[#ff4655] font-bold uppercase tracking-widest block mb-1">
                // OPERATIONAL BACKGROUND &amp; BRIEFING
              </span>
              <p class="text-sm text-[#ece8e1] leading-relaxed">
                Operating as a lead frontend architect and full-stack engineer, Jobert Jan specializes in orchestrating high-speed web interfaces that refuse to compromise on performance. Grounded in <strong>Nuxt 4</strong>, <strong>Vue 3</strong>, and <strong>Tailwind CSS</strong>, with tactical mastery of modern reactive systems, state management, and edge pre-rendering.
              </p>
            </div>

            <!-- Intel Specs Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3.5">
              
              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">AGENT CALLSIGN</span>
                <span class="text-sm font-bold text-white font-mono mt-0.5 block">Jobert Jan</span>
              </div>

              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">DIRECT PHONE // COMMS</span>
                <div class="flex items-center justify-between">
                  <a href="tel:09383808212" class="text-sm font-bold text-[#ff4655] font-mono mt-0.5 hover:underline">
                    09383808212
                  </a>
                  <span class="text-[10px] font-mono text-emerald-400">● LIVE</span>
                </div>
              </div>

              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">DISPATCH EMAIL</span>
                <a href="mailto:timerinserver@gmail.com" class="text-sm font-bold text-white font-mono mt-0.5 hover:text-[#ff4655] truncate block">
                  timerinserver@gmail.com
                </a>
              </div>

              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">GITHUB REPOSITORY</span>
                <a href="https://github.com/timerinserver-lang" target="_blank" rel="noopener noreferrer" class="text-sm font-bold text-cyan-400 font-mono mt-0.5 hover:underline truncate block">
                  github.com/timerinserver-lang
                </a>
              </div>

              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">DEPLOYMENT REGION</span>
                <span class="text-sm font-bold text-white font-mono mt-0.5 block">Philippines // Remote APAC</span>
              </div>

              <div class="p-3.5 bg-[#0f1923] border border-[#2c3e50]">
                <span class="text-[10px] font-mono text-[#8b97a5] uppercase block">PRIMARY WEAPONS STACK</span>
                <span class="text-sm font-bold text-[#ffd166] font-mono mt-0.5 block">Nuxt 4, Vue 3, Tailwind, TS</span>
              </div>

            </div>

          </div>

        </div>

      </section>

      <!-- SECTION 02: COMBAT TRAINING // ACADEMIC INTEL -->
      <section class="bg-[#15222e] border-2 border-[#2c3e50] hover:border-[#ff4655]/60 val-cut-corner p-6 sm:p-8 transition-colors">
        
        <div class="flex items-center gap-3 pb-4 border-b border-[#2c3e50] mb-6">
          <span class="w-3 h-3 bg-[#ff4655] rotate-45 inline-block"></span>
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-white uppercase font-sans tracking-wide">
              Section 02 // Combat Training &amp; Educational Background
            </h2>
            <p class="text-xs font-mono text-[#8b97a5]">ACADEMIC FOUNDATION &amp; TACTICAL ACCREDITATIONS</p>
          </div>
        </div>

        <div class="space-y-6">
          <!-- Timeline Entry 1 -->
          <div class="relative pl-7 sm:pl-9 pb-6 border-l-2 border-[#ff4655] last:border-l-0 last:pb-0">
            <div class="absolute -left-[7px] top-0 w-3 h-3 bg-[#ff4655] shadow-[0_0_10px_#ff4655]"></div>
            
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1 mb-2">
              <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans">
                Bachelor of Science in Information Technology
              </h3>
              <span class="px-2.5 py-0.5 bg-[#ffd166]/20 text-[#ffd166] border border-[#ffd166]/40 text-xs font-mono font-bold w-fit">
                GRADUATED WITH DISTINCTION
              </span>
            </div>

            <p class="text-xs font-mono text-[#8b97a5] mb-2 uppercase">
              MAJOR: WEB &amp; MOBILE APPLICATION DEVELOPMENT
            </p>

            <p class="text-xs sm:text-sm text-[#ece8e1] leading-relaxed mb-3 font-sans">
              Rigorous curriculum covering data structures, scalable system architecture, relational &amp; NoSQL database engineering, human-computer interaction, and enterprise software pipelines. Delivered a capstone full-stack collaborative platform.
            </p>

            <!-- Coursework Badges -->
            <div class="flex flex-wrap gap-2">
              <span class="px-2.5 py-1 bg-[#0f1923] border border-[#2c3e50] text-[#ece8e1] font-mono text-[11px]">System Architecture</span>
              <span class="px-2.5 py-1 bg-[#0f1923] border border-[#2c3e50] text-[#ece8e1] font-mono text-[11px]">Database Warfare (SQL/NoSQL)</span>
              <span class="px-2.5 py-1 bg-[#0f1923] border border-[#2c3e50] text-[#ece8e1] font-mono text-[11px]">Web Technologies &amp; Protocols</span>
              <span class="px-2.5 py-1 bg-[#0f1923] border border-[#2c3e50] text-[#ece8e1] font-mono text-[11px]">UI/UX Reconnaissance</span>
            </div>
          </div>

          <!-- Timeline Entry 2 -->
          <div class="relative pl-7 sm:pl-9 pb-2 border-l-2 border-[#2c3e50] last:border-l-0">
            <div class="absolute -left-[7px] top-0 w-3 h-3 bg-cyan-400 shadow-[0_0_10px_#00f5d4]"></div>
            
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1 mb-2">
              <h3 class="text-lg font-black text-white uppercase tracking-wider font-sans">
                Advanced Training &amp; Nuxt Mastery Certifications
              </h3>
              <span class="px-2.5 py-0.5 bg-cyan-400/20 text-cyan-400 border border-cyan-400/40 text-xs font-mono font-bold w-fit">
                LIFELONG RADIANT LEARNER
              </span>
            </div>

            <p class="text-xs sm:text-sm text-[#ece8e1] leading-relaxed mb-3 font-sans">
              Continuous reconnaissance in modern web developments, maintaining mastery in Nuxt 4 Nitro server engines, Vue 3 Composition design patterns, and Tailwind utility systems.
            </p>

            <div class="flex flex-wrap gap-2">
              <span class="px-2.5 py-1 bg-[#0f1923] border border-cyan-500/30 text-cyan-300 font-mono text-[11px]">Nuxt 4 / Nitro Architecture</span>
              <span class="px-2.5 py-1 bg-[#0f1923] border border-cyan-500/30 text-cyan-300 font-mono text-[11px]">Zero-Latency SSR Caching</span>
              <span class="px-2.5 py-1 bg-[#0f1923] border border-cyan-500/30 text-cyan-300 font-mono text-[11px]">TypeScript Strict Mode</span>
            </div>
          </div>

        </div>

      </section>

      <!-- SECTION 03: ARSENAL // SKILLS & TECH INTERESTS -->
      <section class="bg-[#15222e] border-2 border-[#2c3e50] hover:border-[#ff4655]/60 val-cut-corner p-6 sm:p-8 transition-colors">
        
        <div class="flex items-center gap-3 pb-4 border-b border-[#2c3e50] mb-6">
          <span class="w-3 h-3 bg-[#ff4655] rotate-45 inline-block"></span>
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-white uppercase font-sans tracking-wide">
              Section 03 // Combat Loadout &amp; Technical Interests
            </h2>
            <p class="text-xs font-mono text-[#8b97a5]">PRIMARY &amp; SECONDARY WEAPONRY ARSENAL</p>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          
          <!-- Primary Arsenal (Frontend) -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] val-cut-top-right">
            <div class="flex items-center gap-2.5 mb-4 text-[#ff4655] font-mono text-xs font-bold uppercase tracking-wider">
              <span class="w-2 h-2 bg-[#ff4655]"></span>
              <span>PRIMARY LOADOUT // FRONTEND WEAPONRY</span>
            </div>

            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#ff4655]/60 text-white font-mono text-xs font-bold shadow-xs">Nuxt 4 (SSR / SSG)</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#ff4655]/60 text-white font-mono text-xs font-bold shadow-xs">Vue.js 3 (Composition API)</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#ff4655]/60 text-white font-mono text-xs font-bold shadow-xs">Tailwind CSS (v3 &amp; v4)</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">TypeScript &amp; ES6+</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">HTML5 &amp; Semantic Web</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">Vite Bundler &amp; Nitro</span>
            </div>
          </div>

          <!-- Secondary Arsenal (Backend & Tools) -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] val-cut-top-right">
            <div class="flex items-center gap-2.5 mb-4 text-cyan-400 font-mono text-xs font-bold uppercase tracking-wider">
              <span class="w-2 h-2 bg-cyan-400"></span>
              <span>SECONDARY LOADOUT // BACKEND &amp; UTILITIES</span>
            </div>

            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1.5 bg-[#15222e] border border-cyan-500/50 text-cyan-300 font-mono text-xs font-bold shadow-xs">Node.js Runtime</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-cyan-500/50 text-cyan-300 font-mono text-xs font-bold shadow-xs">RESTful APIs &amp; Fetch</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-cyan-500/50 text-cyan-300 font-mono text-xs font-bold shadow-xs">Git &amp; GitHub Version Control</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">SQL &amp; PostgreSQL/MySQL</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">NPM, PNPM &amp; Node Ecosystem</span>
              <span class="px-3 py-1.5 bg-[#15222e] border border-[#2c3e50] text-[#ece8e1] font-mono text-xs">PowerShell &amp; Linux Terminal</span>
            </div>
          </div>

        </div>

        <!-- Technical Interests Sub-radar -->
        <div class="mt-6 pt-6 border-t border-[#2c3e50]">
          <span class="text-[10px] font-mono text-[#8b97a5] uppercase tracking-widest block mb-3">
            // RADAR RECON // AREAS OF TECHNICAL PASSION
          </span>

          <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 font-mono text-xs">
            <div class="p-3.5 bg-[#0f1923] border-l-2 border-[#ff4655]">
              <strong class="text-white block mb-1">⚡ ZERO-LATENCY EDGE SSR</strong>
              <p class="text-[#8b97a5] font-sans text-xs">Deploying server-rendered Nuxt nodes on global edge locations for instant TTFB.</p>
            </div>

            <div class="p-3.5 bg-[#0f1923] border-l-2 border-[#ffd166]">
              <strong class="text-white block mb-1">🎮 GAMING HUD &amp; UI SYSTEMS</strong>
              <p class="text-[#8b97a5] font-sans text-xs">Designing immersive, tactile cyber interfaces with micro-interactions and audio-visual punch.</p>
            </div>

            <div class="p-3.5 bg-[#0f1923] border-l-2 border-cyan-400">
              <strong class="text-white block mb-1">🤖 AI-POWERED WORKFLOWS</strong>
              <p class="text-[#8b97a5] font-sans text-xs">Harnessing LLM agents and intelligent toolchains to accelerate software delivery cycles.</p>
            </div>
          </div>
        </div>

      </section>

      <!-- SECTION 04: OFF-DUTY ACTIVITIES // HOBBIES -->
      <section class="bg-[#15222e] border-2 border-[#2c3e50] hover:border-[#ff4655]/60 val-cut-corner p-6 sm:p-8 transition-colors">
        
        <div class="flex items-center gap-3 pb-4 border-b border-[#2c3e50] mb-6">
          <span class="w-3 h-3 bg-[#ff4655] rotate-45 inline-block"></span>
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-white uppercase font-sans tracking-wide">
              Section 04 // Off-Duty Activities &amp; Hobbies
            </h2>
            <p class="text-xs font-mono text-[#8b97a5]">CREATIVE PURSUITS &amp; MENTAL RECHARGING</p>
          </div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
          
          <!-- Hobby 1 -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] hover:border-[#ff4655] val-cut-top-right transition-all group hover:-translate-y-1">
            <div class="text-2xl mb-2">🎯</div>
            <h3 class="text-sm font-black text-white uppercase font-sans tracking-wider mb-1">
              Valorant &amp; Tactical Esports
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Playing competitive tactical shooters that sharpen spatial awareness, rapid decision-making, and high-pressure team comms.
            </p>
          </div>

          <!-- Hobby 2 -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] hover:border-cyan-400 val-cut-top-right transition-all group hover:-translate-y-1">
            <div class="text-2xl mb-2">⌨️</div>
            <h3 class="text-sm font-black text-white uppercase font-sans tracking-wider mb-1">
              Custom Keyboards &amp; Hardware
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Modding custom mechanical keyboards with tuned switches and building high-performance PC battle stations.
            </p>
          </div>

          <!-- Hobby 3 -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] hover:border-[#ffd166] val-cut-top-right transition-all group hover:-translate-y-1">
            <div class="text-2xl mb-2">💻</div>
            <h3 class="text-sm font-black text-white uppercase font-sans tracking-wider mb-1">
              Hacking Side Projects
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Prototyping open-source micro-tools, creative frontend animations, and experimenting with new tech stacks.
            </p>
          </div>

          <!-- Hobby 4 -->
          <div class="p-5 bg-[#0f1923] border border-[#2c3e50] hover:border-emerald-400 val-cut-top-right transition-all group hover:-translate-y-1">
            <div class="text-2xl mb-2">📷</div>
            <h3 class="text-sm font-black text-white uppercase font-sans tracking-wider mb-1">
              Photography &amp; Travel Recon
            </h3>
            <p class="text-xs text-[#8b97a5] font-sans leading-relaxed">
              Capturing landscapes and urban geometry to maintain a sharp eye for visual balance, lighting, and creative contrast.
            </p>
          </div>

        </div>

      </section>

      <!-- Bottom Navigation Footer Link -->
      <div class="text-center pt-4 flex flex-wrap items-center justify-center gap-4">
        <NuxtLink 
          to="/" 
          class="px-6 py-3 bg-[#15222e] hover:bg-[#ff4655] text-white border border-[#2c3e50] hover:border-[#ff4655] font-mono text-xs font-black tracking-widest uppercase transition-all shadow-sm flex items-center gap-2"
        >
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
          </svg>
          <span>RETURN TO HEADQUARTERS // HOME</span>
        </NuxtLink>

        <button 
          @click="openContact"
          type="button"
          class="px-6 py-3 bg-[#ff4655] hover:bg-[#e03746] text-white font-mono text-xs font-black tracking-widest uppercase val-cut-btn transition-all shadow-[0_0_20px_rgba(255,70,85,0.4)] flex items-center gap-2 cursor-pointer"
        >
          <span>TRANSMIT COMMS // 09383808212</span>
        </button>
      </div>

    </div>
  </div>
</template>

<script setup>
const contactModal = useState('contactModal', () => false)
const openContact = () => {
  contactModal.value = true
}

useHead({
  title: 'Agent Dossier // Jobert Jan [Valorant Edition]',
  meta: [
    { name: 'description', content: 'Comprehensive combat and technical dossier of Jobert Jan - Personal intel, educational background, weapon loadouts, and hobbies.' }
  ]
})
</script>
