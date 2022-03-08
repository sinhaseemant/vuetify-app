<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn class="mx-2" fab dark small color="primary">
        <v-icon dark> mdi-heart </v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-layout row wrap>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
        </v-layout>
        <v-layout row wrap>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
        </v-layout>
        <v-layout row wrap>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
          <v-flex lg-6 md-6>
            <InputCard />
          </v-flex>
        </v-layout>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import InputCard from "./components/Input-Card.vue";

export default {
  name: "App",
  components: {
    InputCard,
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.card {
  background-color: #ecf0f1;
  border-radius: 4px;
  margin: 0 auto;
  padding: 0 20px 20px;
  width: 360px;
  margin-top: 20px;
}
input {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 1em;
  padding: 10px;
  margin: 10px 5px;
  border: 0;
  border-bottom: 1px solid #757575;
}
button {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 1em;
  padding: 10px;
  margin: 10px 5px;
  border: 0;
  border-radius: 3px;
  background-color: #3498db;
  color: #ecf0f1;
}
#remove {
  background-color: #e74c3c;
} */
</style>
