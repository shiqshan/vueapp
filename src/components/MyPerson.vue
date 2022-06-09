<template>
  <div class="app-school">
    <h1>{{ msg }}</h1>
    <h1>props传过来的数字是： {{ myNum }}</h1>
    <button @click="addNum">加一下</button>
    <div class="demo1">学校是：{{ school ? school.name : name }}</div>
    <div class="demo2">地址是：{{ school ? school.address : address }}</div>
  </div>

</template>

<script>
export default {
  name: "MyPerson",
  data() {
    return {
      msg: '一个学校信息',
      myNum: this.num || 0
    }
  },
  props: ['name', 'address', 'school', 'num'],
  methods: {
    addNum() {
      this.myNum++
    }
  }
}
</script>

<style scoped>
.app-school {
  width: 500px;
  padding: 20px;
  border: 1px solid #323232;
  border-radius: 2px;
}

.demo1 {
  font-size: 20px;
  font-weight: bold;
  color: pink;
}

.demo2 {
  font-size: 20px;
  font-weight: bold;
  color: dodgerblue;
}
</style>