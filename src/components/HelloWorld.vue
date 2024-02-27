<script setup>
import {ref} from "vue";

defineProps({
  msg: {
    type: String,
    required: true
  }
})

const submitEmail = () => {
  console.log(email.value)
}

const email = ref('')

</script>

<template>
    <h1 class="green">{{ msg }}</h1>

    <h3>Enter your email below</h3>

  <input type="email" placeholder="Email" v-model="email" />
  <button @click="submitEmail">Submit</button>


  <p>By submitting your email, you agree to our <a href="#">Privacy Policy</a> and <a href="#">Terms of Service</a>.</p>

</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
