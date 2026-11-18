<template>
  <div>
    <!-- Hero / Welcome Section -->
    <section class="relative overflow-hidden pt-12 pb-20 md:pt-20 md:pb-28">
      <!-- Decorative background glow -->
      <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-indigo-200/40 rounded-full blur-3xl -z-10 pointer-events-none"></div>
      <div class="absolute top-1/3 right-10 w-80 h-80 bg-purple-200/30 rounded-full blur-3xl -z-10 pointer-events-none"></div>

      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
          
          <!-- Text Content -->
          <div class="lg:col-span-7 text-center lg:text-left space-y-6">
            <!-- Welcome Badge -->
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-indigo-50 border border-indigo-100 text-indigo-700 text-xs sm:text-sm font-semibold tracking-wide shadow-xs">
              <span class="inline-block w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
              Welcome to my Personal Portfolio
            </div>

            <!-- Main Heading & Name -->
            <div class="space-y-2">
              <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-slate-900 tracking-tight leading-tight">
                Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-indigo-600 to-purple-600">Jobert Jan</span>
              </h1>
              <p class="text-xl sm:text-2xl font-semibold text-slate-700">
                Senior Web Developer &amp; Nuxt Specialist
              </p>
            </div>

            <!-- Short Introduction -->
            <p class="text-base sm:text-lg text-slate-600 leading-relaxed max-w-2xl mx-auto lg:mx-0">
              Welcome to my personal profile website! I specialize in crafting high-performance, accessible, and elegant web applications using modern JavaScript frameworks like <strong>Nuxt</strong> and <strong>Vue.js</strong>, styled seamlessly with <strong>Tailwind CSS</strong>.
            </p>

            <!-- Navigation / CTA Buttons -->
            <div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 pt-4">
              <NuxtLink 
                to="/profile"
                class="inline-flex items-center justify-center gap-2 px-6 py-3.5 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-semibold text-sm shadow-md hover:shadow-indigo-200 hover:-translate-y-0.5 transition-all duration-200"
              >
                <span>Explore My Profile</span>
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                </svg>
              </NuxtLink>

              <a 
                href="mailto:timerinserver@gmail.com"
                class="inline-flex items-center justify-center gap-2 px-6 py-3.5 rounded-xl bg-white hover:bg-slate-50 text-slate-700 font-semibold text-sm border border-slate-200 shadow-xs hover:border-slate-300 hover:-translate-y-0.5 transition-all duration-200"
              >
                <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
                <span>Get In Touch</span>
              </a>
            </div>

            <!-- Quick Stats -->
            <div class="grid grid-cols-3 gap-4 pt-6 border-t border-slate-200/80 max-w-lg mx-auto lg:mx-0 text-left">
              <div>
                <p class="text-2xl font-bold text-slate-900">5+ Years</p>
                <p class="text-xs text-slate-500">Industry Experience</p>
              </div>
              <div>
                <p class="text-2xl font-bold text-slate-900">20+ Apps</p>
                <p class="text-xs text-slate-500">Delivered &amp; Deployed</p>
              </div>
              <div>
                <p class="text-2xl font-bold text-slate-900">100%</p>
                <p class="text-xs text-slate-500">Client Satisfaction</p>
              </div>
            </div>
          </div>

          <!-- Profile Picture / Avatar Card -->
          <div class="lg:col-span-5 flex justify-center">
            <div class="relative group">
              <!-- Background card glow ring -->
              <div class="absolute -inset-2 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-3xl blur-lg opacity-30 group-hover:opacity-50 transition duration-500"></div>

              <div class="relative w-72 sm:w-80 md:w-88 bg-white p-4 rounded-3xl shadow-xl border border-slate-100 flex flex-col items-center">
                <!-- Avatar Container -->
                <div class="relative w-64 h-64 sm:w-72 sm:h-72 rounded-2xl overflow-hidden shadow-inner bg-slate-100 ring-1 ring-slate-200">
                  <img 
                    src="/berto1.jpg" 
                    alt="Jobert Jan Profile Picture" 
                    class="w-full h-full object-cover object-top hover:scale-105 transition-transform duration-500"
                    onerror="this.src='https://ui-avatars.com/api/?name=Jobert+Jan&background=6366f1&color=fff&size=512';"
                  />
                  
                  <!-- Status badge on image -->
                  <div class="absolute bottom-3 left-3 bg-white/95 backdrop-blur-xs px-3 py-1 rounded-full shadow-md flex items-center gap-1.5 border border-slate-100">
                    <span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span>
                    <span class="text-xs font-semibold text-slate-700">Open to Work</span>
                  </div>
                </div>

                <!-- Avatar Card Footer Details -->
                <div class="mt-4 text-center w-full">
                  <h3 class="text-lg font-bold text-slate-900">Jobert Jan</h3>
                  <p class="text-xs text-indigo-600 font-medium">Full Stack &amp; Frontend Architect</p>
                  
                  <div class="mt-3 pt-3 border-t border-slate-100 flex items-center justify-around text-xs text-slate-500">
                    <span class="flex items-center gap-1">
                      <svg class="w-3.5 h-3.5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                      </svg>
                      Philippines
                    </span>
                    <span class="flex items-center gap-1">
                      <svg class="w-3.5 h-3.5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                      </svg>
                      Fast Learner
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- Highlights Section -->
    <section class="py-16 bg-white border-y border-slate-200/80">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center max-w-2xl mx-auto mb-12">
          <h2 class="text-xs font-bold tracking-widest text-indigo-600 uppercase">Core Competencies</h2>
          <p class="mt-2 text-3xl font-extrabold text-slate-900 tracking-tight sm:text-4xl">
            What I Bring To The Table
          </p>
          <p class="mt-3 text-slate-600 text-sm sm:text-base">
            Combining engineering rigor with intuitive user experience to deliver scalable web products.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <!-- Card 1 -->
          <div class="p-6 rounded-2xl bg-slate-50 border border-slate-200 hover:border-indigo-200 hover:shadow-lg transition-all duration-300 group">
            <div class="w-12 h-12 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center mb-5 group-hover:scale-110 group-hover:bg-indigo-600 group-hover:text-white transition-all">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Modern Nuxt &amp; Vue</h3>
            <p class="text-slate-600 text-sm leading-relaxed">
              Leveraging Nuxt 4, SSR/SSG hydration, server-side data fetching, and state management to build blazing-fast reactive web applications.
            </p>
          </div>

          <!-- Card 2 -->
          <div class="p-6 rounded-2xl bg-slate-50 border border-slate-200 hover:border-indigo-200 hover:shadow-lg transition-all duration-300 group">
            <div class="w-12 h-12 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center mb-5 group-hover:scale-110 group-hover:bg-indigo-600 group-hover:text-white transition-all">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Tailwind CSS &amp; UI Design</h3>
            <p class="text-slate-600 text-sm leading-relaxed">
              Crafting pixel-perfect, responsive interfaces with clean utility-first CSS, adhering to accessibility standards and modern design aesthetics.
            </p>
          </div>

          <!-- Card 3 -->
          <div class="p-6 rounded-2xl bg-slate-50 border border-slate-200 hover:border-indigo-200 hover:shadow-lg transition-all duration-300 group">
            <div class="w-12 h-12 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center mb-5 group-hover:scale-110 group-hover:bg-indigo-600 group-hover:text-white transition-all">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-slate-900 mb-2">Clean Architecture</h3>
            <p class="text-slate-600 text-sm leading-relaxed">
              Writing maintainable, modular, and type-safe code using TypeScript, reusable composables, and structured file architecture.
            </p>
          </div>
        </div>

        <!-- Call to Profile -->
        <div class="mt-12 text-center">
          <NuxtLink 
            to="/profile"
            class="inline-flex items-center gap-2 text-indigo-600 hover:text-indigo-800 font-semibold text-sm group"
          >
            <span>Learn more about my educational background, hobbies, and technical skills</span>
            <span class="group-hover:translate-x-1 transition-transform">&rarr;</span>
          </NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Page meta for Nuxt SEO
useHead({
  title: 'Home | Jobert Jan - Senior Web Developer',
  meta: [
    { name: 'description', content: 'Welcome to the personal profile website of Jobert Jan, Senior Web Developer.' }
  ]
})
</script>
