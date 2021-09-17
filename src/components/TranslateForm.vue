<template>
  <div>
    <input v-model="message" id="translate-form" placeholder="Enter text"/>
  </div>
  <label for="translate-form">You have entered {{input_text}}</label>
</template>

<script>
  export default {
     props: {
        input_text: { default:'nothing yet', type: String }
    }};
</script>