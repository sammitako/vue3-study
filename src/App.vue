<template>
  <h1 @click="increase">{{ count }}</h1>
  <!-- 디렉티브 -->
  <div v-if="count > 4">4보다 큽니다.</div>
  <ul>
    <!-- <li v-for="fruit in fruits" :key="fruit">{{ fruit }}</li> -->
    <list v-for="fruit in fruits" :key="fruit" :name="fruit">
      {{ fruit }}
    </list>
  </ul>
</template>

<script>
import Fruit from "./components/Fruit.vue";

// this
export default {
  components: {
    list: Fruit,
  },
  // 데이터
  data() {
    return {
      count: 0,
      fruits: ["Apple", "Banana", "Cherry"],
    };
  },
  // 함수
  methods: {
    increase() {
      this.count += 1;
    },
  },
};
</script>

<style lang="scss">
h1 {
  font-size: 50px;
  color: royalblue;
}
ul {
  li {
    font-size: 40px;
  }
}
</style>
