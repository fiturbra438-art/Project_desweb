<template>
  <nav class="navbar navbar-expand-lg profile-navbar">
    <div class="container">
      <a class="navbar-brand" href="#beranda">Bryan Fitur Ayni</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Buka navigasi"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div id="navbarNav" class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link" href="#beranda">Beranda</a></li>
          <li class="nav-item"><a class="nav-link" href="#biodata">Biodata</a></li>
          <li class="nav-item"><a class="nav-link" href="#pengalaman">Pengalaman</a></li>
          <li class="nav-item"><a class="nav-link" href="#galeri">Galeri</a></li>
          <li class="nav-item"><a class="nav-link" href="#kontak">Kontak</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
.profile-navbar {
  border-bottom: 1px solid #e8e7e4;
  background: #fff;
}

.navbar-brand {
  color: #292a2c;
  font-weight: 650;
}

.nav-link {
  color: #65666a;
}

.nav-link:hover,
.navbar-brand:hover {
  color: #292a2c;
}
</style>