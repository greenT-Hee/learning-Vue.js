<template>
  <h1>쀼동산</h1>
  <div class="menu">
    <a href="#" v-for="(a,i) in 메뉴" :key="i">{{ a }}</a>
  </div>
  <!-- <div v-for="(a, i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>90 만원</p>
  </div> -->
  <div>
    <h4>{{products[0]}}</h4>
    <p>50 만원</p>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>50 만원</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>50 만원</p>
  </div>
</template>

<script>

export default {
  data() {
    return {
      메뉴 : ['HOME', 'SHOP', "ABOUT"],
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: rgb(49, 175, 127);;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: #fff;
  padding: 10px;
  text-decoration: none;
}
</style>
