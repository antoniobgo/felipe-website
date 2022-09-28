<script setup>
import { ref, defineProps } from "vue";

const props = defineProps(["testimonialContent"]);
const testimonialContent = ref(props.testimonialContent);
</script>

<template>
  <v-card variant="outlined" class="testimonial-card">
    <v-card-text>
      <p class="citation-text text-center">
        {{ testimonialContent.content }}
      </p>
    </v-card-text>
    <div class="grey-color">
      <v-row justify="center">
        <p class="citation-text">{{ testimonialContent.name }}</p>
      </v-row>
      <v-row justify="center">
        <p class="citation-text">{{ testimonialContent.jobTitle }}</p>
      </v-row>
    </div>
  </v-card>
</template>

<style>
.testimonial-card {
  /* width: 12.3rem; */
  height: 9rem;
  border-width: 0;
}
.grey-color {
  color: #858585;
}
</style>
