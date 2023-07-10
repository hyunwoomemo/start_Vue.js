<template>
  <form action="" v-on:submit.prevent="">
    <div>
      <label for="id">id</label>
      <input type="text" v-model="idValue" id="id">
      {{ idValue }}
    </div>
    <div>
      <label for="pw">passwprd</label>
      <input type="password" v-model="pwValue" id="pw">
      {{ pwValue }}
    </div>
    <button>submit</button>
  </form>
</template>

<script>
export default {
  data: function () {
    return {
      idValue: '',
      pwValue: '',
    }
  },
  methods: {
    handleSubmit: function (e) {
      e.preventDefault();
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
  gap: 1rem;

  > div {
    display: flex;
    gap: 1rem;
  }
}
</style>