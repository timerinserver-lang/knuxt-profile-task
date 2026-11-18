<template>
  <div class="py-12 md:py-16">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
      
      <!-- Page Header & Breadcrumb -->
      <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-4 pb-6 border-b border-slate-200">
        <div>
          <div class="flex items-center gap-2 text-xs font-medium text-slate-500 mb-1">
            <NuxtLink to="/" class="hover:text-indigo-600 transition-colors">Home</NuxtLink>
            <span>/</span>
            <span class="text-indigo-600 font-semibold">Profile</span>
          </div>
          <h1 class="text-3xl sm:text-4xl font-extrabold text-slate-900 tracking-tight">
            Personal Profile &amp; Biography
          </h1>
          <p class="text-sm sm:text-base text-slate-600 mt-1">
            An in-depth look at my background, education, technical skill set, and personal passions.
          </p>
        </div>

        <div class="flex items-center gap-3">
          <NuxtLink 
            to="/"
            class="inline-flex items-center gap-1.5 px-4 py-2 rounded-lg border border-slate-200 bg-white text-slate-700 hover:bg-slate-50 text-sm font-medium transition-colors shadow-xs"
          >
            <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18" />
            </svg>
            Back to Home
          </NuxtLink>
        </div>
      </div>

      <!-- 1. PERSONAL INFORMATION SECTION -->
      <section class="bg-white rounded-3xl p-6 sm:p-8 border border-slate-200/90 shadow-sm">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-10 h-10 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center font-bold">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
            </svg>
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-bold text-slate-900">Personal Information</h2>
            <p class="text-xs sm:text-sm text-slate-500">Identity, contact details, and career overview</p>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-start">
          <!-- Profile Photo & Summary Card -->
          <div class="md:col-span-4 flex flex-col items-center p-6 bg-slate-50 rounded-2xl border border-slate-200/70 text-center">
            <div class="w-36 h-36 rounded-2xl overflow-hidden ring-4 ring-indigo-500/20 shadow-md mb-4 bg-white">
              <img 
                src="/berto1.jpg" 
                alt="Jobert Jan" 
                class="w-full h-full object-cover object-top"
                onerror="this.src='https://ui-avatars.com/api/?name=Jobert+Jan&background=6366f1&color=fff&size=512';"
              />
            </div>
            <h3 class="text-lg font-bold text-slate-900">Jobert Jan</h3>
            <p class="text-xs font-semibold text-indigo-600">Senior Web Developer</p>
            <span class="mt-2 inline-flex items-center gap-1.5 px-2.5 py-0.5 rounded-full text-xs font-medium bg-emerald-100 text-emerald-800">
              <span class="w-1.5 h-1.5 rounded-full bg-emerald-500"></span>
              Available for Opportunities
            </span>
          </div>

          <!-- Personal Information Grid & Bio -->
          <div class="md:col-span-8 space-y-6">
            <div>
              <h4 class="text-sm font-semibold text-slate-400 uppercase tracking-wider mb-2">About Me</h4>
              <p class="text-slate-600 text-sm sm:text-base leading-relaxed">
                I am a dedicated, quality-focused Senior Web Developer with a strong emphasis on modern frontend ecosystems like <strong>Nuxt.js</strong>, <strong>Vue 3</strong>, and responsive UI engineering with <strong>Tailwind CSS</strong>. I thrive on translating intricate requirements into intuitive, performant digital solutions with exceptional user experiences.
              </p>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-2">
              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Full Name</p>
                <p class="text-sm font-semibold text-slate-800 mt-0.5">Jobert Jan</p>
              </div>

              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Email Address</p>
                <a href="mailto:timerinserver@gmail.com" class="text-sm font-semibold text-indigo-600 hover:underline mt-0.5 block truncate">
                  timerinserver@gmail.com
                </a>
              </div>

              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Location</p>
                <p class="text-sm font-semibold text-slate-800 mt-0.5">Philippines (Remote / Hybrid)</p>
              </div>

              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Languages</p>
                <p class="text-sm font-semibold text-slate-800 mt-0.5">English, Filipino</p>
              </div>

              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Role Focus</p>
                <p class="text-sm font-semibold text-slate-800 mt-0.5">Frontend Architecture &amp; Full-Stack</p>
              </div>

              <div class="p-3.5 rounded-xl bg-slate-50 border border-slate-100">
                <p class="text-xs text-slate-400 font-medium">Preferred Stack</p>
                <p class="text-sm font-semibold text-slate-800 mt-0.5">Nuxt, Vue, TypeScript, Tailwind</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- 2. EDUCATIONAL BACKGROUND SECTION -->
      <section class="bg-white rounded-3xl p-6 sm:p-8 border border-slate-200/90 shadow-sm">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-10 h-10 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center font-bold">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path d="M12 14l9-5-9-5-9 5 9 5z" />
              <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z" />
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222" />
            </svg>
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-bold text-slate-900">Educational Background</h2>
            <p class="text-xs sm:text-sm text-slate-500">Academic credentials and continuous professional learning</p>
          </div>
        </div>

        <div class="space-y-6">
          <!-- Timeline Item 1 -->
          <div class="relative pl-8 sm:pl-10 pb-6 border-l-2 border-indigo-200 last:border-l-0 last:pb-0">
            <div class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-indigo-600 ring-4 ring-indigo-100"></div>
            
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1 mb-2">
              <h3 class="text-lg font-bold text-slate-900">
                Bachelor of Science in Information Technology
              </h3>
              <span class="inline-flex items-center text-xs font-semibold px-2.5 py-1 rounded-md bg-indigo-50 text-indigo-700 w-fit">
                Graduated with Distinction
              </span>
            </div>

            <p class="text-xs font-medium text-slate-500 mb-2">
              Major in Web and Mobile Application Development
            </p>

            <p class="text-slate-600 text-sm leading-relaxed mb-3">
              Comprehensive study focusing on software engineering principles, modern algorithm design, database architecture, and web systems. Completed a capstone project designing and deploying a collaborative full-stack web platform.
            </p>

            <div class="flex flex-wrap gap-2">
              <span class="px-2.5 py-1 rounded-md bg-slate-100 text-slate-700 text-xs font-medium">Software Engineering</span>
              <span class="px-2.5 py-1 rounded-md bg-slate-100 text-slate-700 text-xs font-medium">Database Management Systems</span>
              <span class="px-2.5 py-1 rounded-md bg-slate-100 text-slate-700 text-xs font-medium">Web Systems &amp; Technologies</span>
              <span class="px-2.5 py-1 rounded-md bg-slate-100 text-slate-700 text-xs font-medium">UI/UX Interaction Design</span>
            </div>
          </div>

          <!-- Timeline Item 2 -->
          <div class="relative pl-8 sm:pl-10 pb-2 border-l-2 border-indigo-200 last:border-l-0">
            <div class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-purple-600 ring-4 ring-purple-100"></div>
            
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-1 mb-2">
              <h3 class="text-lg font-bold text-slate-900">
                Continuous Professional Certifications &amp; Training
              </h3>
              <span class="inline-flex items-center text-xs font-semibold px-2.5 py-1 rounded-md bg-purple-50 text-purple-700 w-fit">
                Lifelong Learner
              </span>
            </div>

            <p class="text-slate-600 text-sm leading-relaxed mb-3">
              Actively keeping up with the modern JavaScript ecosystem through verified certifications in Vue.js Masterclasses, Nuxt Architecture, Tailwind CSS Mastery, and Modern TypeScript.
            </p>

            <div class="flex flex-wrap gap-2">
              <span class="px-2.5 py-1 rounded-md bg-purple-50 text-purple-700 text-xs font-medium">Nuxt 3/4 Deep Dive</span>
              <span class="px-2.5 py-1 rounded-md bg-purple-50 text-purple-700 text-xs font-medium">Modern Responsive CSS</span>
              <span class="px-2.5 py-1 rounded-md bg-purple-50 text-purple-700 text-xs font-medium">REST API Design</span>
            </div>
          </div>
        </div>
      </section>

      <!-- 3. SKILLS AND INTERESTS SECTION -->
      <section class="bg-white rounded-3xl p-6 sm:p-8 border border-slate-200/90 shadow-sm">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-10 h-10 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center font-bold">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-bold text-slate-900">Skills &amp; Interests</h2>
            <p class="text-xs sm:text-sm text-slate-500">Technical stack, development strengths, and areas of curiosity</p>
          </div>
        </div>

        <!-- Skills Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          
          <!-- Category A: Frontend Engineering -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-200/80">
            <div class="flex items-center gap-2 mb-4">
              <div class="w-8 h-8 rounded-lg bg-indigo-600 text-white flex items-center justify-center">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <h3 class="font-bold text-slate-900 text-base">Frontend &amp; Frameworks</h3>
            </div>

            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Nuxt.js (Nuxt 3 &amp; 4)</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Vue.js (Composition API)</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Tailwind CSS (v3 &amp; v4)</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">TypeScript &amp; JavaScript ES6+</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">HTML5 &amp; Modern Semantic CSS</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Vite &amp; Nitro Engine</span>
            </div>
          </div>

          <!-- Category B: Backend & Tooling -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-200/80">
            <div class="flex items-center gap-2 mb-4">
              <div class="w-8 h-8 rounded-lg bg-purple-600 text-white flex items-center justify-center">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01" />
                </svg>
              </div>
              <h3 class="font-bold text-slate-900 text-base">Backend &amp; Tooling</h3>
            </div>

            <div class="flex flex-wrap gap-2">
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Node.js</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">RESTful APIs &amp; Fetch</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Git &amp; GitHub Version Control</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">SQL &amp; NoSQL Databases</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">NPM, PNPM &amp; Package Managers</span>
              <span class="px-3 py-1.5 rounded-lg bg-white border border-slate-200 text-slate-800 text-xs font-semibold shadow-2xs">Linux &amp; Shell Scripting</span>
            </div>
          </div>
        </div>

        <!-- Technical Interests Sub-section -->
        <div class="mt-6 pt-6 border-t border-slate-100">
          <h4 class="text-sm font-semibold text-slate-900 mb-3 flex items-center gap-2">
            <span class="w-2 h-2 rounded-full bg-indigo-500"></span>
            Technical Interests &amp; Explorations
          </h4>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 text-xs sm:text-sm text-slate-600">
            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100">
              <strong class="text-slate-800 block mb-1">⚡ SSR &amp; Edge Performance</strong>
              Exploring zero-latency rendering, static edge delivery, and web vitals optimization.
            </div>
            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100">
              <strong class="text-slate-800 block mb-1">🎨 Design Systems</strong>
              Building cohesive UI tokens, reusable component libraries, and accessible interfaces.
            </div>
            <div class="p-3 bg-slate-50 rounded-xl border border-slate-100">
              <strong class="text-slate-800 block mb-1">🤖 AI-Assisted Workflows</strong>
              Integrating agentic AI and modern developer tooling to ship robust applications faster.
            </div>
          </div>
        </div>
      </section>

      <!-- 4. HOBBIES & PASSIONS SECTION -->
      <section class="bg-white rounded-3xl p-6 sm:p-8 border border-slate-200/90 shadow-sm">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-10 h-10 rounded-xl bg-indigo-100 text-indigo-600 flex items-center justify-center font-bold">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-bold text-slate-900">Hobbies &amp; Personal Interests</h2>
            <p class="text-xs sm:text-sm text-slate-500">Activities that spark creativity and keep life balanced</p>
          </div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
          <!-- Hobby 1 -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-100 hover:border-indigo-200 hover:-translate-y-1 transition-all duration-200">
            <div class="w-10 h-10 rounded-xl bg-amber-100 text-amber-600 flex items-center justify-center text-lg mb-3">
              💻
            </div>
            <h3 class="font-bold text-slate-900 text-sm mb-1">Building Side Projects</h3>
            <p class="text-xs text-slate-600 leading-relaxed">
              Experimenting with new web technologies, open-source libraries, and small micro-tools in my spare time.
            </p>
          </div>

          <!-- Hobby 2 -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-100 hover:border-indigo-200 hover:-translate-y-1 transition-all duration-200">
            <div class="w-10 h-10 rounded-xl bg-blue-100 text-blue-600 flex items-center justify-center text-lg mb-3">
              🎮
            </div>
            <h3 class="font-bold text-slate-900 text-sm mb-1">Gaming &amp; Esports</h3>
            <p class="text-xs text-slate-600 leading-relaxed">
              Enjoying strategy, tactical, and RPG titles that test quick thinking, teamwork, and problem-solving skills.
            </p>
          </div>

          <!-- Hobby 3 -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-100 hover:border-indigo-200 hover:-translate-y-1 transition-all duration-200">
            <div class="w-10 h-10 rounded-xl bg-rose-100 text-rose-600 flex items-center justify-center text-lg mb-3">
              📷
            </div>
            <h3 class="font-bold text-slate-900 text-sm mb-1">Photography &amp; Visual Arts</h3>
            <p class="text-xs text-slate-600 leading-relaxed">
              Capturing landscapes, street life, and compositions that train the eye for design balance and contrast.
            </p>
          </div>

          <!-- Hobby 4 -->
          <div class="p-5 rounded-2xl bg-slate-50 border border-slate-100 hover:border-indigo-200 hover:-translate-y-1 transition-all duration-200">
            <div class="w-10 h-10 rounded-xl bg-emerald-100 text-emerald-600 flex items-center justify-center text-lg mb-3">
              ✈️
            </div>
            <h3 class="font-bold text-slate-900 text-sm mb-1">Travel &amp; Outdoor Hikes</h3>
            <p class="text-xs text-slate-600 leading-relaxed">
              Exploring nature, discovering new local cuisines, and resetting energy away from the keyboard.
            </p>
          </div>
        </div>
      </section>

      <!-- Bottom Navigation Footer Link -->
      <div class="text-center pt-4">
        <NuxtLink 
          to="/" 
          class="inline-flex items-center gap-2 px-6 py-3 rounded-xl bg-slate-900 hover:bg-indigo-600 text-white font-semibold text-sm transition-all duration-200 shadow-sm"
        >
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
          </svg>
          Return to Homepage
        </NuxtLink>
      </div>

    </div>
  </div>
</template>

<script setup>
useHead({
  title: 'Profile | Jobert Jan - Senior Web Developer',
  meta: [
    { name: 'description', content: 'Detailed profile of Jobert Jan - Personal info, educational background, skills, interests, and hobbies.' }
  ]
})
</script>
