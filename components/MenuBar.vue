<template>
        <div>
            <v-app-bar
              app
              color="#000000"
              :width="getWidth"
            >
              <v-container class="fill-height hidden-xs-only">
                <v-spacer></v-spacer>
                <v-btn @click="scrollToSection(link.id_scrool)" v-for="link in links" :key="link.title" text class="white--text">
                  {{ link.title }}
                </v-btn>
              </v-container>
              <v-container class="fill-height hidden-sm-and-up mb-3">
                <v-spacer></v-spacer>
                <v-btn fab dark small color="#121212" @click="drawer = !drawer">
                    <v-icon class="white--text">
                        mdi-menu
                    </v-icon>
                </v-btn>
              </v-container>
            </v-app-bar>
            <v-navigation-drawer
              v-model="drawer"
              :absolute="getAbsolute"
              :app="getApp"
              color="#121212"
            >
              <v-sheet class="mt-1 pa-2" height="auto" color="#121212">
                  <v-btn
                    color="#BDBDBD"
                    small
                    fab
                    right
                    absolute
                    @click="drawer = !drawer"
                  >
                      <v-icon>mdi-close</v-icon>
                  </v-btn>
              </v-sheet>
              <v-list
                nav
                dense
              >
                  <v-list-item-group
                    v-model="group"
                    active-class="white--text text--accent-4"
                    class="mt-12"
                  >
                    <v-list-item @click="scrollToSection(link.id_scrool)" v-for="link in links" :key="link.title">
                      <v-list-item-title class="text-subtitle-1 ml-2">{{ link.title }}</v-list-item-title>
                    </v-list-item>
                  </v-list-item-group>
              </v-list>
              <v-sheet class="mt-10 pa-3" color="#121212">
                  <div class="mb-4 text-subtitle-1">Get in Touch</div>
                  <v-row class="pa-3" align="center" justify="center">
                    <v-col class="pa-0">
                        <v-btn
                          color="white"
                          icon
                          @click="getTouch('https://www.linkedin.com/in/tiago-fortaleza-gai/')"                                        
                        >
                            <v-icon x-large>
                                mdi-linkedin
                            </v-icon>
                        </v-btn>
                    </v-col>
                    <v-col class="pa-0">
                        <v-btn
                          color="white"
                          icon  
                          @click="getTouch('https://github.com/tiagofort')"                                  
                        >
                            <v-icon x-large>
                                mdi-git
                            </v-icon>
                        </v-btn>
                    </v-col>
                    <v-col class="pa-0">
                        <v-btn
                          color="white"
                          icon 
                          @click="getTouch('https://wa.me/353830679963')"                                   
                        >
                            <v-icon x-large>
                                mdi-whatsapp
                            </v-icon>
                        </v-btn>
                    </v-col>
                    <v-col class="pa-0">
                      <Dialog />
                    </v-col>
                  </v-row>
              </v-sheet>
            </v-navigation-drawer>
        </div>       
</template>

<script>
import Dialog from '@/components/Dialog.vue';
export default {
  data: () => ({
      links: 
      [
        {
          title: 'Home',
          id_scrool: '#home'
        },
        {
          title: 'Skills',
          id_scrool: '#skills'
        },
        {
          title: 'Projects',
          id_scrool: '#projects'
        },
        {
          title: 'Contact',
          id_scrool: '#contact'
        }
      ],
      drawer: false,
      group: null
  }),
  computed:{
    getWidth(){
      return this.$vuetify.breakpoint.width;
    },
    getApp(){
      return this.$vuetify.breakpoint.xs ? true : false;
    },
    getAbsolute(){
      return this.$vuetify.breakpoint.xs? false : true;
    }
  },
  methods: {
    scrollToSection(section){
      this.$vuetify.goTo(section, { duration: 1000, offset: 0 });
      this.drawer = false;
    },
    getTouch(url){
      window.open(url, '_blank');
    }, 
  },
  components:{ Dialog }
}
</script>

<style>
  /* This is for documentation purposes and will not be needed in your application */
  #lateral .v-btn--example {
    bottom: 0;
    position: absolute;
    margin: 0 0 16px 16px;
  }
</style>