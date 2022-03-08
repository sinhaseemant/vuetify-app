<template>
  <!-- <v-container>
    <center> -->
  <div>
    <v-card v-for="index in list" v-bind:key="index" elevation="3" class="card">
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
        <v-btn @click="add()" color="success">Add</v-btn>
        <v-spacer></v-spacer>
        <v-btn @click="remove(index)" color="error">Remove</v-btn>
        <v-spacer></v-spacer>
      </v-card-actions>

      <!-- <p v-for="user in list" v-bind:key="user" ref="user">
      UserName: {{ user.username }} <br />
      Email: {{ user.email }}
    </p>  -->
    </v-card>
  </div>
  <!-- </center>
  </v-container> -->
</template>

<script>
export default {
  name: "InputCard",
  data() {
    return {
      list: [
        {
          username: "",
          email: "",
        },
      ],
    };
  },

  methods: {
    add: function () {
      this.list.push({
        username: "",
        email: "",
      });
    },
    remove: function (index) {
      this.list.splice(this.list.indexOf(index), 1);
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
  height: 230px;
  width: 100%;
  margin: 5px 5px;
}
.v-card {
  width: 100%;
  margin: 10px 10px;
}
</style>