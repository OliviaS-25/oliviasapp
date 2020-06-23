<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/email.png')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Let's Get In Touch!
        </h1>

        <p class="subheading font-weight-regular">
          If you want to discuss projects, jobs, or just want to get to know me
          a little more,
          <br />you can reach me by connecting on linkedin or by email.
        </p>
      </v-col>

      <v-col class="mb-5" cols="12">
        <h2 class="headline font-weight-bold mb-3">
          Click Here!
        </h2>

        <v-row justify="center">
          <a
            v-for="(next, i) in clickhere"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    clickhere: [
      {
        text: 'LinkedIn',
        href: 'https://www.linkedin.com/in/olivia-sackitey-563039167/',
      },
      {
        text: 'Email',
        href: 'mailto:oliviadsackitey@gmail.com',
      },
    ],
  }),
}
</script>
