<template>
  <input type="text" :value="modelValue" @input="updateValue">
</template>

<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
  name: "MyInput",
  props: {
    modelValue: String
  },
  setup(props, ctx) {
    const updateValue = (e: KeyboardEvent) => {
      const targetValue = (e.target as HTMLInputElement).value
      ctx.emit('update:modelValue', targetValue)
    }
    return {
      updateValue
    }
  }
})
</script>

<style scoped>

</style>
