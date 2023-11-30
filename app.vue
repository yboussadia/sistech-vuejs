<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const showModal = ref(false)
const isRegistred = ref(false)

const handleClick = () => {
  showModal.value = true
  isRegistred.value = true
}
</script>
<template>
  <header class="gradient-box">
   <a href="https://vuejsexamples.com">
    <span class="title">SISTECH</span>
    </a>
  </header>
  <div class="body">
  <div class="modal" v-if="showModal">
    <button class="close" @click="showModal = false">x</button>
    <svg xmlns="http://www.w3.org/2000/svg" height="5em" viewBox="0 0 512 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path fill="#06a72e" d="M336 16V80c0 8.8-7.2 16-16 16s-16-7.2-16-16V16c0-8.8 7.2-16 16-16s16 7.2 16 16zm-98.7 7.1l32 48c4.9 7.4 2.9 17.3-4.4 22.2s-17.3 2.9-22.2-4.4l-32-48c-4.9-7.4-2.9-17.3 4.4-22.2s17.3-2.9 22.2 4.4zM135 119c9.4-9.4 24.6-9.4 33.9 0L292.7 242.7c10.1 10.1 27.3 2.9 27.3-11.3V192c0-17.7 14.3-32 32-32s32 14.3 32 32V345.6c0 57.1-30 110-78.9 139.4c-64 38.4-145.8 28.3-198.5-24.4L7 361c-9.4-9.4-9.4-24.6 0-33.9s24.6-9.4 33.9 0l53 53c6.1 6.1 16 6.1 22.1 0s6.1-16 0-22.1L23 265c-9.4-9.4-9.4-24.6 0-33.9s24.6-9.4 33.9 0l93 93c6.1 6.1 16 6.1 22.1 0s6.1-16 0-22.1L55 185c-9.4-9.4-9.4-24.6 0-33.9s24.6-9.4 33.9 0l117 117c6.1 6.1 16 6.1 22.1 0s6.1-16 0-22.1l-93-93c-9.4-9.4-9.4-24.6 0-33.9zM433.1 484.9c-24.2 14.5-50.9 22.1-77.7 23.1c48.1-39.6 76.6-99 76.6-162.4l0-98.1c8.2-.1 16-6.4 16-16V192c0-17.7 14.3-32 32-32s32 14.3 32 32V345.6c0 57.1-30 110-78.9 139.4zM424.9 18.7c7.4 4.9 9.3 14.8 4.4 22.2l-32 48c-4.9 7.4-14.8 9.3-22.2 4.4s-9.3-14.8-4.4-22.2l32-48c4.9-7.4 14.8-9.3 22.2-4.4z"/></svg>
    <p class="cancel">Bravo {{name}}, vous êtes bien inscrit<br>à la newsletter Sistech !</p>
  </div>
    <div class="square">
      <svg v-if="!isRegistred" xmlns="http://www.w3.org/2000/svg" height="5em" viewBox="0 0 512 512" class="icon"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/></svg>
      <svg v-else xmlns="http://www.w3.org/2000/svg" height="5em" viewBox="0 0 448 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path fill="#0d5de7" d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"/></svg>
      <h2 v-if="!isRegistred" class="cancel">Inscription</h2>
      <h2 v-else class="cancel">Hello, {{name}}</h2>
      <div v-if="!isRegistred" class="confirmation">
        <span class="text">Souhaitez-vous recevoir des<br>informations de la part de Sistech ?</span>
        <input v-model="name" placeholder="prénom" />
        <br />
        <input v-model="email" placeholder="mon adresse e-mail " />
        <br />
       <button class="button"  @click="handleClick">oui, je m'inscris</button>
      </div>
      <div v-else class="confirmation">
        <div class="text">Suivez les dernières nouveautés<br>Sistech sur Linkdin</div>
        <a href="https://www.linkedin.com/groups/12920520/" >
          <button class="button-linkdin">Aller sur Linkdin</button>
        </a>
      </div>
    </div>
</div>
  <footer class="footer">
    <span class="sistech">© Sistech, 2023</span>
  </footer>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Raleway:500');
a {
  text-decoration: none;
  padding-bottom: 0.5em;
}
input::placeholder {
  color: gainsboro;
}
.modal {
  position: absolute;
  text-align: center;
  background-color: white;
  opacity: 0.95;
  height: 250px;
  width: 500px;
  margin-bottom: 10%;
  border-radius: 20px;
}
.close {
 display: flex;
  margin: 2em;
}
.gradient-box {
  display: flex;
  justify-content: flex-end;
  align-items:end;
  background: linear-gradient(to right, #833AB4, #FD1D1D, #FCB045);
  color: white;
  height: 8em;
  width: 100%;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
}
.title {
  text-align:right;
  font-weight: 800;
  font-size: 1.5em;
  padding-bottom: 0.5em;
  padding-right: 0.6em;
  color: black;
}
.body {
  min-height: 70vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0;
  background-color: #D1D0D1;
}
.square {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1em;
  background-color: #D9D8D9;
  min-width: 25em;
  min-height: 10em;
}
.icon {
  fill: #FE4799;
}
.cancel {
  margin-top: 1.2em;
  margin-bottom: 1.3em;
  font-weight: 400;
  color: #646464;
}
.confirmation {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #EAEAEA;
  padding: 1em 2em;
  text-align: center;
  margin-bottom: 1em;
}
.text {
  color:#646464;
  font-weight: 300;
  margin-bottom: 1em;
  text-align: center;
}
.button {
  padding: 0.8em 2em;
  border-radius: 1.4em;
  margin-top: 1em;
  background: linear-gradient(to right, #A2CCB6, #A2CCB6,#FCEEB5);
  border: none;
  color: white;
  margin-bottom: 1em;
}
.button:hover {
  cursor: pointer;
  background: linear-gradient(to right, #FCEEB5, #EE786E, #EE786E);
}
.footer {
  background-color: #767577;
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
  height: 3em;
  display: flex;
  flex-direction: column;
  justify-content:end;
}
.sistech {
  padding: 0.6em;
  color: #E2E1E2;
}

.button-linkdin {
  padding: 0.8em 2em;
  border-radius: 1.4em;
  margin-top: 1em;
  background: linear-gradient(to right, #A2CCB6, #A2CCB6,#FCEEB5);
  border: none;
  color: white;
  margin-bottom: 1em;
}

.button-linkdin:hover {
  cursor: pointer;
  background: linear-gradient(to right, #FCEEB5, #EE786E, #EE786E);
}
</style>