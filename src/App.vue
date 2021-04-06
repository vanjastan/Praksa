<template>
  <v-app style="background-color: #FFF6A1;">
    <v-main>
      <Square/>
    </v-main>
  </v-app>
</template>

<script>
import Square from './components/Square';

export default {
  name: 'App',

  components: {
    Square,
  },

  data: () => ({
    //
  }),
};
</script>
