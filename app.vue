<script setup>
import { ref } from 'vue'

const msg = ref('Hello World!')
const imageUrl = ref('https://en.wikipedia.org/wiki/JPEG#/media/File:Felis_silvestris_silvestris_small_gradual_decrease_of_quality.png');

</script>

<template>
  <header class="gradient-box">
    <span class="title">SISTECH</span>
  </header>
  <div class="body">
    <div class="square">
      <svg xmlns="http://www.w3.org/2000/svg" height="5em" viewBox="0 0 512 512" class="icon"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/></svg>
      <h2 class="cancel">Désinscription</h2>
      <div class="confirmation">
        <span class="text">Souhaitez-vous vraiment ne plus recevoir<br>d'informations de la part de Sistech ?</span>
        <button class="button">oui, me désinscrire</button>
      </div>
    </div>
  </div>
  <footer class="footer">
    <span class="sistech">© Sistech, 2023</span>
  </footer>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Raleway:500');
.gradient-box {
  display: flex;
  justify-content: flex-end;
  align-items:end;
  background: linear-gradient(to right, #833ab4, #fd1d1d, #fcb045);
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
  background-color: #d1d0d1;
}

.square {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1em;
  background-color: #d9d8d9;
  min-width: 25em;
  min-height: 10em;
}

.icon {
  fill: #fe4799;
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
  background-color: #eaeaea;
  padding: 1em 2em;
  text-align: center;
  margin-bottom: 1em;
}

.text {
  color:#646464;
  font-weight: 300;
  margin-bottom: 1em;
}

.button {
  padding: 0.8em 2em;
  border-radius: 1.4em;
  margin-top: 1em;
  background: linear-gradient(to right, #a2ccb6, #a2ccb6,#fceeb5);
  border: none;
  color: white;
  margin-bottom: 1em;
}

.button:hover {
  cursor: pointer;
  background: linear-gradient(to right, #fceeb5, #ee786e, #ee786e);
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
  color: #e2e1e2;
}
</style>