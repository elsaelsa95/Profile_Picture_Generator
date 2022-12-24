<script>
export default {
  data() {
    return {
      name: "",
      avatar: "",
    };
  },
  methods: {
    changeAvatar() {
      this.avatar = `https://robohash.org/${this.name}.png`;
    },
  },
};
</script>

<template>
  <section class="py-5">
    <div class="d-flex justify-content-sm-center">
      <div class="container px-4 px-lg-5 mt-5">
        <form v-on:submit.prevent="changeAvatar">
          <div class="mb-3">
            <input
              type="text"
              class="form-control"
              id="name"
              placeholder="Ketik Nama Anda..."
              v-model="name"
            />
          </div>
          <button type="submit" class="btn btn-success">
            Buat Profile Picture!
          </button>
        </form>
        <img :src="avatar" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  background-color: lightblue;
  opacity: 75%;
  margin-top: 30vh;
  margin-right: 10vh;
  padding: 50px;
  border-radius: 30px;
}
</style>
