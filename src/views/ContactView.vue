<script setup>
import { useDisplay } from "vuetify";

const { mdAndUp } = useDisplay();
</script>

<template>
  <div class="contact">
    <div class="contact-container">
      <v-row justify="center">
        <v-col cols="10" md="4">
          <v-card variant="outlined" style="border-width: 0">
            <v-card-title>
              <p :class="mdAndUp ? 'title-text' : 'mobile-title-text'">
                CONTACT
              </p>
            </v-card-title>
            <v-card-text>
              <p
                :class="
                  mdAndUp ? 'description-text' : 'mobile-description-text'
                "
              >
                Send an email to
              </p>
              <p
                :class="
                  mdAndUp ? 'description-text' : 'mobile-description-text'
                "
              >
                felipearaujodemirandagomes@gmail.com
              </p>
              <p
                :class="
                  mdAndUp ? 'description-text' : 'mobile-description-text'
                "
              >
                or fill out the form below.
              </p>
              <v-row class="mt-5" no-gutters>
                <v-col cols="12">
                  <p class="subtitle-text">Name</p>
                  <v-text-field
                    bg-color="#D9D9D9"
                    variant="outlined"
                    density="compact"
                  ></v-text-field>
                  <p class="subtitle-text">Email Address</p>
                  <v-text-field
                    bg-color="#D9D9D9"
                    variant="outlined"
                    density="compact"
                  ></v-text-field>
                  <p class="subtitle-text">Message</p>
                  <v-textarea bg-color="#D9D9D9"> </v-textarea>
                  <v-btn
                    flat
                    class="font-menu about-button text-black mb-15 mt-3"
                    color="#D2B100"
                    >submit</v-btn
                  >
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<style scoped>
.testina {
  padding: 0px !important;
}
.contact {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.contact-container {
  padding-top: 3rem;
}
.my-class {
  padding: 0px;
}
.title-text {
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 0.5rem;
  line-height: 2rem;
  margin-bottom: 1rem;
}
.mobile-title-text {
  font-size: 0.875rem;
  color: #cdcdcd;
  letter-spacing: 0.3rem;
}
.description-text {
  font-size: 1rem;
  color: #858585;
  letter-spacing: 0.03rem;
  line-height: 2rem;
}
.mobile-description-text {
  font-size: 0.6rem;
  color: #cdcdcd;
  line-height: 1.1rem;
}
.description-container {
  padding-top: 2rem;
}
.card-1 {
  /* width: 19.3rem; */
  height: 27.7rem;
}
.card-2 {
  /* width: 40rem; */
  height: 27.7rem;
}
.card-3 {
  /* width: 40rem; */
  height: 19.3rem;
}
.card-4 {
  height: 19.3rem;
  /* width: 19.3rem; */
}
.cards-color {
  background-color: #313131;
  margin: 0.55rem;
  border-radius: 0;
}
.form-field {
  max-height: 30px !important;
  padding: 0px !important;
  /* max-height: 3px; */
  /* border-radius: 0px !important; */
}
.subtitle-text {
  font-size: 0.813rem;
  letter-spacing: 0.038rem;
  color: #858585;
  line-height: 1.7rem;
}
</style>
