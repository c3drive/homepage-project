<template>
  <div>
    <h1 class="section-index">Contact</h1>
    <p class="msg">{{ msg }}</p>
    <ul>
    <li>
        {{ mail }}
    </li>
    <li>
        <a
        v-bind:href="this.twitter"
        target="_blank"
        class="btn twitter"
        >
        <span class="fab fa-twitter"></span>
        twitter
        </a>
    </li>
    <li>
        <a
        v-bind:href="this.github"
        target="_blank"
        class="btn github"
        >
        <span class="fab fa-github-alt"></span>
        GitHub
        </a>
    </li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'SNSかメールでお気軽にご連絡ください',
      mail: 'c3drive@gmail.com',
      twitter: 'https://twitter.com/c3drive',
      github: 'https://github.com/c3drive'
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.twitter {
  background-color: #55acee;
}
.github {
  background-color: #24292D;
}
</style>
