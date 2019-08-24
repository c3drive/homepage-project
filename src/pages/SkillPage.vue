<template>
  <div>
    <h1 class="section-index">Skill</h1>
    <p class="msg">{{ msg }}</p>
    <div class="container">
      <div class="left-field">
      </div>
      <div class="right-field">
        <ul class="items">
          <li
            v-for="profile in profiles"
            v-bind:key="profile.id"
          >
            <p class="caption">{{ profile.title }}</p>
            <p class="text">{{ profile.description }}</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: '立ち上がりははやいです',
      profiles: [
        {id: 1, title: 'PHP', description: 'フレームワークベースのクラス設計から可能。Web、API、バッチ開発の経験あり。'},
        {id: 2, title: 'Java', description: 'Strutsベースでの開発、JavaEE、Servletなど経験、ブランクあり。'},
        {id: 3, title: 'HTML5/CSS3/JavaScript', description: '基本的に問題なし。AJaxは必要最低限。'},
        {id: 4, title: 'PostgreSQL/AmazonRDS/MySQL/Sybase/Oracle', description: '各DBの特徴、必要最低限のコマンド知識。'},
        {id: 5, title: 'Apache/Tomcat/Nginx', description: 'インストール、環境構築、運用が可能。'},
        {id: 6, title: 'Vue.js/Python/Go', description: '学習中。'}
      ]
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  display: list-item;
  text-align: left;
  margin-bottom: 10px;
}
.caption {
  font-size: 1.1em;
  font-weight: bold;
}
.text {
  font-size: 1em;
}

</style>
