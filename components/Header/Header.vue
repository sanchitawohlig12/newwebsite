<template>
  <div>
    <v-carousel cycle :height="$vuetify.breakpoint.smAndUp ? '600' : '700'">
      <v-carousel-item
        v-for="(item, i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <div justify="center" align="center">
          <h1 class="h1">
            {{ item.title }}
          </h1>
          <h3 class="p">
            {{ item.caption }}
          </h3>
          <v-btn class="btn" x-large rounded color="primary" dark>
            Get Started
          </v-btn>
          <div class="play">
            <v-btn
              class="mx-2"
              fab
              dark
              color="pink"
              elevation="24"
              @click="overlay = !overlay"
            >
              <v-icon dark> mdi-play </v-icon>
            </v-btn>
          </div>
          <div class="video">
            <v-overlay :value="overlay" :absolute="absolute">
              <div>
                <video width="600" controls autoplay>
                  <source src="../../assets/Video/1.mp4" type="video/mp4" />
                  Your browser does not support HTML video.
                </video>
              </div>
              <div>
                <v-btn
                  class="mx-2"
                  fab
                  dark
                  small
                  color="red"
                  elevation="24"
                  @click="overlay = false"
                >
                  <v-icon dark> mdi-close </v-icon>
                </v-btn>
              </div>
            </v-overlay>
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTvQOfYdk20E70vc5D1tV34WwC5jSSP3oEpLQ&usqp=CAU.jpg",
          title: "Ultimate Platform to monitor your best workflow.",
          caption:
            "It should be noted that although application software is thought of asa program, it can be anything that runs on a computer.",
        },
        {
          src: "https://image.shutterstock.com/image-photo/leaves-dark-shade-600w-1065614543.jpg",
          title: "Ultimate Platform to monitor your best workflow.",
          caption:
            "It should be noted that although application software is thought of asa program, it can be anything that runs on a computer.",
        },
        {
          src: "https://image.shutterstock.com/image-photo/leaves-dark-shade-600w-1065614543.jpg",
          title: "Ultimate Platform to monitor your best workflow.",
          caption:
            "It should be noted that although application software is thought of asa program, it can be anything that runs on a computer.",
        },
        {
          src: "https://wallpaperaccess.com/full/2957951.jpg",
          title: "Ultimate Platform to monitor your best workflow.",
          caption:
            "It should be noted that although application software is thought of asa program, it can be anything that runs on a computer.",
        },
      ],
      overlay: false,
      absolute: false,
    };
  },
};
</script>
<style scoped>
.h1 {
  color: white;
  margin-top: 100px;
}
.p {
  color: white;
  font-size: 25px;
  text-align: center;
}
.btn {
  margin-top: 5rem;
  margin-right: 100px;
}
.play {
  margin-top: -55px;
  margin-left: 150px;
}
</style>