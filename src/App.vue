<template>
  <div>
    <!-- Navbar Component -->
    <Navbar />

    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>

    <!-- About Section -->
    <section class="about">
      <h2>About</h2>
      <p>This app is about products that cat people can purchase products that are used for cat-proofing their home so that sharing their home with a feline can be more pleasant.</p>
    </section>

    <!-- Display Random Cat Photo -->
    <img id="cat" :src="catImage" alt="Random Cat Photo" />

    <!-- HelloWorld Component -->
    <HelloWorld msg="Vite + Vue" />
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue'

const catImage = ref('') // Reactive variable to hold the URL of the cat image

onMounted(async () => {
  try {
    const response = await fetch('http://shibe.online/api/cats?count=1&urls=true&httpsUrls=false')
    const data = await response.json()
    catImage.value = data[0]
  } catch (error) {
    console.error('Failed to fetch cat image:', error)
  }
})
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.about {
  margin-top: 20px;
}
.about h2 {
  font-size: 1.5em;
}
.about p {
  font-size: 1.2em;
}
</style>
