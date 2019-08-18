<template>
  <div>
    <h2>Contact</h2>
    <p>{{ msg }}</p>
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
  color: white;
  display: inline-block;
  opacity: 0.8;
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
