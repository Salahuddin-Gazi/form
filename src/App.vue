<template>
  <v-app app>
    <v-container>
      <Navbar />
    </v-container>
    <br />
    <v-container>
      <router-view />
    </v-container>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar";
export default {
  name: "App",
  components: { Navbar },

  data: () => ({
    //
  }),
};
</script>
