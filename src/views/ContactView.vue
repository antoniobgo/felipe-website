<script setup>
// @ is an alias to /src
</script>

<template>
  <div class="contact">
    <div class="contact-container">
      <v-row justify="center">
        <v-spacer></v-spacer>
        <v-col cols="5">
          <v-card variant="outlined" style="border-width: 0">
            <v-card-title>
              <v-row justify="start" no-gutters dense>
                <p class="title-text">CONTACT</p>
              </v-row>
            </v-card-title>
            <v-card-text>
              <p class="description-text">
                Send an email to felipearaujodemirandagomes@gmail.com or fill
                out the form below.
              </p>
              <v-row class="mt-10" no-gutters>
                <v-col cols="9">
                  <p class="subtitle-text">Name</p>
                  <v-text-field
                    class="form-field"
                    bg-color="#D9D9D9"
                    density="compact"
                    variant="outlined"
                  ></v-text-field>
                  <p class="subtitle-text">Email Address</p>
                  <v-text-field
                    class="form-field"
                    bg-color="#D9D9D9"
                    density="compact"
                    variant="outlined"
                  ></v-text-field>
                  <p class="subtitle-text">Message</p>
                  <v-textarea
                    bg-color="#D9D9D9"
                    density="compact"
                    variant="outlined"
                  >
                  </v-textarea>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
      </v-row>
      <!-- <v-row class="contact-container" no-gutters>
      <v-col cols="4">
        <v-row justify="start">
          <p class="title-text">CONTACT</p>
        </v-row>
        <v-row no-gutters>
          <p class="description-text">
            Send an email to felipearaujodemirandagomes@gmail.com or fill out
            the form below.
          </p>
        </v-row>
      </v-col>
    </v-row> -->
    </div>
  </div>
</template>

<style scoped>
.contact {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.contact-container {
  padding-top: 5rem;
}
.title-text {
  font-family: Alata, sans-serif;
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 1rem;
  margin-bottom: 3rem;
}
.description-text {
  font-family: Alata, sans-serif;
  font-size: 1rem;
  color: #858585;
  letter-spacing: 0.1rem;
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
  /* background-color: #d9d9d9; */
}
.subtitle-text {
  font-size: 0.81em;
  letter-spacing: 0.038;
  font-weight: 400;
  color: #858585;
}
</style>
