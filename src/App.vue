<script>
var vm = new Vue({
  el: '#app',
  data: {
    txt: '', // Mensaje que se mostrará al buscar
    inputText: '' // Texto que el usuario escribe
  },
  methods: {
    search: function () {
      this.txt = this.inputText; 
    }
  }
});
</script>

<template>
   <input 
        v-model="inputText" 
        @keyup.enter="search" 
        placeholder="Ingresa el Dato a Buscar" 
      />
      <!-- Botón de buscar -->
      <button @click="search">Buscar</button>
      <h1>{{ txt }}</h1>
</template>
