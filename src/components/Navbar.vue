<template>
  <!-- <nav class="ma-2"> -->
  <v-app-bar flat app class="grey lighten-4">
    <v-btn depressed router :to="dashboard">
      <span class="red white--text">FO</span>
      <span class="white red--text">RM</span>
    </v-btn>

    <v-spacer></v-spacer>
    <v-btn
      depressed
      class="blue white--text lighten-3 px-2 mx-2"
      router
      :to="explore"
      >Explore</v-btn
    >
    <SignIn />
    <SignUp />
  </v-app-bar>
  <!-- </nav> -->
</template>

<script>
import SignIn from "./SignIn";
import SignUp from "./SignUp.vue";
export default {
  name: "Navbar",
  components: { SignIn, SignUp },

  data() {
    return {
      dashboard: "/",
      explore: "/explore",
    };
  },
};
</script>
