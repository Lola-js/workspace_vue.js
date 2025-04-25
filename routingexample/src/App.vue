<template>
  <div id="app" class="font-sans text-gray-800">
    <nav class="p-6 bg-blue-800">
      <!-- Uso v-for para iterar las rutas -->
      <router-link
        v-for="route in routes"
        :key="route.name"
        :to="{ name: route.name }"
        class="text-white font-bold mr-4 hover:text-indigo-400 transition-colors duration-300"
      >
        {{ route.label }}
      </router-link>
    </nav>

    <router-view />
  </div>
</template>

<script>
// Importa las rutas
import { routes } from '@/data/routes.js'

export default {
  name: 'App',
  data() {
    return {
      routes
    }
  }
}
</script>

<style scoped>
</style>
