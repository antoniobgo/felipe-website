<script setup>
import { ref } from "vue";
import SkillLine from "@/components/SkillLine.vue";
import SoftwareLine from "@/components/SoftwareLine.vue";

const portugueseValue = ref(95);
const englishValue = ref(70);
const spanishValue = ref(45);

const skills = ref([
  {
    title: "Art Director",
    rating: 4,
  },
  {
    title: "Animation",
    rating: 4,
  },
  {
    title: "UX/UI",
    rating: 3,
  },
  {
    title: "Photography",
    rating: 4,
  },
  {
    title: "Video Edition",
    rating: 3,
  },
  {
    title: "Visual Effects",
    rating: 2,
  },
  {
    title: "3D and Render",
    rating: 3,
  },
  {
    title: "Illustration",
    rating: 2,
  },
  {
    title: "Short film script",
    rating: 2,
  },
]);

const softwares = ref([
  {
    title: "Ad. Premier",
    iconPath: "pr.png",
  },
  {
    title: "Ad. Photoshop",
    iconPath: "ps.png",
  },
  {
    title: "Ad. Illustrator",
    iconPath: "ai.png",
  },
  {
    title: "Ad. After Effects",
    iconPath: "ae.png",
  },
  {
    title: "Blender 3d",
    iconPath: "blender.png",
  },
  {
    title: "Figma",
    iconPath: "figma.png",
  },
  {
    title: "DaVinci",
    iconPath: "davince.png",
  },
  {
    title: "Unreal",
    iconPath: "unreal.png",
  },
]);
</script>

<template>
  <div class="about">
    <v-row justify="center" class="about-container" no-gutters>
      <v-col cols="6">
        <v-row no-gutters>
          <p class="title-text mb-15">ABOUT</p>
        </v-row>
        <v-row no-gutters justify="" class="description-container">
          <v-col cols="4" align-self="center">
            <v-row no-gutters justify="center">
              <div class="about-picture-container"></div>
            </v-row>
          </v-col>
          <v-col cols="8" align-self="center">
            <p class="description-text">
              Currently motion designer senior and 3d student, living in
              Florianópolis, Brazil. Dedicated, responsive, experienced, loves
              nature, electronics, skateboarding, studying, creating things and
              working in a team.
            </p>
          </v-col>
        </v-row>
        <v-row no-gutters class="mt-15">
          <v-col
            cols="4"
            style="border-right: solid 2px #474543; margin-bottom: 3rem"
          >
            <div class="text-white w-75">
              <p class="about-title-text">Graduate</p>
              <ul class="pl-5 mt-5">
                <li class="description-text">
                  <p>Bachelor Degree in Design - UNISUL</p>
                </li>
                <li class="description-text">
                  <p>Degree in Technological Education - IFSC</p>
                </li>
              </ul>
              <p class="about-title-text mt-5">Languages</p>
              <v-row no-gutters dense justify="space-between" align="center">
                <v-col cols="9" class="mt-5">
                  <v-row
                    no-gutters
                    dense
                    justify="space-between"
                    align="center"
                  >
                    <p class="description-text">Portuguese</p>
                    <v-progress-linear
                      height="12"
                      v-model="portugueseValue"
                      :buffer-value="bufferValue"
                      class="testizin mt-1"
                    ></v-progress-linear>
                  </v-row>
                </v-col>
              </v-row>
              <v-row no-gutters dense>
                <v-col cols="9">
                  <v-row
                    no-gutters
                    dense
                    justify="space-between"
                    align="center"
                  >
                    <p class="description-text">English</p>
                    <v-progress-linear
                      height="12"
                      v-model="englishValue"
                      :buffer-value="bufferValue"
                      class="testizin mt-1"
                    ></v-progress-linear>
                  </v-row> </v-col
              ></v-row>
              <v-row no-gutters dense>
                <v-col cols="9">
                  <v-row
                    no-gutters
                    dense
                    justify="space-between"
                    align="center"
                  >
                    <p class="description-text">Spanish</p>
                    <v-progress-linear
                      height="12"
                      v-model="spanishValue"
                      :buffer-value="bufferValue"
                      class="testizin mt-1"
                    ></v-progress-linear>
                  </v-row>
                </v-col>
              </v-row>
            </div>
          </v-col>
          <v-col
            cols="4"
            style="border-right: solid 2px #474543; margin-bottom: 3rem"
            ><div>
              <p class="about-title-text ml-7">Skills</p>
              <v-row no-gutters dense justify="center" align="center">
                <v-col cols="12" class="mt-5">
                  <div class="">
                    <SkillLine
                      v-for="item in skills"
                      :key="item.title"
                      :title="item.title"
                      :rating="item.rating"
                    />
                  </div>
                </v-col>
              </v-row>
            </div>
          </v-col>
          <v-col cols="4">
            <div>
              <p class="about-title-text ml-7">Softwares</p>
              <v-row no-gutters dense justify="center" align="center">
                <v-col cols="12" class="mt-5">
                  <div class="">
                    <SoftwareLine
                      v-for="item in softwares"
                      :key="item.title"
                      :title="item.title"
                      :iconPath="item.iconPath"
                    />
                  </div>
                </v-col>
              </v-row></div
          ></v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<style>
.testizin {
  max-width: 80px;
}
.about {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.about-container {
  padding-top: 5rem;
}
.title-text {
  font-size: 1.5rem;
  color: #c8c8c8;
  letter-spacing: 1rem;
}
.description-text {
  font-size: 1rem;
  line-height: 2rem;
  color: #858585;
  letter-spacing: 0.031rem;
}
.about-title-text {
  font-size: 1.25rem;
  line-height: 1.75rem;
  color: #858585;
  letter-spacing: 0.5rem;
}
.description-container {
  margin-top: 4rem;
  height: 270px;
  border: solid 2px #474543;
}
.about-picture-container {
  min-width: 173px;
  min-height: 156px;
  background-image: url("../assets/about_pic.png");
}
</style>
