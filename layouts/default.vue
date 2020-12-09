<template>
  <div>
    <b-navbar :transparent="true" :fixed-top="true" :wrapper-class="'container'">
      <template slot="brand">
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img src="https://raw.githubusercontent.com/buefy/buefy/dev/static/img/buefy-logo.png" alt="logo">
        </b-navbar-item>
      </template>

      <template slot="start">
        <b-navbar-item tag="router-link" :to="{ path: '/' }">Features</b-navbar-item>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">Guide</b-navbar-item>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">Changelog</b-navbar-item>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">Streamers</b-navbar-item>
        <b-navbar-item tag="router-link" :to="{ path: '/user/1' }">Users</b-navbar-item>
      </template>

<!--      TODO: Make language select dynamic -> selecte Language must be the lable and not in the list-->
      <template slot="end">
        <b-navbar-dropdown :hoverable="true" label="Language">
          <b-navbar-item href="#">English</b-navbar-item>
          <b-navbar-item href="#">Nederlands</b-navbar-item>
        </b-navbar-dropdown>

        <b-navbar-item><b-icon pack="fas" icon="sun"></b-icon></b-navbar-item>
        <b-navbar-item tag="router-link" :to="{ path: '/login'}">
          <span>Login</span>
          <b-icon pack="fas" icon="sign-in-alt" size="is-small" custom-class="ml-2"></b-icon>
        </b-navbar-item>

      </template>
    </b-navbar>

    <nuxt />
  </div>
</template>

<script>
export default {}
</script>
