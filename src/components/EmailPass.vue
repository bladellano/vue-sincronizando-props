<template>
  <div>
    <form action="">
      <div class="mb-3">
        <label for="" class="form-label">E-mail</label>
        <input
          v-model="localEmail"
          type="text"
          class="form-control"
          name="password"
          id="password"
        />
      </div>
      <div class="mb-3">
        <label for="" class="form-label">Password</label>
        <input
          v-model="localPassword"
          type="password"
          class="form-control"
          name="password"
          id="password"
        />
      </div>
      <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "EmailPass",
  props: {
    email: {
      type: String,
      default: "",
    },
    password: {
      propName: {
        type: String,
        default: "",
      },
    },
  },
  data() {
    return {
      localEmail: "",
      localPassword: "",
    };
  },

  created() {
    // this.localEmail = this.email;
    // this.localPassword = this.password;
  },
  watch: {
    localEmail(val) {
      this.$emit("emailUpdate", val);
    },
    localPassword(val) {
      this.$emit("passwordUpdate", val);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>