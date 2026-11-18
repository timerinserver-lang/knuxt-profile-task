<template>
  <div class="flex flex-col min-h-screen bg-[#0f1923] text-[#ece8e1] val-grid-bg relative">
    <Navbar />
    
    <main class="flex-grow relative z-10">
      <slot />
    </main>

    <Footer />

    <!-- Interactive Valorant Comms Modal -->
    <ContactModal />
  </div>
</template>

<script setup>
// Layout auto-mounts Navbar, Footer, and ContactModal
</script>
