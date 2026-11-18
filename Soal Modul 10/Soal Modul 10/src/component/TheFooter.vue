<template>
  <footer class="py-4 mt-5 profile-footer">
    <div class="container">
      <p class="mb-1">© {{ year }} Bryan Fitur Ayni</p>
      <a href="https://github.com/fiturbra438-ar" target="_blank" rel="noreferrer">
        GitHub
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return { year: new Date().getFullYear() };
  },
};
</script>

<style scoped>
.profile-footer {
  color: #65666a;
  border-top: 1px solid #e8e7e4;
}

.profile-footer a {
  color: #292a2c;
  text-decoration: none;
}

.profile-footer a:hover {
  text-decoration: underline;
}
</style>