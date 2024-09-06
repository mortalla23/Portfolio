<template>
  <header>
    <div class="logo">PORTFOLIO</div>
    <nav class="nav">
      <ul>
        <li><router-link to="/">Accueil</router-link></li>
        <li><router-link to="/about">A propos</router-link></li>
        <li><router-link to="/services">Services</router-link></li>
        <li><router-link to="/portfolio">Liste des projets</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.nav {
  flex-grow: 1;
  text-align: center;
}

.nav ul {
  list-style: none;
  display: inline-flex;
  gap: 20px;
  padding: 0;
  margin: 0;
}

.nav a {
  text-decoration: none;
  color: #333;
  font-size: 16px;
}

.cta-button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #ff5a5f;
  color: #fff;
  border: none;
  cursor: pointer;
}
</style>
