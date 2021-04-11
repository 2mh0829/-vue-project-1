<template>

  <div class="black-bg" v-if="modalStatue">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="modalStatue = false">닫기</button>
    </div>
  </div>


  <div class="menu">
    <a v-for="(a,b) in 메뉴들" :key="b">{{a}}</a>

  </div>

  <div v-for="(a,i) in data" :key="i">
    <img :src="data[i].image" class="room-img">
    <h4>{{data[i].title}}</h4>
    <p>{{data[i].price}} 원</p>
  </div>

</template>

<script>

import data from './assets/data.js';

export default {
  name: 'App',
  data(){
    return { // 데이터 보관함
      data : data,
      modalStatue : false,
      신고수 : [0,0,0],
      메뉴들 : ['Home', 'Shop', 'About'],
      product : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      price: ['50', '60', '70']
    }
  },
  methods:{
    
  },
  components: {
  }
}
</script>

<style>
body {
  margin: 0;
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}


.room-img {
  width: 100%;
  margin-top: 40px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}

</style>
