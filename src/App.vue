<template>
  <div id="app">
    <!-- Bootswatch Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary shadow-sm mb-4">
      <div class="container">
        <router-link class="navbar-brand font-weight-bold" :to="{ name: 'HomePage' }">
          <i class="fas fa-cubes mr-2"></i>Nicole Rivera
        </router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarColor01">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarColor01">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'HomePage' }" exact>Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'BlogPage' }">Blog</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'GalleryPage' }">Projects</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'AboutPage' }">About</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'ContactPage' }">Contact</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Main Dynamic Route Viewport -->
    <main class="container">
      <router-view/>
    </main>

    <!-- Footer -->
    <footer class="container text-center text-muted py-4 mt-5 border-top">
      <p class="small mb-0">&copy; 2026 Ella Nicole Rivera. Built with Vue 3 &amp; Vite.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
/* Active link highlighting in Vue Router 4 */
.router-link-exact-active,
.router-link-active {
  font-weight: 700;
  color: #fffde8 !important;
  border-bottom: 2px solid #fffde8;
}

/* Portfolio palette: dark #111123 / light #fffde8 */
body {
  background-color: #fffde8;
  color: #111123;
}
.bg-primary {
  background-color: #111123 !important;
  background-image: none;
}
.text-primary {
  color: #111123 !important;
  background-image: none;
}
.text-white {
  color: #fffde8 !important;
}
.bg-light,
.bg-white {
  background-color: #fffde8 !important;
}
.text-muted {
  color: rgba(17, 17, 35, 0.65) !important;
  background-image: none;
}
.border-top,
.border-bottom,
.border {
  border-color: rgba(17, 17, 35, 0.15) !important;
  background-image: none;
}
.navbar-dark .navbar-brand,
.navbar-dark .navbar-nav .nav-link {
  color: rgba(255, 253, 232, 0.7);
}
.navbar-dark .navbar-brand:hover,
.navbar-dark .navbar-nav .nav-link:hover {
  color: #fffde8;
}
.card {
  background-color: #fffde8;
  border: 1px solid rgba(17, 17, 35, 0.12) !important;
  background-image: none;
}
.card-header {
  border-bottom: 1px solid rgba(17, 17, 35, 0.12);
  background-image: none;
}
.list-group-item {
  background-color: transparent;
  color: #111123;
  border-color: rgba(17, 17, 35, 0.12);
  background-image: none;
}
.btn-primary {
  background-color: #111123;
  border-color: #111123;
  color: #fffde8;
  background-image: none;
}
.btn-primary:hover,
.btn-primary:focus {
  background-color: #26264a;
  border-color: #26264a;
  color: #fffde8;
}
.btn-outline-secondary {
  color: #111123;
  border-color: #111123;
}
.btn-outline-secondary:hover {
  background-color: #111123;
  color: #fffde8;
}
.badge-primary,
.badge-secondary,
.badge-info,
.badge-success {
  background-color: #111123;
  color: #fffde8;
  background-image: none;
}
.alert-info,
.alert-success {
  background-color: rgba(17, 17, 35, 0.08);
  border-color: rgba(17, 17, 35, 0.2);
  color: #111123;
  background-image: none;
}
.form-control {
  background-color: #fffde8;
  color: #111123;
  border-color: rgba(17, 17, 35, 0.3);
  background-image: none;
}
.form-control:focus {
  background-color: #fffde8;
  color: #111123;
  border-color: #111123;
  box-shadow: 0 0 0 0.2rem rgba(17, 17, 35, 0.15);
  background-image: none;
}
h1, h2, h3, h4, h5, h6, .h5, .h4, .h3, .h2, .h1 {
  color: #111123;
}
</style>
