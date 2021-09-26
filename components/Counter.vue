<template>
  <!-- <Tutorial/> -->
  <div>
    <h1>Hello World</h1>
    <button class="butt1" @click="increment">+</button>
    {{count}}
    <button class="butt2" @click="count-=7">-</button>

  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 10
    }
  },
  methods: {
    increment() {
      this.count++
    }
  }
}
</script>


<style scoped>
  .butt1 {
    background-color: aqua;
  }
  .butt2 {
    background: skyblue
  }
</style>
