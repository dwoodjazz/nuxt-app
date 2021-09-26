<template>
  <!-- <Tutorial/> -->
  <div>
    <h1>Sam was here</h1>
    <button class="butt2" @click="count-=7">-</button>
    {{count}}
    <button class="butt1" @click="increment">+</button>

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
