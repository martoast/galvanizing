<template>
  <div id="home">

    <v-container
      id="goals"
      tag="section"
    >
      <SectionHeader
        header="North American Galvanizing Industries"
        sub-header="Our Services"
      />

      <v-row>
        <v-col
          v-for="(feature, i) in features"
          :key="i"
          class="d-flex"
          cols="12"
          sm="6"
          md="4"
        >
          <v-card
            outlined
            max-width="100%"
          >
            <v-img
              :src="feature.src"
              height="200"
            />
            <v-card-title
              class="align-center"
              style="min-height: 88px;"
              v-text="feature.title"
            />
            <v-card-text
              class="pb-5 pt-3"
              v-text="feature.text"
            />

          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <section>
      <VideoSheet />
    </section>

    <v-container
      id="testimonials"
      class="py-5"
      tag="section"
    >
      <SectionHeader
        header="North American Galvanizing"
        sub-header="Listen to what our clients had to say!"
      />

      <v-row>
        <v-col
          v-for="(testimonial, i) in testimonials"
          :key="i"
          cols="12"
          md="6"
        >
          <testimonial :testimonial="testimonial" />
        </v-col>
      </v-row>
    </v-container>

    <v-container
      id="highlighted-testimonial"
      class="pt-5 px-0 mb-n3"
      fluid
      tag="section"
    >
      <v-parallax
        contain
        src="https://galco.ie/wp-content/uploads/2016/08/Hot-dip-galvanizing-in-action.jpg"
      >
        >
        <v-overlay
          absolute
          class="px-3"
          opacity=".8"
        >
          <testimonial
            dark
            :testimonial="highlightedTestimonial"
          />
        </v-overlay>
      </v-parallax>
    </v-container>

    <Contact />

  </div>
</template>

<script>
export default {
  metaInfo: {
    title: "Home",
    meta: [
      {
        name: "description",
        content: "Customized vue-cli templates for Vue and Vuetify"
      }
    ]
  },

  components: {
    Heading: () => import("@/components/Heading"),
    Testimonial: () => import("@/components/Testimonial"),
    NetlifyForm: () => import("@/components/netlify-form"),
    SectionHeader: () => import("@/components/SectionHeader"),
    VideoSheet: () => import("@/components/VideoSheet"),
    Contact: () => import("@/components/Contact")
  },

  data: () => ({
    highlightedTestimonial: {
      blurb:
        "The complexities and challenges AlphaConstruction successfully overcame on our behalf includes substantial permit obstacles, coordination and selection support of all design and finish materials, and the diffculty of integrating existing and new structures.",
      person: "Joe Malonagi",
      title: "General Manager, Springfield Tower"
    },
    features: [
      {
        title: "Hot dip galvanizing",
        text:
          "Hot-dip galvanizing is the most effective form of galvanizing which involves the process of coating iron and steel with a molting layer of zinc which protects against corrosion.",
        src:
          "https://az276020.vo.msecnd.net/valmontproduction/webforge-css/galvanising-plant.jpg?sfvrsn=2151fb93_2"
      },
      {
        title: "Efficiency and Quality",
        text:
          "North American Galvanizing Industries LLC counts including both 30 feet and a 60 feet Kettles, allowing us to supply galvanizing solutions for your most demanding jobs.",
        src:
          "https://rrgi.ca/wp-content/gallery/galvanizing-portfolio/IMG_2512-1.jpg"
      },
      {
        title: "Where We Operate",
        text:
          "We are based off San Diego County and  Can offer solutions in Santa Clarita, Imperial Valley, Riverside, San Bernardino, Orange County, Los Angeles, Ventura and Santa Barbara Counties.",
        src:
          "https://web.distran.com/hs-fs/hub/48397/file-14362921-jpg/images/poles_in_kettle_1.jpg"
      }
    ],
    testimonials: [
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Nancy Swanson",
        title: "President, Springfield Country Club"
      },
      {
        blurb:
          "Leverage agile frameworks to provide a robust synopsis for high level over Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.",
        person: "Jason Schraiber",
        title: "Mayor, Boca Raton"
      }
    ]
  })
};
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>
