<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
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
</template>

<style scoped>
.blue-link {
  color: rgba(19,110,182,0.84);
}
</style>


