<template>
  <div>
    <div>
      <label>Username: </label>
      <input type="text" v-model="username" />
      <br />
    </div>
    <span>Is the username valid?: {{ usernameOK }}</span>
    <div>
      <label>Password: </label>
      <input type="text" v-model="password" />
      <br />
    </div>
    <span> Does password contain special characters?: {{passwordOK}}</span>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      username: "",
      password: "",
    };
  },
  computed: {
    usernameOK: function () {
      if (this.username.length > 6) {
        return true;
      } else {
        return false;
      }
    },
    passwordOK: function () {
      let specialCharacters = "~!@#$%^&^*().";
      for (let c of specialCharacters) {
        if (this.password.includes(c)) {
          return true;
        }
      } 
          return false;
        }
  },
};
</script>