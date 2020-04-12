<template>
  <v-img
    v-if="namespace"
    :src="this.src"
    aspect-ratio="4.0"
    gradient="to top, rgba(160, 90, 70, .35), rgba(30, 40, 30, 0.6)"
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
          <!-- <div class="hidden-md-and-up">
            <BigLogo />
          </div> -->

          <h1
            class="mb-4"
            :class="$vuetify.breakpoint.mdAndUp ? 'display-2' : 'display-1'"
          >
            North American Galvanizing Industries LLC

          </h1>

          <p class="title font-weight-light">
            Providing superior quality and Services
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
import BigLogo from "~/components/BigLogo.vue";
export default {
  data: () => ({
    src: require("@/assets/head-northamericangalvanizingindustries.png")
  }),
  components: { BigLogo },

  computed: {
    namespace() {
      return this.$route.name;
    }
  }
};
</script>
