<template>
  <div>
    <section class="grey lighten-3">
      <v-container>

        <SectionHeader
          sub-header="Why Our Galvanizing Services?"
          header="North American Galvanizing Industries"
        />
        <v-row
          align="center"
          justify="space-around"
        >
          <v-col
            cols="12"
            md="5"
            offset-xl="1"
          >

            <div class="ma-12">
              <v-row justify="center">
                <h2 class="mb-4 headline">
                  Quality is our priority
                  <br />
                </h2>

                <p class="subtitle-1">
                  In North American Galvanizing Industries LLC our procedures are tracked and stringently managed at every stage of the operation. Every day we continue to invest and develop new technology and procedures to excel and enhance our offering to steel building markets and fabricators in the industry.
                </p>

                <v-btn
                  outlined
                  color="#BF9B2A"
                  class="px-5"
                  x-large
                  to="/contact"
                >
                  Contact us
                </v-btn>

              </v-row>

            </div>

          </v-col>

          <v-col
            cols="12"
            md="5"
          >

            <div align="center">
              <v-container>

                <iframe
                  style="top:55px; left:0; bottom:0; right:0; height: 400px; border:none; margin:0; padding:0; z-index:999999;"
                  src="https://player.vimeo.com/video/404896466"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                  width="100%"
                ></iframe>

              </v-container>

            </div>

          </v-col>
        </v-row>
      </v-container>
    </section>

  </div>
</template>
<script>
import SectionHeader from "~/components/SectionHeader.vue";
export default {
  components: { SectionHeader },
  data() {
    return {};
  }
};
</script>
