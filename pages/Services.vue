<template>
  <section
    id="services"
    class="py-5"
  >
    <SectionHeader
      header="North American Galvanizing Industries"
      sub-header="Explore our Services"
    />

    <v-container>
      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
        >
          <v-card outlined>
            <v-img
              src="https://rrgi.ca/wp-content/gallery/galvanizing-portfolio/IMG_2512-1.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            flat
            color="transparent"
          >
            <v-card-title>Hot-Dip Coating </v-card-title>

            <v-card-text>
              “Hot-dip galvanizing is a proven technology that combats corrosion for decades without the need for maintenance.”-American Galvanizers Association (Lets backlink to their website) This practice is essentially simple and delivers a definite advantage over other rust protection techniques. As the steel is dipped in the kettle, the iron from the steel metallurgically responds with the molten zinc to create a tightly-bonded metal coating that offers superior rust protection to steel. At North American Galvanizing Industries LLC, we process our work through 5 different preparation pools to allow the steel to bond to the purest zinc coating.
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
          order-md="2"
        >
          <v-card outlined>
            <v-img
              src="https://rrgi.ca/wp-content/gallery/galvanizing-portfolio/IMG_2512-1.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            color="transparent"
            flat
          >
            <v-card-title>Efficiency in Delivering
            </v-card-title>

            <v-card-text>
              <p>
                Our quick Turn around times are due to our galvanizing plants high capacity and efficient logistics, when the job needs to get done quickly you can count on us to get it done without compromising quality.

              </p>

            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <v-row
        align="center"
        class="mb-5"
      >
        <v-col
          cols="12"
          md="4"
        >
          <v-card outlined>
            <v-img
              src="https://rrgi.ca/wp-content/gallery/galvanizing-portfolio/IMG_2512-1.jpg"
              height="250"
            />
          </v-card>
        </v-col>

        <v-col
          class="px-0"
          cols="12"
          md="8"
        >
          <v-card
            flat
            color="transparent"
          >
            <v-card-title>Lorem ipsum dolor sit amet</v-card-title>

            <v-card-text>
              <p>
                Te dolor consul mei, etiam molestie indoctum usu ad, qui inermis eleifend an. Pro iriure alienum incorrupte ex, cu diceret moderatius mei. Te corrumpit posidonium sit, in cum nonumy utamur. Usu impedit patrioque vituperatoribus ei, cu voluptua nominati philosophia mel. Sea at legendos percipitur, nulla dicant convenire ne duo. Veniam epicuri vis cu, ea pri alii ceteros fierent.
              </p>
              <p>
                Te dolor consul mei, etiam molestie indoctum usu ad, qui inermis eleifend an. Pro iriure alienum incorrupte ex, cu diceret moderatius mei. Te corrumpit posidonium sit, in cum nonumy utamur. Usu impedit patrioque vituperatoribus ei, cu voluptua nominati philosophia mel. Sea at legendos percipitur, nulla dicant convenire ne duo. Veniam epicuri vis cu, ea pri alii ceteros fierent.
              </p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

    </v-container>
  </section>
</template>

<script>
export default {
  layout: "services",
  metaInfo: {
    title: "Services",
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
    SectionHeader: () => import("@/components/SectionHeader")
  },

  data: () => ({
    testimonial: {
      blurb:
        "With Alpha Construction managing all of our customer-facing services and ASCC, helping us monitor and understand building performance, Abocado is in great shape to create and release new products.",
      person: "Jay Oakrson",
      title: "CEO Avocado"
    }
  })
};
</script>
