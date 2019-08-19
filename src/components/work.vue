<template>
  <div class="work">
      <h3>{{ this.title}}</h3>
      <ul>
          <li>
              <p class="left-field">URL</p>
              <p class="right-field">
                  <a
                    v-bind:href="this.url"
                    target="_blank"
                  >
                  {{ this.url }}
                  </a>
              </p>
          </li>
          <li>
              <p class="left-field">ソースコード</p>
              <p
                v-if="this.giturl.length"
                class="right-field"
              >
                  <a
                    v-bind:href="this.giturl"
                    target="_blank"
                  >
                  {{ this.giturl }}
                  </a>
              </p>
              <p
                v-else
                class="right-field"
              >
                ソースコードは有りません。
              </p>
          </li>
          <li>
              <p class="left-field">説明</p>
              <p class="right-field">
                  {{ this.description }}
              </p>
          </li>
          <li>
              <p class="left-field">使用した主な技術・ツール</p>
              <p class="right-field">
                  {{ this.technology }}
              </p>
          </li>
        </ul>
        <br>
  </div>
</template>

<script>
export default {
  name: 'Work',
  props: [
    'title',
    'url',
    'giturl',
    'description',
    'technology'
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
    clear: both;
}
h3::after {
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
    display: list-item;
    margin: 8px 16px;
    text-align: left;
}
li::after {
    content: "";
    display: block;
    clear: both;
    border-bottom: solid #ccc 1px;
}
a {
    color: black;
}
.work {
    width:70%;
    margin: 0 auto;
}
li .left-field {
    float: left;
    width: 40%;
}
li .right-field {
    float: right;
    width: 60%;
}
</style>
