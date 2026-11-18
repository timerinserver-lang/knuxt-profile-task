<template>
  <footer class="mt-auto bg-[#0a1017] border-t-2 border-[#2c3e50] relative overflow-hidden">
    <!-- Top red accent line -->
    <div class="h-0.5 w-full bg-gradient-to-r from-transparent via-[#ff4655]/60 to-transparent"></div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-center justify-between">
        
        <!-- Agent Identity & Brand -->
        <div class="md:col-span-5 space-y-2">
          <div class="flex items-center gap-2">
            <span class="w-2.5 h-2.5 bg-[#ff4655] rotate-45 inline-block"></span>
            <span class="text-xs font-mono font-bold tracking-widest text-[#ff4655] uppercase">
              // AGENT PROTOCOL: JOBERT JAN
            </span>
          </div>
          <p class="text-xs text-[#8b97a5] font-mono leading-relaxed max-w-sm">
            Deploying resilient, high-precision web experiences built with Nuxt 4, Vue 3, and Tailwind CSS.
          </p>
          <div class="text-[11px] font-mono text-[#8b97a5] flex flex-wrap gap-x-4 gap-y-1 pt-1">
            <span>HOTLINE: <a href="tel:09383808212" class="text-white hover:text-[#ff4655] underline">09383808212</a></span>
            <span>EMAIL: <a href="mailto:timerinserver@gmail.com" class="text-white hover:text-[#ff4655] underline">timerinserver@gmail.com</a></span>
          </div>
        </div>

        <!-- Direct Comms Quick Access -->
        <div class="md:col-span-4 flex flex-col sm:flex-row md:flex-col lg:flex-row items-start md:items-center gap-3">
          <button 
            @click="openContact"
            type="button"
            class="px-4 py-2 bg-[#15222e] hover:bg-[#ff4655] text-white border border-[#2c3e50] hover:border-[#ff4655] text-xs font-mono font-bold tracking-wider uppercase transition-all flex items-center gap-2 cursor-pointer shadow-xs"
          >
            <span class="w-1.5 h-1.5 bg-[#ff4655] group-hover:bg-white"></span>
            <span>OPEN COMMS MODAL</span>
          </button>

          <a 
            href="https://github.com/timerinserver-lang" 
            target="_blank" 
            rel="noopener noreferrer"
            class="px-4 py-2 bg-[#0f1923] hover:bg-[#1f2d3d] text-cyan-400 border border-cyan-500/40 hover:border-cyan-400 text-xs font-mono font-bold tracking-wider uppercase transition-all flex items-center gap-1.5"
          >
            <span>GITHUB</span>
            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
            </svg>
          </a>
        </div>

        <!-- Navigation Links & Copyright -->
        <div class="md:col-span-3 text-left md:text-right space-y-2">
          <div class="flex items-center md:justify-end gap-4 text-xs font-mono text-[#8b97a5]">
            <NuxtLink to="/" class="hover:text-[#ff4655] transition-colors">HOME</NuxtLink>
            <span>/</span>
            <NuxtLink to="/profile" class="hover:text-[#ff4655] transition-colors">DOSSIER</NuxtLink>
            <span>/</span>
            <button @click="openContact" class="hover:text-[#ff4655] transition-colors cursor-pointer">COMMS</button>
          </div>
          <p class="text-[10px] font-mono text-[#8b97a5]">
            // PROTOCOL VALORANT-STYLE // © {{ new Date().getFullYear() }} JOBERT JAN. ALL RIGHTS RESERVED.
          </p>
        </div>

      </div>
    </div>
  </footer>
</template>

<script setup>
const contactModal = useState('contactModal', () => false)
const openContact = () => {
  contactModal.value = true
}
</script>
