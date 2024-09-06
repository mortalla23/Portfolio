

<template>
    <footer>
      <p>&copy; 2024 Talla</p>
      <div class="social-media">
        <a href="#"><i class="fab fa-facebook-f"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-linkedin-in"></i></a>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'AppFooter'
  }
  </script>
  
  <style scoped>
  footer {
    text-align: center;
    padding: 20px;
    background-color: #fff;
  }
  .social-media a {
    margin: 0 10px;
    font-size: 20px;
    color: #000;
  }
  </style>
  