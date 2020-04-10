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
        title: "Hot drip galvanizing",
        text:
          "Every achievement begins with a vision. It is built on a foundation of creative concepts and dreams to become something bigger and better. At AlphaConstruction we build with those who follow a vision, not a path.",
        src:
          "https://az276020.vo.msecnd.net/valmontproduction/webforge-css/galvanising-plant.jpg?sfvrsn=2151fb93_2"
      },
      {
        title: "Relentless pursuit of your vision",
        text:
          "Our commitment to excellence and continous improvement, to building lasting relationships with our clients, and to the team members who create your vision, are the guiding principles that assure successful outcomes on every project we build.",
        src:
          "https://rrgi.ca/wp-content/gallery/galvanizing-portfolio/IMG_2512-1.jpg"
      },
      {
        title: "Your vision - Our mission",
        text:
          "Our commitment to excellence and continous improvement, to building lasting relationships with our clients, and to the team members who create your vision, are the guiding principles that assure successful outcomes on every project we build.",
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
