<script setup lang="ts">
import type {Form} from "../App.vue";

const formData = defineModel<Form>({required: true})
</script>

<template>
  <input type="text" v-model="formData.input"/>
  <input type="text" v-model="formData.input2"/>
  <input type="text" v-model="formData.input3"/>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
