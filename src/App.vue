<script setup></script>

<template>
  <!-- <Greet name="rooney" nick-mame="shlc" />
  <Greet name="thhs" nickName="esther" />
  <Greet :name="name" :nickName="channel" /> -->

  <Article id="art" title="article title" :likes="50" :isPublished="true" />
</template>

<script>
import Greet from './components/Greet.vue'
import Article from './components/Article.vue'

export default {
  name: 'App',
  setup() {
    return {}
  },
  methods: {},
  components: {
    Greet,
    Article
  },
  data() {
    return {
      name: 'asdf',
      channel: 'Code'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.sold-out {
  color: red;
}
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
