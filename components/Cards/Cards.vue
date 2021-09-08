<template>
  <v-container>
    <scroll-wrap target="blog-list">
      <h3 class="display-2 text-center mb-4">Latest News</h3>
      <p class="body-1 text-center mb-4">
        Quis ipsum suspendisse ultrices gravida. Risus commodo viverra maecenas
        accumsan lacus vel facilisis.
      </p>
      <div id="blog-list" class="blog-wrap">
        <v-row justify="center">
          <v-col md="9" cols="12">
            <v-row>
              <v-col
                v-for="(item, index) in blogData"
                :key="index"
                md="4"
                cols="12"
                class="px-4"
              >
                <v-card max-width="500">
                  <v-img :src="item.img" class="white--text" height="200px" />
                  <v-card-title class="title">
                    {{ item.title }}
                  </v-card-title>
                  <v-card-text>
                    <span class="text--primary">
                      <span>{{ item.desc }}</span>
                    </span>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn text color="black"> Read more </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </div>
    </scroll-wrap>
  </v-container>
</template>

<style scoped lang="scss">
//@import './blog-style';
</style>

<script>
//import BlogCard from '../Cards/BlogCard'
//import ScrollWrap from '../ScrollWrap'

export default {
  components: {
    //BlogCard,
    //ScrollWrap,
  },
  data() {
    return {
      blogData: [
        {
          title: "First Leaf",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          img: "https://img.freepik.com/free-photo/tree-leaves-dark-pattern-background_232693-137.jpg?size=626&ext=jpg&ga=GA1.2.1936636705.1630627200",
        },
        {
          title: "Second Leaf",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          img: "https://images.unsplash.com/photo-1541855951501-fc42a85d86d3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80",
        },
        {
          title: "Third Leaf",
          desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTIFos_2BeZoyEmxEg_a1BISGh0zJhxWE3QGnlgc37KJBmottlMglQqC4Jwj4YXo5-u2M0&usqp=CAU",
        },
      ],
    };
  },
};
</script>
<style scoped>
.title {
  font-size: 20px;
  font-weight: bold;
}
</style>
