<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br>
    <my-input v-model="vModelInputData"></my-input>
    <my-checkbox v-model="vModelCheckboxData"></my-checkbox>
    <h1>my input: {{vModelInputData}}</h1>
    <h1>my checkbox: {{vModelCheckboxData}}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import MyInput from "@/components/MyInput.vue";
import MyCheckbox from "@/components/MyCheckbox.vue";

export default defineComponent({
  name: 'App',
  components: {
    MyCheckbox,
    MyInput
  },
  setup(){
    const vModelInputData = ref('')
    const vModelCheckboxData = ref(false)
    return {
      vModelInputData,
      vModelCheckboxData
    }
  }
});
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
</style>
