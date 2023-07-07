<template>
        <div>
            <v-app-bar
              app
              color="#000000"
              :width="getWidth"
            >
              <v-container class="fill-height hidden-sm-and-down">
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
            </v-navigation-drawer>
        </div>       
</template>

<script>
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
  }
}
</script>