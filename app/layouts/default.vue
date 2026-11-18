<template>
  <div class="flex flex-col min-h-screen bg-slate-50 text-slate-800">
    <Navbar />
    
    <main class="flex-grow">
      <slot />
    </main>

    <Footer />
  </div>
</template>

<script setup>
// Nuxt auto-imports components inside app/components/
</script>
