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
      <div class="div-container">
        <v-container fluid>
          <v-layout row-9>
            <v-flex
              v-for="index in list1"
              v-bind:key="index"
            >
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
                  <v-btn @click="add(list1)" color="success" class="button"
                    >Add</v-btn
                  >
                  <v-spacer></v-spacer>
                </v-card-actions>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn @click="remove(index,list1)" color="error">Remove</v-btn>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
           <v-layout row-9>
            <v-flex
              v-for="index in list2"
              v-bind:key="index"
            >
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
                  <v-btn @click="add(list2)" color="success" class="button"
                    >Add</v-btn
                  >
                  <v-spacer></v-spacer>
                </v-card-actions>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn @click="remove(index,list2)" color="error">Remove</v-btn>
                  <v-spacer></v-spacer>
                </v-card-actions>
              </v-card>
            </v-flex>
          </v-layout>
           <v-layout row-9>
            <v-flex
              v-for="index in list3"
              v-bind:key="index"
            >
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
                  <v-btn @click="add(list3)" color="success" class="button"
                    >Add</v-btn
                  >
                  <v-spacer></v-spacer>
                </v-card-actions>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn @click="remove(index,list3)" color="error">Remove</v-btn>
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
    list1: [
      {
        username: "",
        email: "",
      },
    ],
    list2: [
      {
        username: "",
        email: "",
      },
    ],
    list3: [
      {
        username: "",
        email: "",
      },
    ],
  }),
  methods: {
    add: function (list) {
      if(list.length>=9)
      {
        alert("You can't add more than 9 Cards");
        return;
      }
      list.push({
        username: "",
        email: "",
      });
    },
    remove: function (index,list) {
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
  height: 275px;
  width: 100%;
  margin: 5px 5px;
}
.v-card {
  width: 100%;
  margin: 10px 10px;
}
.div-container {
  background-color: aqua;
}
</style>
