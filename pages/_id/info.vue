<template>
  <div>
    <h3>User #{{ id }} info</h3>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        id: this.$route.params.id
      }
    }
  }
</script>