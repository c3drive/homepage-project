<template>
  <div>
    <h1 class="section-index">About</h1>
    <p class="msg">{{ msg }}</p>
    <div class="container">
      <div class="left-field">
        <img
          src="@/assets/icon.jpeg"
          class="myicon"
        />
        <a
        v-bind:href="this.github"
        target="_blank"
        class="tips"
        >
        <img
          src="@/assets/GitHub-Mark-120px-plus.png"
          class="icon"
        />
        </a>
        <a
        v-bind:href="this.qiita"
        target="_blank"
        class="tips"
        >
        <img
          src="@/assets/qiita-square.png"
          class="icon"
        />
        </a>
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
      msg: '東京在住。転職活動中。趣味は、筋トレと投資、勉強',
      github: 'https://github.com/c3drive',
      qiita: 'https://qiita.com/c3drive',
      profiles: [
        {id: 1, title: '2006年04月：JAVA開発', description: '主に携帯アプリのJava開発。今でも好き。'},
        {id: 2, title: '2010年05月：Webシステム開発・管理', description: '主にPHPでフロントからバックエンドまで開発。要件定義からインフラ構築まで一通り関われ気づけば6年ほどいました。あまりに居心地が良すぎて危機感を覚え転職'},
        {id: 3, title: '2016年11月：WebシステムQA', description: '営業的な立ち回り4割、管理7割。売り上げはかなり伸ばせたのと、スクラム開発のQAとして関われる様になったのはよかった。立場上、自動化を提案できないことにモヤモヤしていたところに売り上げ拡充のためアカウントマネージャーへの転向を求められ拒否し、給与が頭打ちになる。'},
        {id: 4, title: '2019年12月：QAコンサル', description: '外資系Sler。300,400人規模のプロジェクトのテスト推進リーダーやメンバーなど。大規模プロジェクトの経験と外資系を経験したかったので望み通りではある。'},
        {id: 5, title: '◆保有資格◆', description: 'データベーススペシャリスト、応用技術者試験、AWSクラウドプラクティショナー、TOEIC530点、JSTQB'}
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
.myicon {
  display: block;
  border-radius: 50%;
  width: 180px;
  margin: 10px auto;
}
.tips{
  margin: 5px;
  border: 0px;
}
.icon {
  height: 40px;
}
.caption {
  font-size: 1.1em;
  font-weight: bold;
}
.text {
  font-size: 1em;
}

</style>
