<template>
  <v-app>
    <v-main>
      <div class="div-container">
        <v-container fluid>
          <v-layout row-9>
            <v-flex v-for="index in firstRowList" v-bind:key="index">
              <v-card elevation="3" class="card">
                <div class="subtitle">
                  <div class="input">
                    <v-text-field
                      label="Username"
                      type="text"
                      id="username"
                      name="username"
                      v-model="index.username"
                    />
                  </div>
                  <v-text-field
                    label="Email"
                    type="email"
                    id="email"
                    name="email"
                    v-model="index.email"
                  />
                </div>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="add(firstRowList)"
                        color="green"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-plus</v-icon
                      >
                    </template>
                    Add Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="remove(index, firstRowList)"
                        color="red"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-close</v-icon
                      >
                    </template>
                    Remove Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
          <v-layout row-9>
            <v-flex v-for="index in secondRowList" v-bind:key="index">
              <v-card elevation="3" class="card">
                <div class="subtitle">
                  <div class="input">
                    <v-text-field
                      label="Username"
                      type="text"
                      id="username"
                      name="username"
                      v-model="index.username"
                    />
                  </div>
                  <v-text-field
                    label="Email"
                    type="email"
                    id="email"
                    name="email"
                    v-model="index.email"
                  />
                </div>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="add(secondRowList)"
                        color="green"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-plus</v-icon
                      >
                    </template>
                    Add Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="remove(index, secondRowList)"
                        color="red"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-close</v-icon
                      >
                    </template>
                    Remove Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
          <v-layout row-9>
            <v-flex v-for="index in thirdRowList" v-bind:key="index">
              <v-card elevation="3" class="card">
                <div class="subtitle">
                  <div class="input">
                    <v-text-field
                      label="Username"
                      type="text"
                      id="username"
                      name="username"
                      v-model="index.username"
                    />
                  </div>
                  <v-text-field
                    label="Email"
                    type="email"
                    id="email"
                    name="email"
                    v-model="index.email"
                  />
                </div>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="add(thirdRowList)"
                        color="green"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-plus</v-icon
                      >
                    </template>
                    Add Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                  <v-tooltip top>
                    <template v-slot:activator="{ on, attrs }">
                      <v-icon
                        @click="remove(index, thirdRowList)"
                        color="red"
                        large
                        v-bind="attrs"
                        v-on="on"
                        >mdi-close</v-icon
                      >
                    </template>
                    Remove Card
                  </v-tooltip>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </div>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    lg: 12,
    firstRowList: [
      {
        username: "",
        email: "",
      },
    ],
    secondRowList: [
      {
        username: "",
        email: "",
      },
    ],
    thirdRowList: [
      {
        username: "",
        email: "",
      },
    ],
  }),
  methods: {
    add: function (list) {
      if (list.length >= 9) {
        alert("You can't add more than 9 Cards");
        return;
      }
      list.push({
        username: "",
        email: "",
      });
    },
    remove: function (index, list) {
      list.splice(list.indexOf(index), 1);
    },
  },
};
</script>

<style>
.subtitle {
  /* height: 10px; */
  height: 170px;
  padding: 5px 10%;
  align-items: center;
}
.card {
  height: calc(30vh);
  width: 100%;
  margin: 5px 5px;
}
.v-card {
  width: 100%;
  margin: 10px 10px;
}
.div-container {
  background-color: aqua;
  height:100vh;
  overflow: hidden;
}
</style>
