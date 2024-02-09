<script setup>
 import {ref} from 'vue'
 const message = ref('Mantra!')

 function reverseMessage() {
  message.value = message.value.split('').reverse().join('')
}

function notify() {
  alert('navigation has default behavior ')
}
 </script>




<template>
  <h1>{{ message }}</h1>

  <button @click="message += '!'"> Append "!"</button>
  
  <button @click="reverseMessage">Reverse Message</button>

  <a href="https://500apps.com/" @click="notify">
    A link navigating to specified webpage 
  </a>
</template>
<style>
button,a{
  display: block;
  margin: 1em;
}

</style>