<template>
  <div>
    <h2>User # {{ this.$route.params.id }}</h2>
    <nuxt-child></nuxt-child>
  </div>
</template>

<script>
  export default {
    validate ({ params }) {
      return /^\d+$/.test(params.id)
    },
    fetch ({ store, redirect, params }) {
      return redirect({name: "id-info", params: params})
    }
  }
</script>