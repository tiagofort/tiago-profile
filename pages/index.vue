<template>
  <v-container :max-width="getMaxWidth" class="transparent">
            <v-row justify="center" class="mb-5 transparent">
                <v-col class="pa-0">
                      <v-sheet id="home" :height="getHeight" class="pa-1 mt-10" color="transparent">
                          <AboutMe />
                      </v-sheet>
                </v-col>
           </v-row> 
           <v-row justify="center" class="mb-5">
                <v-col>
                      <v-sheet id="skills" height="1000" class="pa-1 mt-10" color="transparent">
                          <Skills />
                      </v-sheet>
                </v-col>
           </v-row> 
           <v-row justify="center" class="mb-5">
                <v-col>
                      <v-sheet id="projects" height="900" class="pa-1 mt-10" color="transparent">
                          <Projects />
                      </v-sheet>
                </v-col>
           </v-row>
           <v-row justify="center" class="mb-5">
                <v-col>
                      <v-sheet id="contact" height="600" class="pa-1 mt-10" color="transparent">
                          <Contact />
                      </v-sheet>
                </v-col>
           </v-row>  
  </v-container>
</template>

<script>
import AboutMe  from '@/components/AboutMe.vue';
import Skills   from '@/components/Skills.vue';
import Projects from '@/components/Projects.vue';
import Contact  from '@/components/Contact.vue';
export default { 
computed:{
    getMaxWidth (){
        return this.$vuetify.breakpoint.width - (this.$vuetify.breakpoint.width * 0.2);
    },
    getHeight(){
        return this.$vuetify.breakpoint.xs ? "auto" : "1000"
    }
},
components: { AboutMe, Skills, Projects, Contact }
}
</script>

<style>
.transparent {
background-color: transparent;
}
</style>
