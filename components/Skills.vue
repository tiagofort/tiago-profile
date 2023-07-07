<template>
    <v-container  fill-height fluid class="transparent">
        <v-layout align-start justify-center>
            <v-card width="900" class="rounded-xl" color="#000000">
                <v-card-title class="text-h4 px-0 hidden-xs-only">Languages</v-card-title>
                <v-card-title class="text-h6 px-0 hidden-sm-and-up">Languages</v-card-title>
                <v-row>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="JavaScript" icon="mdi-language-javascript" setcolor="#323330"/>
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="TypeScript" icon="mdi-language-typescript" setcolor="#2d79c7" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="NodeJS" icon="mdi-nodejs" setcolor="#80bd01" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="JAVA" icon="mdi-language-java" setcolor="#5382a1" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="HTML5" icon="mdi-language-html5" setcolor="#e34f26" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="CSS3" icon="mdi-language-css3" setcolor="#1572b6" />
                    </v-col>
                </v-row>
                <v-card-title class="text-h4 px-0 hidden-xs-only mt-2">Frameworks & Libraries</v-card-title>
                <v-card-title class="text-h6 px-0 hidden-sm-and-up mt-2">Frameworks & Libraries</v-card-title>
                <v-row>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="VueJS" icon="mdi-vuejs" setcolor="#00c180" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Nuxt" icon="mdi-nuxt" setcolor="#00dc82" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Vuetify" icon="mdi-vuetify" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Bootstrap" icon="mdi-bootstrap" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="React" icon="mdi-react" setcolor="#1697f6" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Sass" icon="mdi-sass" setcolor="#1697f6" />
                    </v-col>
                </v-row>
                <v-card-title class="text-h4 px-0 hidden-xs-only mt-2">Other Tools</v-card-title>
                <v-card-title class="text-h6 px-0 hidden-sm-and-up mt-2">Other Tools</v-card-title>
                <v-row>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="MongoDB" icon="mdi-code-braces" setcolor="#439945" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="MYSQL" icon="mdi-database" setcolor="#e48e00" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Postgresql" icon="mdi-elephant" setcolor="#316092" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="AWS" icon="mdi-aws" setcolor="#203344" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="AWS Bucket" icon="mdi-aws" setcolor="#d64e3f" />
                    </v-col>
                    <v-col xs="6" sm="6" md="4" lg="4" xl="4" class="px-0">
                        <Badge text="Git" icon="mdi-git" setcolor="#1697f6" />
                    </v-col>
                </v-row>
            </v-card>    
        </v-layout>
    </v-container>
</template>

<script>
import Badge from '@/components/Badge.vue';
export default {
    data () {
        return {
        } 
    },
    components: { Badge } 
}
</script>
