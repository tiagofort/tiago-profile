<template>
    <v-footer :width="getWidth" absolute  color="#000000">
      <v-spacer></v-spacer>
        <span>Tiago Fortaleza Gai&copy; - {{ new Date().getFullYear() }}</span>
      <v-spacer></v-spacer>
    </v-footer>
</template>

<script>
export default {
  data: () => ({
  }),
  computed:{
    getWidth(){
      return this.$vuetify.breakpoint.width;
    }
  }
}
</script>