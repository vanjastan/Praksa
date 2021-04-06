<template>
  <v-container style="height:100%;">
   <div class="parent">
   <div class="square"></div>
   <div class="square"></div>
   <div class="square"></div>
   </div>
   </v-container>
</template>

<style>
.square {
  height: 250px;
  width: 250px;
  background-color: #0D48E0; 
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
  }
</script>