<template>
  <v-container style="height:100%;">
   <div class="parent">
   <div 
   v-for="sqr in squares"
   v-bind:style="{'background-color':sqr.color}"
   :key="sqr.id"
   class="square">
   </div>
   </div>
  </v-container>
</template>

<style>
   .parent {
    height:100%;
    width:100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
   }
   .square {
     height: 270px;
     width: 270px;
   }

</style>

<script>
  export default {
    name: 'Square',

    data () {
        return {
           squares: [
               {
                   id: 1,
                   color: "blue",
               },
               {
                   id: 2,
                   color: "blue",
               },
               {
                   id: 3,
                   color: "blue",
               },
           ],
        };
    },
  }
</script>