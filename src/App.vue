<template>
  <div id="app">
    <div>@_{{ user.username }}-{{ fullname }}</div>
    <div>
      <strong>Followers: {{ followers }}</strong>
    </div>
    <button>Follow</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: "Adejam",
        firstname: "Adeleye",
        lastname: "Jamiu",
        email: "oluwaloseyifunmiadeleye1@gmail.com",
        isAdmin: true,
      },
    };
  },
  computed: {
    fullname() {
      return `${this.user.firstname} ${this.user.lastname}`;
    },
  },
  methods: {
    followUsers() {
      this.followers += 1;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
