<script setup>
import { ref, defineProps } from "vue";
import { useDisplay } from "vuetify";

const { mdAndUp } = useDisplay();

const props = defineProps(["testimonialContent"]);
const testimonialContent = ref(props.testimonialContent);
</script>

<template>
  <v-row justify="center" class="testimonial-card" no-gutters dense>
    <v-col :cols="mdAndUp ? 7 : 12" align-self="center">
      <v-container class="pa-0">
        <p
          class="text-center"
          :class="mdAndUp ? 'citation-text' : 'smaller-citation-text'"
        >
          {{ testimonialContent.content }}
        </p>
        <div class="grey-color">
          <v-row no-gutters dense justify="center">
            <p
              class="mt-10"
              :class="mdAndUp ? 'testimonial-text' : 'smaller-testimonial-text'"
            >
              {{ testimonialContent.name }}
            </p>
          </v-row>
          <v-row no-gutters dense justify="center">
            <p
              :class="mdAndUp ? 'testimonial-text' : 'smaller-testimonial-text'"
            >
              {{ testimonialContent.jobTitle }}
            </p>
          </v-row>
        </div>
      </v-container>
    </v-col>
  </v-row>
</template>

<style>
.testimonial-card {
  height: 200px;
}
.grey-color {
  color: #858585;
}
</style>
