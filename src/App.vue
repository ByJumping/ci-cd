<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import {reactive} from "vue";

export interface Form {
  input: string;
  input2: string;
  input3: number;
}

const formData: Form = reactive({
  input: '',
  input2: '',
  input3: ''
})
</script>

<template>
  <div>
    <div>
      <p>Первый инпут:</p>
      <p>{{ formData.input }}</p>
    </div>
    <div>
      <p>Второй инпут:</p>
      <p>{{ formData.input2 }}</p>
    </div>
    <div>
      <p>Третий инпут:</p>
      <p>{{ formData.input3 }}</p>
    </div>



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
