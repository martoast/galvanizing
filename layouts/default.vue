<template>
  <v-app dark>

    <AppBar />
    <Jumbotron />
    <v-content>

      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <Footer />
  </v-app>
</template>

<script>
import Jumbotron from "~/components/Jumbotron.vue";
import AppBar from "~/components/AppBar.vue";
import Footer from "~/components/Footer.vue";
export default {
  components: {
    Jumbotron,
    AppBar,
    Footer
  },
  data() {
    return {
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ]
    };
  }
};
</script>
