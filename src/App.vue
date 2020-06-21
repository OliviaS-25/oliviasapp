<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app>
      <v-list nav dense>
        <v-list-item-group active-class="primary--text">
          <v-list-item v-on:click="routeTo('/')">
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <v-list-item v-on:click="routeTo('/aboutme')">
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>About Me</v-list-item-title>
          </v-list-item>
          <v-list-item v-on:click="routeTo('/experience')">
            <v-list-item-icon>
              <v-icon>mdi-clipboard-text</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Experience</v-list-item-title>
          </v-list-item>
          <v-list-item v-on:click="routeTo('/interests')">
            <v-list-item-icon>
              <v-icon>mdi-image-filter-vintage</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Interests</v-list-item-title>
          </v-list-item>
          <v-list-item v-on:click="routeTo('/contactme')">
            <v-list-item-icon>
              <v-icon>mdi-email-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Contact Me</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
    </v-app-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  data: () => ({
    drawer: false,
  }),
  methods: {
    routeTo(newPath) {
      this.$router.push({ path: newPath })
    },
  },
}
</script>
