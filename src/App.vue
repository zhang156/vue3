<template>
  <Keyboard msg="111"></Keyboard>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Keyboard from './components/Keyboard.vue'
import HelloWrod from './components/HelloWorld.vue'

export default defineComponent({
  name: 'App',
  components: {
    HelloWrod,
    Keyboard
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

html, body, #app {
  height: 100%;
  margin: 0;
  padding: 0;
}
</style>
