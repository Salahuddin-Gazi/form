<template>
  <div>
    <h4 class="subheading grey--text">Explore</h4>
    <v-container class="ma-5">
      <v-layout row wrap>
        <v-flex xs12 md8>
          <v-row>
            <div v-for="prop in property" :key="prop.title">
              <div>
                <h1>{{ prop.title }}</h1>
              </div>
              <div>
                <p>{{ prop.content }}</p>
              </div>
            </div>
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
