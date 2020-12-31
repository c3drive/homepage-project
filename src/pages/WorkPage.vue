<template>
  <div>
    <h1 class="section-index">Work</h1>
    <p class="msg">{{ msg }}</p>
    <div class="workarea">
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
        {id: 2, title: 'Portfolio', url: 'https://c3drive.github.io/homepage-project/dist/', giturl: 'https://github.com/c3drive/homepage-project', description: 'このサイトです。Qiitaにアウトプットしつつ環境構築から開発を行いました。', technology: 'vue-cli, gitHub, html5, javascript, css'},
        {id: 3, title: 'Docker勉強', url: 'https://c3drive-product-register.herokuapp.com/', giturl: 'https://github.com/c3drive/my_product-register', description: 'おそらくRailsで良く見る画面（登録と参照と削除ができるやつ）。Railsの勉強はしておらず、Dockerを使った開発・テスト・本番（Herokuデプロイ）を一通り行うためのサイト。構成はWeb/DBの簡単なものですが、こちらもdocker-composeで複数のコンテナを立てることが目的', technology: 'Docker, docker-compose, gitHub, AWS（EC2にアップできることを確認しましたが最終的には利用していません）, Ruby on Rails , TravisCI, Heroku'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
