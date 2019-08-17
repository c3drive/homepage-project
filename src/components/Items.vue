<template>
  <div>
    <div class="items">
        <item-component
            v-for="post in posts"
            v-bind:key="post.id"
            v-bind:icon="post.icon"
            v-bind:title="post.title"
        ></item-component>
    </div>
  </div>
</template>

<script>
import Item from '@/components/parts/Item'
export default {
  components: {
    'item-component': Item
  },
  data () {
    return {
      posts: [
        {id: 1, title: 'Work', icon: 'fas fa-images'},
        {id: 2, title: 'Skill', icon: 'fas fa-list-ul'},
        {id: 3, title: 'About', icon: 'fas fa-user'},
        {id: 4, title: 'Contact', icon: 'fas fa-envelope'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.items {
  padding: 10px 0;
}
</style>
