<template>
  <v-img
    v-if="namespace"
    src="https://galco.ie/wp-content/uploads/2016/08/Hot-dip-galvanizing-in-action.jpg"
    aspect-ratio="4.0"
    gradient="to top, rgba(160, 90, 70, .85), rgba(30, 40, 30, .85)"
    height="100vh"
  >
    <v-container fill-height>
      <v-row
        align="center"
        justify="center"
        class="pt-5 px-3"
      >
        <v-sheet
          color="transparent"
          dark
          max-width="500"
        >
          <h1
            class="mb-4"
            :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'"
          >
            North American Galvaniznig Industries
          </h1>

          <p class="title font-weight-light">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          </p>

          <div class="py-4" />

          <v-row
            class="ma-0"
            justify="center"
            justify-md="start"
          >
            <v-btn
              class="mr-md-3 my-2"
              color="white"
              href="#pricing"
              large
              min-width="175"
              outlined
              rounded
              @click.prevent="$vuetify.goTo('#pricing')"
            >
              Learn More
            </v-btn>

            <v-btn
              class="text--primary my-2"
              color="white"
              href="#try-it"
              large
              min-width="175"
              rounded
              @click.prevent="$vuetify.goTo('#try-it')"
            >
              Contact us
            </v-btn>
          </v-row>
        </v-sheet>
      </v-row>
    </v-container>
  </v-img>
</template>

<script>
export default {
  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
