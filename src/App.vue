<template>
  <h1>영화정보</h1>
  <div v-for="(movie, i) in data" :key="i">
    <h3 class="bg-yellow" :style="textRed">{{ data[i].title }}</h3>
    <p>개봉: {{ data[i].year }}</p>
    <p>장르: {{ data[i].category }}</p>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        foods: ["김밥", "순대", "만두", "떡국"],
        data: [
          {
            title: "노랑",
            year: 2023,
            category: "액션, 드라마",
            textRed: "color: red"
          },
          {
            title: "아쿠아맨과 로스트 킹덤",
            year: 2023,
            category: "액션, 판타지, 어드벤처",
          },
        ]
      }
    }
  }
</script>

<style>
  .bg-yellow {
      background: gold;
      padding: 10px;
    }
</style>
