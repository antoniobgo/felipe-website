<script setup>
import PortfolioCard from "@/components/PortfolioCard.vue";
import { useDisplay } from "vuetify";

const { mdAndUp } = useDisplay();

const portfolioItems = [
  {
    jobName: "MOTION HUD",
    jobCompany: "Agência 300",
    softwareText: "Software: After Effects",
    backgroundUrl: "motion/motion_hud.png",
  },
  {
    jobName: "RUNNING CYCLES",
    jobCompany: "Autoral test character animation",
    softwareText: "Software: After Effects",
    backgroundUrl: "motion/running.png",
  },
  {
    jobName: "APPS LAUNCH CAMPAIGN",
    jobCompany: "Hughueir APS",
    softwareText:
      "Softwares: After Effects, Premiere, Photoshop and Illustrator",
    backgroundUrl: "motion/launch_app.png",
  },
  {
    jobName: "WAKE UP",
    jobCompany: "Illustration and Animation Authorial",
    softwareText: "Softwares: After Effects, Premiere and Illustrator",
    backgroundUrl: "motion/wakeup.png",
  },
  {
    jobName: "PRICE OFFERS VIDEO",
    jobCompany: "Led Outdoor",
    softwareText: "Softwares: C4D, After Effects",
    backgroundUrl: "motion/imperatriz.png",
  },
  {
    jobName: "PRE-LAUNCH VIDEO MARFARÁ",
    jobCompany: "Agencia 300",
    softwareText: "Software: After Effects",
    backgroundUrl: "motion/marfara.png",
  },
  {
    jobName: "SCRIPT, EDITION AND MOTION",
    jobCompany: "Plaza Jardim",
    softwareText: "Softwares: Premiere and After Effects",
    backgroundUrl: "motion/plaza.png",
  },
  {
    jobName: "ADVERTISING CAMPAIGN",
    jobCompany: "Oliveira Imóveis",
    softwareText: "Softwares: After Effects and Illustrator",
    backgroundUrl: "motion/oliveira.png",
  },
  {
    jobName: "NARRATIVA INSPIRA MOVIMENTAR",
    jobCompany: "Autoral",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "motion/capa_motion.png",
  },
  {
    jobName: "MOTION EVENT",
    jobCompany: "Creative Led",
    softwareText: "Softwares: Illustrator and After Effects",
    backgroundUrl: "motion/duelo.png",
  },
  {
    jobName: "MOTION AND VISUAL IDENTITY",
    jobCompany: "Essência don Campo",
    softwareText: "Softwares: Illustrator, Photoshop and After Effects",
    backgroundUrl: "motion/essencia_do_campo.png",
  },
  {
    jobName: "MOTION LOGO",
    jobCompany: "Rosane Dutra",
    softwareText: "Softwares: After Effects",
    backgroundUrl: "motion/rosane.png",
  },
];
</script>

<template>
  <div class="motion">
    <v-row
      no-gutters
      justify="center"
      :class="
        mdAndUp ? 'motion-container-margins' : 'mobile-motion-container-margins'
      "
    >
      <v-col cols="11" md="9">
        <v-row no-gutters justify="center">
          <v-col cols="12" md="8">
            <v-row no-gutters justify="start">
              <p :class="mdAndUp ? 'title-text' : 'mobile-title-text'">
                MOTION
              </p>
            </v-row>
            <v-row>
              <v-col cols="12" md="8">
                <PortfolioCard
                  :job="portfolioItems[0]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[1]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[2]"
                  :cardHeight="mdAndUp ? '444' : '150'"
                />
              </v-col>
              <v-col cols="12" md="8">
                <PortfolioCard
                  :job="portfolioItems[3]"
                  :cardHeight="mdAndUp ? '444' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[4]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[5]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[6]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[7]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="8">
                <PortfolioCard
                  :job="portfolioItems[8]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[9]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[10]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
              <v-col cols="12" md="4">
                <PortfolioCard
                  :job="portfolioItems[11]"
                  :cardHeight="mdAndUp ? '310' : '150'"
                />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped>
.motion {
  background-color: #101010;
  width: 100%;
  height: 100%;
}
.motion-container-margins {
  padding-top: 5rem;
  margin-bottom: 10rem;
}
.mobile-motion-container-margins {
  padding-top: 2rem;
  margin-bottom: 3rem;
}
.title-text {
  font-size: 1.5rem;
  color: #cdcdcd;
  letter-spacing: 1rem;
  margin-bottom: 3rem;
}
.mobile-title-text {
  font-size: 0.875rem;
  color: #cdcdcd;
  letter-spacing: 0.3rem;
  margin-bottom: 1rem;
  margin-left: 1.85rem;
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
.card-2 {
  /* width: 40rem; */
  height: 27.7rem;
}
.card-3 {
  /* width: 40rem; */
  min-height: 19.3rem;
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
</style>
