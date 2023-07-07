<template>
  <v-app class="transparent">
      <div class="stars"></div>
      <div class="cloud"></div>
      <MenuBar />
          <v-main fluid class="transparent">
              <v-container class="transparent">
                  <v-row class="transparent">
                      <v-col
                        cols="12"
                        class="transparent pa-0"
                      >
                          <nuxt />
                      </v-col>
                  </v-row>
              </v-container> 
          </v-main>
      <Footer />
  </v-app>    
</template>

<script>
import MenuBar from '@/components/MenuBar.vue';
import Footer from '@/components/Footer.vue';
export default {
  data () {
    return {
      
    }
  },
  components: { MenuBar, Footer }
}
</script>

<style>
.transparent {
    background-color: transparent !important;
}

*{
    margin: 0;
    padding: 0;
}

@keyframes move-twink-back {
    from {background-position:0 0;}
    to {background-position:-10000px 5000px;}
}

@keyframes move-clouds-back {
    from {background-position:0 0;}
    to {background-position:10000px 0;}
}

.stars, .twinkling, .clouds {
  position:absolute;
  top:0;
  left:0;
  right:0;
  bottom:0;
  width:100%;
  height:100%;
  display:block;
}

.stars {
  background:#000 url('@/static/bg_imgs/stars.png') repeat top center;
  z-index:0;
}

.twinkling{
  background:transparent url('@/static/bg_imgs/twinkling.png') repeat top center;
  z-index:1;
  animation:move-twink-back 200s linear infinite;
}

.clouds{
    background:transparent url('@/static/bg_imgs/clouds.png') repeat top center;
    z-index:2;
    opacity: .4;
    animation:move-clouds-back 200s linear infinite;
}
</style>
