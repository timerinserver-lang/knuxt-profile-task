<template>
  <Teleport to="body">
    <Transition
      enter-active-class="transition duration-200 ease-out"
      enter-from-class="opacity-0 scale-95"
      enter-to-class="opacity-100 scale-100"
      leave-active-class="transition duration-150 ease-in"
      leave-from-class="opacity-100 scale-100"
      leave-to-class="opacity-0 scale-95"
    >
      <div 
        v-if="isOpen" 
        class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md"
        @click.self="closeModal"
        @keydown.esc="closeModal"
      >
        <!-- Modal Container -->
        <div 
          class="relative w-full max-w-lg bg-[#15222e] border-2 border-[#ff4655] shadow-[0_0_50px_rgba(255,70,85,0.35)] p-6 sm:p-8 val-cut-corner overflow-hidden"
        >
          <!-- Tactical background watermark & grid -->
          <div class="absolute -right-12 -bottom-12 text-[#ff4655]/5 text-9xl font-black select-none pointer-events-none">
            V
          </div>
          <div class="absolute top-0 right-0 w-24 h-24 bg-gradient-to-bl from-[#ff4655]/20 to-transparent pointer-events-none"></div>

          <!-- Top Protocol Header -->
          <div class="flex items-start justify-between pb-4 border-b border-[#2c3e50] mb-6">
            <div>
              <div class="inline-flex items-center gap-2 text-[10px] font-mono tracking-widest text-[#ff4655] uppercase">
                <span class="w-2 h-2 rounded-full bg-[#ff4655] animate-ping"></span>
                <span>SECURE TRANSMISSION // DIRECT COMMS</span>
              </div>
              <h3 class="text-2xl font-black tracking-wider text-white uppercase mt-1">
                Initiate Contact
              </h3>
              <p class="text-xs text-[#8b97a5] font-mono mt-0.5">
                AGENT: JOBERT JAN // STATUS: READY FOR DISPATCH
              </p>
            </div>

            <!-- Close Button -->
            <button 
              @click="closeModal"
              class="w-8 h-8 flex items-center justify-center bg-[#1f2d3d] hover:bg-[#ff4655] text-[#8b97a5] hover:text-white transition-colors border border-[#2c3e50] hover:border-[#ff4655]"
              title="Close transmission"
            >
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>

          <!-- Contact Channels List -->
          <div class="space-y-4">
            
            <!-- 1. PHONE NUMBER -->
            <div class="p-4 bg-[#0f1923] border border-[#2c3e50] hover:border-[#ff4655]/60 transition-colors group">
              <div class="flex items-center justify-between text-xs text-[#8b97a5] font-mono mb-1">
                <span class="flex items-center gap-1.5 text-[#ff4655]">
                  <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                  COMMS PROTOCOL 01: MOBILE / HOTLINE
                </span>
                <span class="text-[10px] text-emerald-400 font-mono">● LIVE</span>
              </div>

              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mt-2">
                <span class="text-lg font-bold tracking-wider text-white font-mono">
                  09383808212
                </span>
                <div class="flex items-center gap-2">
                  <button 
                    @click="copyText('09383808212', 'phone')"
                    class="px-3 py-1.5 bg-[#1f2d3d] hover:bg-[#ff4655] text-xs font-mono font-semibold text-white transition-colors border border-[#2c3e50]"
                  >
                    {{ copiedField === 'phone' ? '✓ COPIED' : 'COPY' }}
                  </button>
                  <a 
                    href="tel:09383808212"
                    class="px-3 py-1.5 bg-[#ff4655] hover:bg-[#e03746] text-xs font-mono font-bold text-white transition-colors flex items-center gap-1"
                  >
                    <span>DIAL</span>
                    <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                    </svg>
                  </a>
                </div>
              </div>
            </div>

            <!-- 2. EMAIL ADDRESS -->
            <div class="p-4 bg-[#0f1923] border border-[#2c3e50] hover:border-[#ff4655]/60 transition-colors group">
              <div class="flex items-center justify-between text-xs text-[#8b97a5] font-mono mb-1">
                <span class="flex items-center gap-1.5 text-[#ff4655]">
                  <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                  COMMS PROTOCOL 02: ENCRYPTED EMAIL
                </span>
                <span class="text-[10px] text-emerald-400 font-mono">● READY</span>
              </div>

              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mt-2">
                <span class="text-sm sm:text-base font-bold tracking-wide text-white font-mono break-all">
                  timerinserver@gmail.com
                </span>
                <div class="flex items-center gap-2 shrink-0">
                  <button 
                    @click="copyText('timerinserver@gmail.com', 'email')"
                    class="px-3 py-1.5 bg-[#1f2d3d] hover:bg-[#ff4655] text-xs font-mono font-semibold text-white transition-colors border border-[#2c3e50]"
                  >
                    {{ copiedField === 'email' ? '✓ COPIED' : 'COPY' }}
                  </button>
                  <a 
                    href="mailto:timerinserver@gmail.com"
                    class="px-3 py-1.5 bg-[#ff4655] hover:bg-[#e03746] text-xs font-mono font-bold text-white transition-colors flex items-center gap-1"
                  >
                    <span>COMPOSE</span>
                    <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3" />
                    </svg>
                  </a>
                </div>
              </div>
            </div>

            <!-- 3. GITHUB REPOSITORY / PROFILE -->
            <div class="p-4 bg-[#0f1923] border border-[#2c3e50] hover:border-[#ff4655]/60 transition-colors group">
              <div class="flex items-center justify-between text-xs text-[#8b97a5] font-mono mb-1">
                <span class="flex items-center gap-1.5 text-[#ff4655]">
                  <svg class="w-3.5 h-3.5 fill-current" viewBox="0 0 24 24">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.53 1.032 1.53 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" />
                  </svg>
                  COMMS PROTOCOL 03: GITHUB INTEL
                </span>
                <span class="text-[10px] text-cyan-400 font-mono">● PUBLIC REPO</span>
              </div>

              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 mt-2">
                <span class="text-sm font-bold tracking-wide text-white font-mono break-all">
                  github.com/timerinserver-lang
                </span>
                <a 
                  href="https://github.com/timerinserver-lang" 
                  target="_blank" 
                  rel="noopener noreferrer"
                  class="px-4 py-1.5 bg-gradient-to-r from-[#ff4655] to-[#ff2a3b] hover:from-[#e03746] hover:to-[#c71e2e] text-xs font-mono font-bold text-white transition-all shadow-[0_0_15px_rgba(255,70,85,0.4)] flex items-center justify-center gap-1.5 shrink-0"
                >
                  <span>ACCESS GITHUB</span>
                  <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                  </svg>
                </a>
              </div>
            </div>

          </div>

          <!-- Bottom Status Bar -->
          <div class="mt-6 pt-4 border-t border-[#2c3e50] flex flex-col sm:flex-row items-center justify-between gap-2 text-[11px] font-mono text-[#8b97a5]">
            <span class="flex items-center gap-1.5">
              <span class="w-1.5 h-1.5 bg-[#ff4655]"></span>
              LOC: PHILIPPINES // APAC SERVER
            </span>
            <button 
              @click="closeModal"
              class="text-xs text-[#8b97a5] hover:text-[#ff4655] transition-colors underline"
            >
              [ CLOSE TRANSMISSION ]
            </button>
          </div>
        </div>
      </div>
    </Transition>
  </Teleport>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = useState('contactModal', () => false)
const copiedField = ref(null)

const closeModal = () => {
  isOpen.value = false
}

const copyText = async (text, fieldName) => {
  try {
    await navigator.clipboard.writeText(text)
    copiedField.value = fieldName
    setTimeout(() => {
      copiedField.value = null
    }, 2000)
  } catch (err) {
    // Fallback if clipboard API not permitted
    const textArea = document.createElement("textarea")
    textArea.value = text
    document.body.appendChild(textArea)
    textArea.select()
    document.execCommand("copy")
    document.body.removeChild(textArea)
    copiedField.value = fieldName
    setTimeout(() => {
      copiedField.value = null
    }, 2000)
  }
}
</script>
