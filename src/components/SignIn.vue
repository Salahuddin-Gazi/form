<template>
  <v-dialog max-width="600px" v-model="dialog">
    <template v-slot:activator="{ on }">
      <v-btn depressed class="mx-2" v-on="on">
        <span>Sign In</span>
        <v-icon right>mdi-account-key</v-icon>
      </v-btn>
    </template>

    <!-- <template v-slot:default="dialog"> -->

    <v-card class="px-2 grey lighten-4">
      <v-card-title>Sign Up</v-card-title>
      <v-card-text>
        <v-form class="pa-2" ref="form">
          <v-text-field
            v-model="email"
            label="Email"
            :rules="emailRules"
          ></v-text-field>
          <v-text-field
            v-model="password"
            label="Password"
            :rules="passRules"
          ></v-text-field>
          <v-btn depressed class="success mt-3" @click="submit">
            Submit
          </v-btn>
        </v-form>
      </v-card-text>
      <!-- <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="primary" text @click="dialog.value = false">
            I accept
          </v-btn>
        </v-card-actions> -->
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      emailRules: [
        (v) => {
          if (v.length >= 3) {
            const patt = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
            return patt.test(v) || "E-mail must be valid";
          } else {
            return "E-mail must be valid";
          }
        },
      ],
      password: "",
      passRules: [(v) => v.length >= 8 || "Minimum password length is 8"],
      dialog: false,
    };
  },
  methods: {
    submit() {
      if (this.$refs.form.validate()) {
        console.log(this.email, this.password);
        this.dialog = false;
        this.$refs.form.resetValidation();
        this.email = "";
        this.password = "";
        // this.$refs.form.reset();
      }
    },
  },
};
</script>
