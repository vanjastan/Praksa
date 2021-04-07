<template>
  <v-container style="height:100%;">
   <div class="parent">
   <div id="1" class="square" v-on:click="select($event)"></div>
   <div id="2" class="square" v-on:click="select($event)"></div>
   <div id="3" class="square" v-on:click="select($event)"></div>
   </div>
   </v-container>
</template>

<style>
.square {
  height: 250px;
  width: 250px;
  background-color: #0D48E0; 
  color: white;
  font-size: 150px;
  text-align: center;
}

.parent {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: space-around; 
    align-items: center;
}

</style>

<script>
  export default {
    name: 'Square',

    data: () => ({
    }),

    methods: {
        select: function(event) {
            var clicked = event.currentTarget.id;
            document.getElementById("2").innerHTML = clicked;
        },
    }
  }
</script>