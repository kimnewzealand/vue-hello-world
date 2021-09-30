<template>
<section class="showcase">
        <div class="container">
            <div class="grid">
              <div class="grid-item-1">
                <div class="showcase-text">
                    <h1>  
                      <label  :for="id" class="font-bold block">
                            Welcome to your translator using Vue.js
                      </label>
                    </h1>
                </div>
                <div>
                  <input
                  :id="id"
                  :type="type"
                  :value="input_text"
                  @input="updateInput"
                  class="border w-full p-1"
                  />
                </div>
                <div class="input-text">    
                  <label for="translate-form">You have entered {{input_text}}</label>
                </div>
                 </div>
                <div class="grid-item-2">
                  <div class="image">
                    <img src="../assets/talk2.jpeg" alt="">
                  </div>
                </div>
             
           </div>
        </div>
</section>   
</template>
<script>
    export default {
  name: "BaseInput",
  props: {
    id: {
      type: String,
      default: "",
    },
    input_text: {
      type: [String, Number],
      default: "nothing yet",
    },
    type: {
      type: String,
      default: "",
    }
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    }
  }
};
</script>