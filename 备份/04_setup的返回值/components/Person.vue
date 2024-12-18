<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年齡：{{ age }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
  </div>
</template>

<script lang="ts">
export default {
  name: "Person",
  setup() {
    //数据
    let name = "张三";
    let age = 18;
    let tel = "100000";

    //方法
    function changeName() {
      name = "zhang-san";
    }
    function changeAge() {
      age += 1;
    }
    function showTel() {
      alert(tel);
    }

    // return { name, age, changeName, changeAge, showTel };
    return () => "哈哈";
  },
};
</script>

<style>
.person {
  background: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}

button {
  margin: 0 20px;
}
</style>
