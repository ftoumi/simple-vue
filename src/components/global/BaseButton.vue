<template>
  <button 
    class="font-bold py-2 px-4 rounded text-white bg-blue-500 hover:bg-blue-700"
    :disabled="isDisabled"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "base-button",
  props: ['text', 'isDisabled']
}
</script>