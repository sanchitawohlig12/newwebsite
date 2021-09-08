<template>
  <section id="features" class="featuresArea">
    <v-container>
      <div class="section-title pb-3">
        <h1>{{ title }}</h1>
        <p>
          {{ subTitle }}
        </p>
      </div>
      <v-row>
        <v-col v-for="card in featuresCards" :key="card" cols="12" sm="4">
          <v-hover v-slot="{ hover }">
            <v-sheet
              :elevation="hover ? 16 : 2"
              :class="{ 'on-hover': hover }"
              class="pa-6"
            >
              <div class="singleFeature">
                <v-icon
                  :color="card.color"
                  class="icon"
                  :class="card.class"
                  large
                  >{{ card.icon }}</v-icon
                >
                <h3 class="pt-8">{{ card.name }}</h3>
                <p class="pa-2">
                  {{ card.desc }}
                </p>
              </div>
            </v-sheet>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "OUR SERVICES",
      subTitle:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores optiomagni adipisci culpa error iusto",
      featuresCards: [
        {
          name: "Content Writing",
          icon: "mdi-lead-pencil",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#f36",
          class: "bg-1",
        },
        {
          name: "Web Development",
          icon: "mdi-cog",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#307ffa",
          class: "bg-2",
        },
        {
          name: "Graphic Design",
          icon: "mdi-chart-bell-curve-cumulative",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#18b32a",
          class: "bg-3",
        },
        {
          name: "UI/UX Design",
          icon: "mdi-layers-triple-outline",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#08722e",
          class: "bg-4",
        },
        {
          name: "App Development",
          icon: "mdi-cellphone",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#ba7a09",
          class: "bg-5",
        },
        {
          name: "Digital Marketing",
          icon: " mdi-briefcase-account-outline",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. A odio magnam atque, amet dignissimos ipsam voluptatum iste, optio autem molestiae asperiores. Ipsa officia rem voluptates?",
          color: "#097966",
          class: "bg-6",
        },
      ],
    };
  },
};
</script>

<style>
#features {
  text-align: center;
  color: black;
}

.featuresArea {
  position: relative;
  z-index: 1;
  padding-bottom: 70px;
  padding-top: 100px;
  background-color: #f9f9f9;
}
.v-row {
  box-sizing: border-box;
}

.singleFeature {
  text-align: center;
  padding: 20px;
}
.pa-2 {
  font-family: "Times New Roman", Times, serif;
}

.icon {
  width: 80px;
  height: 80px;
  display: inline-block;
  position: relative;
  z-index: 1;
  transition: 0.5s;
  border-radius: 50px;
  /* transform: (180deg);*/
  box-shadow: 5px 5px 1px 0 rgb(0 0 0 / 10%);
}
.ico::before {
  box-sizing: border-box;
}
.bg-1 {
  background: linear-gradient(
    180deg,
    #fb8488,
    #fb938f,
    #fba298,
    #fab0a2,
    #f9bdae
  );
}
.bg-2 {
  background: linear-gradient(
    180deg,
    #a3c7fd,
    #a6d0fd,
    #acd8fd,
    #b5e0fc,
    #c0e7fb
  );
}
.bg-3 {
  background: linear-gradient(
    180deg,
    #a8ed95,
    #b2f18f,
    #bcf588,
    #c8f980,
    #d4fc79
  );
}
.bg-4 {
  background: linear-gradient(
    180deg,
    #40ed92,
    #34f1a5,
    #2df4b7,
    #2ef7c8,
    #38f9d7
  );
}
.bg-5 {
  background: linear-gradient(180deg, #fcc21e, #fdc919, #fecf12, #ffd60a, #fd0);
}
.bg-6 {
  background: linear-gradient(
    180deg,
    #37ceb9,
    #50d1c1,
    #65d3c7,
    #78d6ce,
    #89d8d3
  );
}
</style>