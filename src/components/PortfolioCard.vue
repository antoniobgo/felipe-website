<script setup>
import { defineProps, ref } from "vue";
import { useDisplay } from "vuetify";

const { mdAndUp } = useDisplay();

const props = defineProps(["job", "cardHeight"]);
const job = ref(props.job);
const cardHeight = ref(props.cardHeight);
console.log(cardHeight);
const styleObject = ref({
  backgroundImage:
    "linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)), " +
    `url(${require("@/assets/images/" + job.value.backgroundUrl)})`,
  minHeight: cardHeight.value + "px",
  backgroundSize: "cover",
});
const onHoverStyleObject = ref({
  backgroundImage:
    "linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), " +
    `url(${require("@/assets/images/" + job.value.backgroundUrl)})`,
  minHeight: cardHeight.value + "px",
  backgroundSize: "cover",
});
</script>
<template>
  <v-hover v-slot="{ isHovering, props }">
    <v-card
      :style="isHovering ? onHoverStyleObject : styleObject"
      class="h-100 rounded-0 huk"
      v-bind="props"
    >
      <div class="d-flex flex-column justify-end h-100" v-if="isHovering">
        <div :class="mdAndUp ? 'mb-5 ml-5' : 'mb-8 ml-8'">
          <p
            class="text-left"
            :class="
              mdAndUp ? 'portfolio-card-font' : 'mobile-portfolio-card-font'
            "
          >
            {{ job.jobName }}
          </p>
          <p
            class="text-left"
            :class="
              mdAndUp ? 'portfolio-card-font' : 'mobile-portfolio-card-font'
            "
          >
            {{ job.jobCompany }}
          </p>
          <p
            class="text-left"
            :class="
              mdAndUp ? 'portfolio-card-font' : 'mobile-portfolio-card-font'
            "
          >
            {{ job.softwareText }}
          </p>
        </div>
      </div>
      <!-- <v-row class="h-100" no-gutters dense justify="start">
        <v-col cols="12" align-self="end">
          <div v-if="isHovering" class="bottom-text-area">
            <v-row no-gutters dense>
              <v-col cols="10" class="ml-15 mb-15">
                <p class="text-left portfolio-card-font text-white">
                  {{ job.jobName }}
                </p>
                <p class="text-left portfolio-card-font text-white">
                  {{ job.jobCompany }}
                </p>
                <p class="text-left portfolio-card-font text-white">
                  {{ job.softwareText }}
                </p>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row> -->
    </v-card>
  </v-hover>
</template>

<style>
.bottom-text-area {
  height: 72px;
}
.portfolio-card-font {
  font-size: 0.875rem;
  letter-spacing: 0.156rem;
  line-height: 1.438rem;
  color: #cdcdcd;
}
.mobile-portfolio-card-font {
  font-size: 0.625rem;
  letter-spacing: 0.156rem;
  line-height: 1.15rem;
  color: #cdcdcd;
}
.card-height {
  min-height: 19rem;
}
</style>
