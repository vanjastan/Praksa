<template>
  <v-container style="height:100%;">
   <div class="parent">
   <div 
   v-for="sqr in squares"
   v-bind:style="{'background-color':sqr.color}"
   v-on:click="changeColor(sqr.id)"
   :key="sqr.id"
   class="square"><p class="number">{{sqr.number}}</p>
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

    data () {
        return {
           squares: [
               {
                   id: 1,
                   color: "blue",
                   number: "",
               },
               {
                   id: 2,
                   color: "blue",
                   number: "",
               },
               {
                   id: 3,
                   color: "blue",
                   number: "",
               },
           ],
        };
    },

    methods: {
        changeColor(id) {
            for (let i = 0; i < this.squares.length; i++) {
                if(this.squares[i].id === id) {
                    this.squares[i].color = "red";
                }
                else this.squares[i].color = "blue";
            }

            if(id === 1) {
                this.squares[1].number = "1";
            }
            else if (id === 2) {
                this.squares[1].number = "2";
            }
            else this.squares[1].number = "3";
        }
    }
  }
</script>