<template>
  <div class="container">
    <div class="head">
      <h1>WHY CHOOSE US</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos
        debitis.
      </p>
    </div>
    <div class="main">
      <v-row>
        <v-col v-for="feature in features" :key="feature" cols="12" sm="4">
          <div class="data">
            <h3>
              <v-icon color="blue" class="pr-3">{{ feature.icon }}</v-icon
              >{{ feature.title }}
            </h3>
            <p class="h4" align="left">{{ feature.desc }}</p>
          </div>
        </v-col>
      </v-row>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      features: [
        {
          title: "Refreshing Design",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: "mdi-page-layout-header-footer",
        },
        {
          title: "Fully Responsive",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: "mdi-cellphone",
        },
        {
          title: "Fat & Smooth",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: " mdi-rocket-launch",
        },
        {
          title: "SEO Optimize",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: "mdi-database ",
        },
        {
          title: "Clean Code",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: "mdi-leaf",
        },
        {
          title: "Free 24/7 Support",
          desc: "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et magna aliqua.",
          icon: "mdi-lead-pencil ",
        },
      ],
    };
  },
};
</script>
<style scoped>
.h4 {
  margin-top: 5px;
  margin-left: 40px;
}
</style>