<template>
  <!-- <Tutorial/> -->
  <div>
    <div class="hero">
    <h1>A simple calculator</h1>
    </div>
  <div class="calculatorBox">
    <div class="unitCostBox"> 
      <div class="unitCostItem costHeader" id="CPU">COST PER UNIT</div>
      <div class="unitCostItem costAmount" id="CPUdisplay" >$175.50</div>
    </div>
    <div class="incrementsBox">
      <h3 class="incTitle"># of units</h3>
      <button class="button2" @click="decrement">-</button>
      <div class="count">
      {{count}}
      </div>
      <button class="button1" @click="increment">+</button>
    </div>
    <div class="totalCostBox">
      <div class="totalCostItem costHeader" id="total">TOTAL COST</div>
      <div class="totalCostItem costAmount" id="totalDisplay">${{(count*175.50).toFixed(2)}}</div>
    </div>
  </div>
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
    },
    decrement() {
      this.count--
    },
    computeTotalCost() {
        count*175.50
    }
  }
}
</script>


<style scoped>
  * {
  display: inline-block;
  color:blanchedalmond;
  background-color: rgb(37, 36, 36);
  text-align: center;
} 
.hero {
  width: 100%;
  height: 10rem;
}
h1 {
  padding: 2rem 0rem;
}
.calculatorBox {
  display: flexbox;
  width: 100%;
}
.incrementsBox   {
  height: auto;
  margin: 0 2rem 0 2rem;

  /* border-style: solid;
  border-color:hotpink; */
}

.unitCostBox {
  background-color: rgba(109, 245, 200);
  height: auto;
  width: 35%;

  /* border-style: solid;
  border-color:hotpink; */

}
.totalCostBox {
  /* flex-basis: 2fr; */
  background-color: rgb(183, 138, 226);
  height: auto;
  width: 35%;

  /* border-style: solid;
  border-color:hotpink; */
}

#CPU, #CPUdisplay{
  background-color: rgba(109, 245, 200);
}

#total, #totalDisplay  {
  background-color: rgb(183, 138, 226);
}

.incTitle {
  text-align: center;
  color: honeydew;
  width: 100%;
}

  .button1 {
    border-style: solid;
    border-color: honeydew;
    border-radius: 2rem;
    margin: 2rem .2rem 2rem 0rem;
    height: 3rem;
    width: 3rem;
    align-content: center;
    box-shadow: 0px 5px 10px gray;
    
  }
   .count {
    align-content: center;
    width: 3rem;
    color: black;
    background-color: honeydew;

  }
  .button2 {
    border-style: solid;
    border-color: honeydew;
    border-radius: 2rem;
    margin: 2rem .2rem 2rem 2rem;
    height: 3rem;
    width: 3rem;
    box-shadow: 0px 5px 10px gray;
  }

.costHeader {
  color: black;
  font-size: 1rem;
  margin: 1rem;
  height:auto;
  width: auto;
}

.costAmount {
  color: honeydew;
  font-size: 2.5rem;
  margin: 1rem;
  height:auto;
  width: 90%;
}

</style>