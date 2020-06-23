<template>
      <div class="aboutme">
            <h1>About Me</h1>
            <welcome-page />
      </div>
</template>

<script>
import WelcomePage from '@/components/WelcomePage.vue'
export default {
      name: 'AboutMe',
      components: {
            WelcomePage,
      },
}
</script>
