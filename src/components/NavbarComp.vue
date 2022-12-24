<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>

  <nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">AMS</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
          <a class="nav-link" href="#">Feature 1</a>
          <a class="nav-link" href="#">Feature 2</a>
        </div>
      </div>
    </div>
    <form class="container-fluid justify-content-end">
      <button class="btn btn-outline-info me-2" type="button">Logout</button>
    </form>
  </nav>

</template>

<style scoped>
</style>
