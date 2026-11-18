<template>
  <form class="contact-form" @submit.prevent="submitForm">
    <div class="mb-3">
      <label for="name" class="form-label">Nama</label>
      <input id="name" v-model.trim="form.name" type="text" class="form-control" autocomplete="name" required />
    </div>
    <div class="mb-3">
      <label for="email" class="form-label">Email</label>
      <input id="email" v-model.trim="form.email" type="email" class="form-control" autocomplete="email" required />
    </div>
    <div class="mb-3">
      <label for="message" class="form-label">Pesan</label>
      <textarea id="message" v-model.trim="form.message" class="form-control" rows="4" required></textarea>
    </div>
    <button type="submit" class="btn btn-outline-dark">Kirim pesan</button>
    <p v-if="submitted" class="text-secondary mt-3 mb-0" role="status">
      Form ini hanya demo dan belum terhubung ke server.
    </p>
  </form>
</template>

<script>
export default {
  data() {
    return {
      form: { name: "", email: "", message: "" },
      submitted: false,
    };
  },
  methods: {
    submitForm() {
      this.submitted = true;
    },
  },
};
</script>

<style scoped>
.contact-form {
  padding: 1.25rem 0;
}

.form-control:focus {
  border-color: #8b8b8b;
  box-shadow: 0 0 0 0.2rem rgb(41 42 44 / 10%);
}
</style>