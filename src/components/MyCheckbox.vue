<template>
  <input type="checkbox" :checked="modelValue" @change="updateValue">
</template>

<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
  name: "MyCheckbox",
  props: {
    modelValue: Boolean
  },
  setup(props, ctx) {
    const updateValue = (e: MouseEvent) => {
      const targetValue = (e.target as HTMLInputElement).checked
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
