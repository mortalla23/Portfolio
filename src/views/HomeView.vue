<template>
  <div class="home">
    <div class="content">
      <div class="text-content">
        <p>BIENVENUE</p>
        <h1> Mor TALLA<br> Développeur Full-stack</h1>
        <p>Elève Ingénieur des services numériques à l'ESIGELEC.</p>
        <div class="buttons">
          <button class="learn-more">Pour en savoir plus</button>
          <button class="hire-me">Engagez-moi</button>
        </div>
      </div>
      <div class="image-content">
        <div class="image-background"></div>
        <img src="@/assets/Image/IMG_1.jpg" alt="Designer">
      </div>
    </div>
    <button class="cta-button" @click="showContactForm = true">Get Free Consultant</button>
    <div v-if="showContactForm" class="modal">
      <div class="modal-content">
        <span class="close" @click="showContactForm = false">&times;</span>
        <ContactForm />
      </div>
    </div>
  </div>
</template>

<script>
import ContactForm from '@/components/ContactForm.vue';

export default {
  name: 'HomeView',
  components: {
    ContactForm
  },
  data() {
    return {
      showContactForm: false
    };
  }
}
</script>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f7f8fc;
  padding: 20px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 0;
  width: 100%;
}

.text-content {
  max-width: 50%;
}

.text-content p {
  color: #ff5a5f;
  font-size: 18px;
  margin-bottom: 20px;
}

.text-content h1 {
  font-size: 48px;
  margin-bottom: 20px;
}

.text-content p {
  font-size: 18px;
  margin-bottom: 40px;
}

.buttons {
  display: flex;
  gap: 20px;
}

.buttons .learn-more, .buttons .hire-me {
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.buttons .learn-more {
  background-color: #ff5a5f;
  color: #fff;
}

.buttons .hire-me {
  background-color: #f0f0f0;
  color: #333;
}

.image-content {
  position: relative;
  max-width: 40%;
}

.image-content .image-background {
  position: absolute;
  right: -20px;
  top: -20px;
  width: 120%;
  height: 120%;
  background: radial-gradient(circle at center, #800080, #4b0082);
  border-radius: 20px;
  z-index: -1;
}

.image-content img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  position: relative;
  z-index: 1;
}

.cta-button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #ff5a5f;
  color: #fff;
  border: none;
  cursor: pointer;
  margin-top: 20px;
}

.modal {
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  width: 80%;
  max-width: 500px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
}
</style>
