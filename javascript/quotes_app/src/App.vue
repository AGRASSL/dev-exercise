<template>
<div class="container">
  <Header title="Quote...Unquote!" />
  <ul>
    <li v-for="quote in quotes" :key="quote.quote">
      {{quote.quote}}
    </li>
  </ul>
</div>
</template>

<script>
import Header from './components/Header.vue'
import quoteData from "./quotes.json"

export default {
  name: 'App',
  components: {
    Header
  },
  data() {
    return {
      quotes: quoteData,
    };
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
