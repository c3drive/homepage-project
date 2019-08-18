<template>
  <div>
    <h2>Work</h2>
    <p>{{ msg }}</p>
      <router-link
        v-for="post in posts"
        v-bind:key="post.id"
        v-bind:to="post.title"
        target="_self"
        class="btn"
      >
          {{ post.title}}
      </router-link>
    <work-component
        v-for="post in posts"
        v-bind:key="post.id"
        v-bind:title="post.title"
        v-bind:url="post.url"
        v-bind:giturl="post.giturl"
        v-bind:description="post.description"
        v-bind:technology="post.technology"
    ></work-component>
  </div>
</template>

<script>
import Work from '@/components/work'
export default {
  components: {
    'work-component': Work
  },
  data () {
    return {
      msg: '今まで開発したものです。クリックで詳細が表示されます。',
      posts: [
        {id: 1, title: 'HomePage', url: 'http://selene.himegimi.jp/', giturl: '', description: '個人的な趣味のHPです。Javaからhtmlを出力しレンタルサーバーへアップして公開していました。', technology: 'Java, eclipse, html, javascript, css'},
        {id: 2, title: 'Portfolio', url: 'https://c3drive.github.io/homepage-project/', giturl: 'https://github.com/c3drive/homepage-project', description: 'このサイトです。', technology: 'vue-cli, github, html5, javascript, css'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2::after {
  content: "";
  display: block;
  height: 1px;
  width: 30%;
  background-color: #ccc;
  margin: auto;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 5px 8px;
}
a {
  color: white;
  text-decoration: none;
}
.btn {
  padding: 8px 20px;
  color: black;
  display: inline-block;
  opacity: 0.8;
  border: solid #24292D 1px;
  border-radius: 4px;
  transition: all 1s;
}
.btn:hover {
  opacity: 1;
}
.twitter {
  background-color: #55acee;
}
.github {
  background-color: #24292D;
}

</style>
