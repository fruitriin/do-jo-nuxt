<template>
  <div>index</div>

  <input type="text" v-model="input.username">
  <input type="text" v-model="input.password">

  <p>{{ loginAble() }}</p>
  <button :disabled="!loginAble()" @click="login">ろぐいん！</button>

</template>

<script >
export default {
  data(){
    return {
      input: {
        username: "",
        password: "",
      },
      test: "makimasu"
    }
  },
  methods: {
    loginAble(){
      if(this.input.username !== "user") return false
      if(this.input.password !== "password") return false

      return true

    },
    login(){
      if(this.input.username !== "user") return false
      if(this.input.password !== "password") return false

      this.$router.push("/bbbb")
    }
  }

}

</script>
