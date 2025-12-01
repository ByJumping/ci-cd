<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import {reactive} from "vue";

export interface Form {
  input: string;
  input2: string;
  input3: string;
}

const formData: Form = reactive({
  input: '',
  input2: '',
  input3: ''
})
</script>

<template>
  <div>
    <p>{{ formData.input }}</p>
    <p>{{ formData.input2 }}</p>
    <p>{{ formData.input3 }}</p>
  </div>
  <HelloWorld v-model="formData"/>
</template>

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
</style>
