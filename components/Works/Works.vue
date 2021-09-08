<template>
  <div class="container">
    <div class="head">
      <h1>OUR WORKS</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos
        debitis.
      </p>
    </div>
    <div v-if="$vuetify.breakpoint.smAndUp" class="btns" align="center">
      <v-btn class="btn" x-large rounded color="primary" dark> ALL </v-btn>
      <v-btn class="btn" x-large rounded color="primary" dark> DESIGN </v-btn>
      <v-btn class="btn" x-large rounded color="primary" dark>
        DEVELOPMENT
      </v-btn>
      <v-btn class="btn" x-large rounded color="primary" dark> PRINT </v-btn>
    </div>
    <div v-if="!$vuetify.breakpoint.smAndUp" class="btns d-flex" align="center">
      <v-btn class="btn" small rounded color="primary" dark> ALL </v-btn>
      <v-btn class="btn" small rounded color="primary" dark> DESIGN </v-btn>
      <v-btn class="btn" small rounded color="primary" dark>
        DEVELOPMENT
      </v-btn>
      <v-btn class="btn" small rounded color="primary" dark> PRINT </v-btn>
    </div>
    <div class="images">
      <v-row justify="center">
        <v-col>
          <img
            class="img"
            src="https://image.shutterstock.com/image-photo/dark-green-leaves-on-black-260nw-1593310846.jpg"
            alt=""
          />
        </v-col>
        <v-col>
          <img
            class="img"
            src="https://img.freepik.com/free-photo/tree-leaves-dark-pattern-background_232693-137.jpg?size=626&ext=jpg&ga=GA1.2.1936636705.1630627200"
            alt=""
          />
        </v-col>
        <v-col>
          <img
            class="img"
            src="https://c0.wallpaperflare.com/preview/934/105/169/russia-uva-color-dark.jpg"
            alt=""
          />
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col>
          <img
            class="img"
            src="https://image.shutterstock.com/image-photo/tropical-banana-leaf-texture-garden-260nw-1894090834.jpg"
            alt=""
          />
        </v-col>
        <v-col>
          <img
            class="img"
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQk0lrkqXAnc2ih721W0p5bihPmvlTIlF8xwg&usqp=CAU"
            alt=""
          />
        </v-col>
        <v-col>
          <img
            class="img"
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTaaOVQC6KNQWdD6X5k_-wPS6pqAjBfZtse8w&usqp=CAU"
            alt=""
          />
        </v-col>
      </v-row>
    </div>
  </div>
</template>
<style scoped>
.btns {
  margin-top: 50px;
}
.img {
  height: 300px;
  width: 300px;
}
.img {
  transition: transform 0.5s ease;
}

/* [3] Finally, transforming the image when container gets hovered */
.img:hover {
  transform: scale(1.1);
}
.images {
  padding-top: 40px;
  overflow: hidden;
}
@media only screen and (max-width: 991px) {
  .btns {
    margin-left: 50px;
  }
  .images {
    margin-left: 50px;
  }
}
</style>