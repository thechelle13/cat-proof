<template>
  <nav class="navbar">
    <ul>
      <li><router-link to="/" class="nav-link">Home</router-link></li>
      <li><router-link to="/products" class="nav-link">Products</router-link></li>
      <li><router-link to="/products" class="nav-link">Cart</router-link></li>
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

.navbar ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.navbar li {
  display: inline;
  margin-right: 10px;
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
