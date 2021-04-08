<template>
  <v-app style="background-color: #FFF6A1;">
    <v-main>
      <v-container  style="height:100%;">
      <div class="parent">
      <square 
      v-for="sqr in squares"
      v-bind:id="sqr.id"
      v-bind:color="sqr.color"
      v-bind:number="sqr.number"
      :key="sqr.id"
      v-on:changecolor="handleChangeColor"
      >
      </square>
      </div>
      </v-container>
    </v-main>
  </v-app>
</template>

<style>
.parent {
    height:100%;
    width:100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
   }

</style>

<script>
import Square from './components/Square';

export default {
  name: 'App',

  components: {
     Square,
  },

  data () {
     return {
        squares: [
          { id: 1,
            color: "blue",
            number: null,
          },
          { id: 2,
            color: "blue",
            number: null,
          },
          { id: 3,
            color: "blue",
            number: null,
          },
        ]
     }
  },

   methods: {
        handleChangeColor(id) {
          console.log(id);
            for (let i = 0; i < this.squares.length; i++) {

                if(this.squares[i].id === id) {
                    this.squares[i].color = "red";
                }
                else this.squares[i].color = "blue";
            } 
             this.squares[1].number = id;
        }
   }
};
</script>
