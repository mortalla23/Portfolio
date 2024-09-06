<template>
    <div class="contact-form">
      <h2>Consultation Gratuite</h2>
      <form @submit.prevent="sendEmail">
        <div>
          <label for="name">Nom:</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div>
          <label for="message">Message:</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <button type="submit">Envoyer</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ContactForm',
    data() {
      return {
        name: '',
        email: '',
        message: ''
      };
    },
    methods: {
      sendEmail() {
        const subject = encodeURIComponent('Consultation Gratuite');
        const body = encodeURIComponent(`Nom: ${this.name}\nEmail: ${this.email}\n\nMessage:\n${this.message}`);
        window.location.href = `mailto:ton-email@example.com?subject=${subject}&body=${body}`;
      }
    }
  };
  </script>
  
  <style scoped>
  .contact-form {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
  .contact-form h2 {
    margin-bottom: 20px;
  }
  .contact-form div {
    margin-bottom: 10px;
  }
  .contact-form label {
    display: block;
    margin-bottom: 5px;
  }
  .contact-form input, .contact-form textarea {
    width: 100%;
    padding: 8px;
    box-sizing: border-box;
  }
  .contact-form button {
    padding: 10px 20px;
    background-color: #ff5a5f;
    color: #fff;
    border: none;
    cursor: pointer;
  }
  </style>
  