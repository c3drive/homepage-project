<template>
  <div>
    <div class="top-wrapper">
      <div class="container">
        <h1>{{ title }}</h1>
        <p>{{ msg }}</p>
      </div>
    </div>
    <div>
      <div class="section-item">
        <ul>
          <li>
            <a
              href="https://vuejs.org"
              target="_blank"
            >
              Home
            </a>
          </li>
          <li>
            <a
              href="https://forum.vuejs.org"
              target="_blank"
            >
              Profile
            </a>
          </li>
          <li>
            <a
              href="https://chat.vuejs.org"
              target="_blank"
            >
              Works
            </a>
          </li>
          <li>
            <a
              href="https://twitter.com/vuejs"
              target="_blank"
            >
              contact
            </a>
          </li>
          <br>
          <li>
            <a
              href="http://vuejs-templates.github.io/webpack/"
              target="_blank"
            >
              Docs for This Template
            </a>
          </li>
        </ul>
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
            <span class="fa fa-twitter"></span>
              twitter
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
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
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
  text-decoration: none;
}
.container {
  padding: 0 15px;
  margin:0 auto;
}
.top-wrapper {
  padding: 180px 0 100px 0;
  background-image: url("../assets/keyboard-2308477_1920.jpg");
  background-size: cover;
  color: white;
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
  padding: 8px 24px;
  color: white;
  display: inline-block;
  opacity: 0.8;
  border-radius: 4px
}
.btn:hover {
  opacity: 1.0;

}
.twitter {
  background-color: #55acee;
}
.section-menu {
  border-bottom: 2px solid #dee7ec;
}
</style>
