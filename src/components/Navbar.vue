<template>
  <nav class="navbar">
    <ul class="nav-links">
      <li><router-link to="/" class="nav-link">Home</router-link></li>
      <li><router-link to="/products" class="nav-link">Products</router-link></li>
      <li><router-link to="/cart" class="nav-link">Cart</router-link></li>
      <!-- Add more links as needed -->
    </ul>
  </nav>
</template>

<script setup>
// Optionally, import any other dependencies you may need
</script>

<style scoped>
.navbar {
  background-color: #333;
  padding: 10px;
}

.nav-links {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-evenly; /* Add this line */
}

.navbar li {
  display: inline;
}

.navbar li .nav-link {
  color: red;
  text-decoration: none;
}

.navbar li .nav-link:hover {
  color: white;
  text-decoration: underline;
}
</style>
