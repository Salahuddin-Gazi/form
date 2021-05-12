<template>
  <div>
    <div>
      <h4 class="subheading grey--text ma-5">Dashboard</h4>
    </div>
    <v-container class="ma-5">
      <v-layout row wrap>
        <v-flex xs12 md8>
          <v-row>
            <v-expansion-panels accordion>
              <v-expansion-panel v-for="prop in property" :key="prop.title">
                <v-expansion-panel-header>{{
                  prop.title
                }}</v-expansion-panel-header>
                <v-expansion-panel-content>{{
                  prop.content
                }}</v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-row>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      property: [
        {
          title: "About Us",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod repellat saepe, autem consequuntur placeat quaerat sequi officiis facere quasi, itaque tenetur eum laborum repellendus, tempore ducimus. Blanditiis unde saepe ipsa.",
        },
        {
          title: "Contact Us",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod repellat saepe, autem consequuntur placeat quaerat sequi officiis facere quasi, itaque tenetur eum laborum repellendus, tempore ducimus. Blanditiis unde saepe ipsa.",
        },
      ],
    };
  },
};
</script>
