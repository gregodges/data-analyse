<template>
  <div class="hello-world">
    <h2>Bonjour, {{ person }} 👋</h2>
    <p v-if="showMessage">
      Ceci est ton premier composant Nuxt 3 avec TypeScript !
    </p>
    <button @click="toggle">
      {{ showMessage ? 'Masquer' : 'Afficher' }} le message
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
defineProps<{
  person: object
}>()

const showMessage = ref(true)

function toggle() {
  showMessage.value = !showMessage.value
}
</script>

<style scoped>
.hello-world {
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: 8px;
  background: #f9f9f9;
}

.hello-world h2 {
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  font-weight: bold;
}

.hello-world button {
  margin-top: 1rem;
  padding: 0.5rem 1rem;
  background-color: #2f80ed;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.hello-world button:hover {
  background-color: #1366d6;
}
</style>
