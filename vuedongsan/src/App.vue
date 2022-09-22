<template>
  <!-- 모달 -->
  <div class="black-bg" v-if="모달창열림 == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용임</p>
      <button @click="모달창열림 = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a href="#" v-for="(a,i) in 메뉴" :key="i">{{ a }}</a>
  </div>

  <div v-for="(a) in 원룸들" :key="a.id">
    <img :src='a.image' class="roomImg">
    <h4 @click="모달창열림 = true">{{a.title}}</h4>
    <p>{{a.content}}</p>
    <p>{{a.price}} 원</p>
  </div>
</template>

<script>
import data  from '../src/data.js'; 

export default {
  name: 'App',
  data() {
    return {
      원룸들: data,
      모달창열림 : false,
      신고 : [0, 0, 0],
      메뉴 : ['HOME', 'SHOP', "ABOUT"],
      products: ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  methods : {
    increase() {
      this.신고++;
      console.log(this.신고)
    }
  },
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
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.black-bg{
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg{
  width: 100%;
  background: #fff;
  border-radius: 8px;
  padding: 20px;
}

.menu {
  background: rgb(61, 97, 165);;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: #fff;
  padding: 10px;
  text-decoration: none;
}
.roomImg{
  width: 1020px;
  margin-top: 40px;
}
</style>
