<template>
  <div class="person">
    <h2>一辆{{ car.brand }}, 价值{{ car.price }}万</h2>
    <button @click="changePrice">修改汽车价格</button>
  </div>
</template>

<script lang="ts">
export default {
  name: "Person",
};
</script>

<script lang="ts" setup>
import { reactive } from "vue";

//数据
let car = reactive({ brand: "奔驰", price: 100 });

//方法
function changePrice() {
  car.price += 10;
  console.log(car.price);
}
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
