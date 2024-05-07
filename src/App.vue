<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>


<template>
  <div>
    <a href="" target="_blank">
      <img src="./assets/logovespa.png" class="logo" alt="Vite logo" />
    </a>
    <a href="" target="_blank">
      <img src="./assets/download.png" class="logo vue" alt="Vue logo" />
    </a>

    <!-- Element input teks -->
    <input type="text" v-model="inputText" @input="handleChange">

    <!-- Elemen yang menggunakan class bindings dan style bindings -->
    <div :class="{ 'red-text': isRed }" :style="{ fontSize: fontSize + 'px' }">
      {{ message }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'vespa sahabat kita !!',
      isRed: false,
      fontSize: 16,
      inputText: ''
    };
  },
  methods: {
    handleChange(event) {
      this.message = event.target.value;
    }
  }
}
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.red-text {
  color: red;
}
</style>

