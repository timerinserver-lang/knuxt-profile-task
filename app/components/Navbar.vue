<template>
  <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-slate-200/80 transition-shadow">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo / Brand -->
        <NuxtLink to="/" class="flex items-center gap-3 group focus:outline-none">
          <div class="w-10 h-10 rounded-full overflow-hidden ring-2 ring-indigo-500/30 group-hover:ring-indigo-500 transition-all duration-300 shadow-sm flex items-center justify-center bg-indigo-50">
            <img 
              src="/berto1.jpg" 
              alt="Jobert Jan" 
              class="w-full h-full object-cover object-top"
              onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';"
            />
            <span class="hidden font-bold text-indigo-600 text-sm tracking-wide">JJ</span>
          </div>
          <div class="flex flex-col">
            <span class="font-bold text-slate-900 tracking-tight text-base group-hover:text-indigo-600 transition-colors">
              Jobert Jan
            </span>
            <span class="text-xs font-medium text-slate-500">
              Senior Web Developer
            </span>
          </div>
        </NuxtLink>

        <!-- Desktop Navigation Links -->
        <nav class="hidden md:flex items-center space-x-1 lg:space-x-2">
          <NuxtLink 
            to="/" 
            class="px-3.5 py-2 rounded-lg text-sm font-medium transition-all duration-200"
            :class="route.path === '/' ? 'text-indigo-600 bg-indigo-50/80 font-semibold shadow-xs' : 'text-slate-600 hover:text-slate-900 hover:bg-slate-100'"
          >
            <span class="flex items-center gap-1.5">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
              </svg>
              Home
            </span>
          </NuxtLink>

          <NuxtLink 
            to="/profile" 
            class="px-3.5 py-2 rounded-lg text-sm font-medium transition-all duration-200"
            :class="route.path === '/profile' ? 'text-indigo-600 bg-indigo-50/80 font-semibold shadow-xs' : 'text-slate-600 hover:text-slate-900 hover:bg-slate-100'"
          >
            <span class="flex items-center gap-1.5">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
              Profile
            </span>
          </NuxtLink>

          <div class="h-5 w-px bg-slate-200 mx-2"></div>

          <a 
            href="mailto:timerinserver@gmail.com" 
            class="inline-flex items-center gap-1.5 text-xs font-semibold px-3 py-1.5 rounded-full bg-slate-900 text-white hover:bg-indigo-600 transition-colors shadow-xs"
          >
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            Contact
          </a>
        </nav>

        <!-- Mobile Menu Button -->
        <div class="flex md:hidden">
          <button 
            @click="isMobileMenuOpen = !isMobileMenuOpen"
            type="button" 
            class="p-2 rounded-lg text-slate-600 hover:text-slate-900 hover:bg-slate-100 focus:outline-none focus:ring-2 focus:ring-indigo-500"
            aria-label="Toggle navigation menu"
          >
            <svg v-if="!isMobileMenuOpen" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation Drawer -->
      <div v-show="isMobileMenuOpen" class="md:hidden py-3 border-t border-slate-100 space-y-1">
        <NuxtLink 
          to="/" 
          @click="isMobileMenuOpen = false"
          class="flex items-center gap-2 px-3 py-2.5 rounded-lg text-base font-medium transition-colors"
          :class="route.path === '/' ? 'text-indigo-600 bg-indigo-50 font-semibold' : 'text-slate-700 hover:bg-slate-100'"
        >
          <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
          </svg>
          Home
        </NuxtLink>

        <NuxtLink 
          to="/profile" 
          @click="isMobileMenuOpen = false"
          class="flex items-center gap-2 px-3 py-2.5 rounded-lg text-base font-medium transition-colors"
          :class="route.path === '/profile' ? 'text-indigo-600 bg-indigo-50 font-semibold' : 'text-slate-700 hover:bg-slate-100'"
        >
          <svg class="w-5 h-5 text-indigo-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
          </svg>
          Profile
        </NuxtLink>

        <div class="pt-2">
          <a 
            href="mailto:timerinserver@gmail.com" 
            class="flex items-center justify-center gap-2 w-full py-2.5 rounded-lg bg-indigo-600 text-white font-medium text-sm hover:bg-indigo-700 transition-colors shadow-xs"
          >
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
            Contact via Email
          </a>
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
</script>
