<template>
  <v-sheet
    :height="$vuetify.breakpoint.smAndUp ? '40vh' : '100vh'"
    color="primary"
    tile
  >
    <v-img
      src="https://web.distran.com/hs-fs/hub/48397/file-14362921-jpg/images/poles_in_kettle_1.jpg"
      gradient="to top, rgba(171,184,193,1), rgba(226,42,27,1)"
      height="100%"
    >

      <v-container
        fill-height
        white--text
      >
        <v-slide-x-transition appear>
          <v-col
            align="center"
            justify="center"
          >
            <h1
              :class="$vuetify.breakpoint.smAndUp ? 'display-3' : 'display-2'"
              class="mb-2"
              v-text="title"
            />
            <div
              class="title font-weight-light"
              v-text="subtitle"
            />
          </v-col>
        </v-slide-x-transition>
      </v-container>
    </v-img>
    <GetAQuote />
  </v-sheet>
</template>

<script>
import GetAQuote from "~/components/GetAQuote.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
export default {
  components: {
    GetAQuote,
    VuetifyLogo
  },
  data: () => ({
    titles: {
      home: {
        title: "Building a Culture of Excellence",
        subtitle: "Vestibulum volutpat pretium libero. Suspendisse eu ligula."
      },
      services: {
        title: "Next Generation Development Today",
        subtitle:
          "Phasellus gravida semper nisi. Fusce convallis metus id felis luctus adipiscing."
      },
      projects: {
        title: "Premium Quality and Branding",
        subtitle: "Vestibulum turpis sem, aliquet eget, lobortis pellentesque."
      },
      contact: {
        title: "Contact Alpha Construction",
        subtitle: "Aenean viverra rhoncus pede. Morbi mollis tellus ac sapien."
      }
    }
  }),

  computed: {
    namespace() {
      if (!this.$route || !this.$route.name) return "";
      return this.$route.name.toLowerCase();
    },

    subtitle() {
      return "Galvanizing industries";
    },
    title() {
      return "North American";
    }
  }
};
</script>
