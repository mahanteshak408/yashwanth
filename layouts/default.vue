<template>
  <v-app>
    <!-- App Bar -->
    <v-app-bar color="primary" prominent>
      <v-img src="/title.jpeg" cover class="v-app-bar__image" />

      <v-spacer></v-spacer>

      <!-- Search and Filter Buttons for larger screens -->
      <template v-if="$vuetify.display.mdAndUp">
        <v-btn icon="mdi-magnify" variant="text" />
        <v-btn icon="mdi-filter" variant="text" />
      </template>
    </v-app-bar>

    <!-- Main content section -->
    <v-main>
      <slot />
    </v-main>

    <!-- Footer -->
    <AppFooter />
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
      items: [
        { title: "Foo", value: "foo" },
        { title: "Bar", value: "bar" },
        { title: "Fizz", value: "fizz" },
        { title: "Buzz", value: "buzz" },
      ],
    };
  },

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style scoped>
.v-app-bar__image {
  max-width: 100%;
  height: auto;
}
</style>
