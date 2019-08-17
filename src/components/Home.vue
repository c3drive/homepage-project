<template>
  <div>
    <div class="top-wrapper">
      <div class="container">
        <h1>{{ title }}</h1>
        <p>{{ msg }}</p>
      </div>
      <div class="container">
        <items-component></items-component>
      </div>
    </div>
    <div class="container">
      <h2>Contact</h2>
      <ul>
        <li>
          {{ mail }}
        </li>
        <li>
          <a
            href="https://twitter.com/c3drive"
            target="_blank"
            class="btn twitter"
          >
          <span class="fab fa-twitter"></span>
          twitter
          </a>
        </li>
        <li>
          <a
            href="https://github.com/c3drive"
            target="_blank"
            class="btn github"
          >
          <span class="fab fa-github-alt"></span>
          GitHub
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Items from '@/components/Items'
export default {
  components: {
    'items-component': Items
  },
  name: 'Home',
  data () {
    return {
      title: 'Yuko Kanai\'s portfolio',
      msg: 'wellcome',
      mail: 'c3drive@gmail.com'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
  font-size: 60px;
}
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
header {
  height: 58px;
  width: 100%;
  background-color: rgba(14, 21, 22, 0.9);
  z-index: 1;
}
.container {
  padding: 0 15px;
  margin:0 auto;
}
.top-wrapper {
  padding: 100px 0 50px 0;
  background-image: url("../assets/keyboard-2308477_1920.jpg");
  background-size: cover;
  color: white;
  border-bottom: 2px solid #dee7ec;
}
.top-wrapper h1 {
  opacity: 0.8;
  font-size: 45px;
  letter-spacing: 3px;
}
.top-wrapper p {
  opacity:0.8;
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
