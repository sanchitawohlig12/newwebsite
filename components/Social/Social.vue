<template>
  <v-tabs class="d-flex justify-end">
    <v-btn v-for="social in socials" :key="social" icon>
      <v-icon :color="social.color">
        {{ social.icon }}
      </v-icon>
    </v-btn>
  </v-tabs>
</template>

<script>
export default {
  data () {
    return {
      socials: [
        { name: 'facebook', icon: 'mdi-facebook', color: 'blue darken-1' },
        { name: 'instagram', icon: 'mdi-instagram', color: 'pink lighten-2' },
        { name: 'pinterest', icon: 'mdi-pinterest', color: 'red lighten-1' },
        { name: 'twitter', icon: 'mdi-twitter', color: 'blue lighten-1' },
        { name: 'youtube', icon: 'mdi-youtube', color: 'red' }
      ]
    }
  }
}
</script>

<style>
</style>
