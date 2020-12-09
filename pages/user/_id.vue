<template>
  <div class="actual-body">
    <section class="hero">
      <div class="hero-body">
        <div class="container profile">
          <div class="avatar">
            <img alt="user-avatar" draggable="false" src="https://cdn.discordapp.com/avatars/455641453994180618/625ca2959f0fc15fc5cc5fb480eb35c1.png?size=512" class="lazyLoad isLoaded">
          </div>
          <h1 class="title">{{ $route.params.id }}</h1>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  fetch({ redirect, route}) {
    if (!route.params.id)
      redirect('/')
  },
  asyncData({ route }) {
    // TODO: add logic for showing the user based on Id Or Username
  }
}
</script>
