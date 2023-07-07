<template>
    <v-container class="pa-0" width="180">
        <v-btn x-large rounded :color="setcolor" :width="getWidth" height="60" class="zoom px-3">
                <v-icon class="text-left" left :large="getIconSize">
                    {{ icon }}
                </v-icon>
                <span class="hidden-xs-only">{{ text }}</span>
                <span class="text-caption hidden-sm-and-up ml-n2">{{ text }}</span>
        </v-btn>
    </v-container>
</template>

<script>
export default {
   computed:{
    getWidth(){
        return this.$vuetify.breakpoint.xs ? 100 : 170;
    },
    getHeight(){
        return this.$vuetify.breakpoint.xs ? 30 : 60;
    },
    getIconSize(){
        return this.$vuetify.breakpoint.xs ? false : true;
    }
   }, 
   props: ["text","icon","setcolor"] 
}
</script>

<style>
.zoom{
    transition: 1.0s;
}
.zoom:hover{
	transform: scale(1.1);
	z-index: 2;
	box-shadow: 2px 2px 2px #000;
}
</style>