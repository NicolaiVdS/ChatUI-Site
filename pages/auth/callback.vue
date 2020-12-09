<template>
  <div>
    <h1> {{ $route.query}}</h1>
  </div>
</template>
<script>

Object.size = (obj) => {
  let size = false, key;
  for (key in obj) if (obj.hasOwnProperty(key)) size = true;
  return size;
}

export default {
  fetch({redirect, query}) {
    if (!Object.size(query))
      redirect('/')
  },
  asyncData({query}) {
    // TODO: Add logic for logging in
  }
}
</script>
