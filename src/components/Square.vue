<template>
  <v-container>
    <div class="square" 
      v-on:click="changeColor(id)"
      v-bind:style="{'background-color':color}"
      >
      <p class="number">{{number}}</p>
    </div>
  </v-container>
</template>

<style>
   .square {
     height: 270px;
     width: 270px;
   }

   .number {
    font-size: 150px;
    display: flex;
    color: white;
    justify-content: space-around;
   }
</style>

<script>
  export default {
    name: 'Square',

    props: {
            id: Number,
            color: String,
            number: Number,
    },

    methods: {
        changeColor(id) {
            this.$emit("changecolor", id);
        }
    }
  }
</script>