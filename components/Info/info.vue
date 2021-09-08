<template>
  <div class="container">
    <v-row>
      <v-col v-for="detail in details" :key="detail" cols="12" sm="12">
        <v-icon color="pink">{{ detail.icon }}</v-icon>
        <h3>{{ detail.title }}</h3>
        <p>{{ detail.desc }}</p>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      details: [
        {
          title: "Location",
          desc: "1900 Pico Blvd, New York br Centernial, colorado",
          icon: "mdi-map-marker-radius",
        },
        {
          title: "E-mail",
          desc: "info@example.com",
          icon: "mdi-hexagram-outline",
        },
        { title: "Phone", desc: "+48 123 456 789", icon: "mdi-phone-classic" },
      ],
    };
  },
};
</script>
<style scoped>
.container {
}
</style>