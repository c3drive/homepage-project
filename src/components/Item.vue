<template>
  <router-link
    v-bind:to="this.link"
    target="_self"
    class="btn section"
  >
    <p class="caption">
      <span v-bind:class="this.icon"></span>
      {{ this.title }}
    </p>
  </router-link>
</template>

<script>
export default {
  name: 'Item',
  props: [
    'icon',
    'title',
    'link'
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: white;
  text-decoration: none;
}
.section {
  width: 20%;
  margin: 10px;
  border: 1px solid #dee7ec;
  background-color:rgba(0, 0, 0, 0.3);
}
.section:hover {
  background-color:rgba(255, 255, 255, 0.3);
}
</style>
