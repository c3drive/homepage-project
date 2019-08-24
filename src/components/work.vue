<template>
<div class="container">
  <a
    v-on:click="show = !show"
    href="#!"
    class="btn workindex"
  >
      {{ this.title}}
  </a>
  <transition
    v-if="show"
    name="slide-fade"
  >
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
  </transition>
  <br>
</div>
</template>

<script>
import vueAccordion from 'vue-accordion'
export default {
  components: {
    'vue-accordion': vueAccordion
  },
  name: 'Work',
  props: [
    'title',
    'url',
    'giturl',
    'description',
    'technology'
  ],
  data () {
    return {
      show: false
    }
  }
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
  height: 0px;
  width: 30%;
  background-color: #ccc;
  margin: auto;
}
li {
    display: list-item;
    padding: 10px 8px;
    text-align: left;
    border-bottom: solid #ccc 1px;
}
li::after {
    content: "";
    display: block;
    clear: both;
}
.workindex {
  display: inline-block;
  width: 20%;
  background-color: #24292D;
}
.work {
    margin: 10px auto;
    padding: 10px;
    border: solid #b0c4de 1px;
}

.work a {
    color: black;
    text-decoration-line: underline;
}
</style>
