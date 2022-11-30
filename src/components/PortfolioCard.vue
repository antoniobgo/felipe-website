<script setup>
import { defineProps, ref } from "vue";

const props = defineProps(["job", "cardHeight"]);
const job = ref(props.job);
const cardHeight = ref(props.cardHeight);
const styleObject = ref({
  backgroundImage:
    "linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)), " +
    `url(${require("@/assets/images/" + job.value.backgroundUrl)})`,
  minHeight: cardHeight.value + "px",
  backgroundSize: "cover",
});
const onHoverStyleObject = ref({
  backgroundImage:
    "linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)), " +
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
        <div class="mb-5 ml-5">
          <p class="text-left portfolio-card-font text-white">
            {{ job.jobName }}
          </p>
          <p class="text-left portfolio-card-font text-white">
            {{ job.jobCompany }}
          </p>
          <p class="text-left portfolio-card-font text-white">
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
.portfolio-background {
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url("../assets/threed_bg.png");
}
.portfolio-background-onhover {
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url("../assets/threed_bg.png");
}
.bottom-text-area {
  height: 72px;
}
.portfolio-card-font {
  font-size: 0.875rem;
  letter-spacing: 0.156rem;
  line-height: 1.438rem;
}
.card-height {
  min-height: 19rem;
}
</style>
