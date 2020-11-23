<template>
<!-- <div></div> -->
      <b-navbar toggleable type="dark" variant="dark">
      <b-navbar-brand href="#">NavBar</b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
      <template #default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
        <b-icon v-else icon="chevron-bar-down"></b-icon>
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="/about">About</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>


    export default {
 
    }
</script>

<style lang="scss" scoped>
.navbar{
    background-color: #EE7B00!important;
}

.navbar-brand{
    color:white!important;
}

.nav-link{
    color:white!important;
}

.navbar-toggler{
    background-color: #FFF!important;
}
</style>