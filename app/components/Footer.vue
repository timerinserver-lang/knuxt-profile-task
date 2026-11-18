<template>
  <footer class="mt-auto bg-white border-t border-slate-200/80">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
      <div class="flex flex-col md:flex-row items-center justify-between gap-4">
        <div class="flex items-center gap-3">
          <div class="w-8 h-8 rounded-full overflow-hidden ring-1 ring-slate-300">
            <img 
              src="/berto1.jpg" 
              alt="Jobert Jan" 
              class="w-full h-full object-cover object-top"
              onerror="this.style.display='none';"
            />
          </div>
          <div>
            <p class="text-sm font-semibold text-slate-800">Jobert Jan</p>
            <p class="text-xs text-slate-500">Built with Nuxt.js & Tailwind CSS</p>
          </div>
        </div>

        <!-- Quick Links -->
        <div class="flex items-center gap-6 text-sm text-slate-600">
          <NuxtLink to="/" class="hover:text-indigo-600 transition-colors">Home</NuxtLink>
          <NuxtLink to="/profile" class="hover:text-indigo-600 transition-colors">Profile</NuxtLink>
          <a href="mailto:timerinserver@gmail.com" class="hover:text-indigo-600 transition-colors">Contact</a>
        </div>

        <p class="text-xs text-slate-400">
          &copy; {{ new Date().getFullYear() }} Jobert Jan. All rights reserved.
        </p>
      </div>
    </div>
  </footer>
</template>
