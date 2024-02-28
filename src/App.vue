<template>
  <header>
    <img alt="FIFA logo" class="logo" src="./assets/fifa.png" height="168" width="512" />

    <div class="wrapper">
      <h2 class="prompt">Please Enter Your Email Below</h2>
      <input type="email" class="email-input" placeholder="Email" v-model="email" />
      <button @click="submitEmail" class="submit-button">Submit</button>
    </div>
  </header>

  <main>
    <!-- Use the icons imported from TheWelcome.vue -->
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Documentation</template>

      Here is my official
      <a href="https://github.com/LukasBel/FIFA_Scraper.git" target="_blank" rel="noopener" class="blue-link">documentation</a>
      if anyone desires to make any modifications.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>Contact Me</template>

      If you have any questions or suggestions please feel free to contact me through
      <a href="https://www.linkedin.com/in/lukas-belashov-0b838b177/" target="_blank" rel="noopener" class="blue-link">LinkedIn</a>, or
      <a href="https://github.com/LukasBel" target="_blank" rel="noopener" class="blue-link">Github</a>
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <SupportIcon />
      </template>
      <template #heading>Purpose</template>

      As a soccer enthusiast from Pennsylvania, hearing that the World Cup Final will take place
      in New Jersey I decided to build a web scraper that would notify me daily about ticket information.
      Though the FIFA website has an official newsletter, I wanted to create my own application with less traffic
      and more reliability.
    </WelcomeItem>
  </main>
</template>

<script setup>
import { ref } from "vue";
import axios from "axios";
import WelcomeItem from "@/components/WelcomeItem.vue";
import DocumentationIcon from "@/components/icons/IconDocumentation.vue";
import CommunityIcon from "@/components/icons/IconCommunity.vue";
import SupportIcon from "@/components/icons/IconSupport.vue";


const submitEmail = async () => {
  try {
    await axios.post("http://localhost:8080/FIFA/create", { email: email.value });
    console.log("Email submitted successfully!");
  } catch (error) {
    console.error("Failed to submit email:", error);
  }
};

const email = ref("");
</script>

<style scoped>
header {
  line-height: 1.5;
  position: relative;
}

.logo {
  display: block;
  position: absolute;
  top: 0;
  left: 0;
}

.wrapper {
  margin-top: 200px; /* Adjust as needed */
  text-align: center;
}

.prompt {
  font-size: 1.5rem;
  margin-bottom: 20px;
}

.email-input {
  padding: 10px;
  font-size: 1rem;
  margin-bottom: 10px;
}

.submit-button {
  padding: 10px 20px;
  font-size: 1rem;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.submit-button:hover {
  background-color: #0056b3;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

.blue-link {
  color: rgba(30, 138, 222, 0.87);
}
</style>
