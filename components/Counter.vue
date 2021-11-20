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

    <div class="hero">
      <h1>A simple input</h1>
    </div>
    <div class="simpleInput">
      <div class="inputBox">
        <label for="zipCode">Type your zip code here</label>
        <input type="text" id="zipEntry" name="zip" value="83814" required
       minlength="5" maxlength="5" size="10">
      </div>

      <div class="stateBox">
        <div class="state">STATE</div>
        <div id="stateResult" >{{zipToState(zipcode)}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 10,
      zipcode: document.getElementById("zipEntry"),
      // zipcode: 56554
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
    },
    zipToState(zipcode) {
          /* Zipcode cases alphabetized by state */ 
          let st="st";
          let state = "state";
      if (zipcode >= 35000 && zipcode <= 36999) {
          st = 'AL';
          state = 'Alabama';
      } else if (zipcode >= 99500 && zipcode <= 99999) {
          st = 'AK';
          state = 'Alaska';
      } else if (zipcode >= 85000 && zipcode <= 86999) {
          st = 'AZ';
          state = 'Arizona';
      } else if (zipcode >= 71600 && zipcode <= 72999) {
          st = 'AR';
          state = 'Arkansas';
      } else if (zipcode >= 90000 && zipcode <= 96699) {
          st = 'CA';
          state = 'California';
      } else if (zipcode >= 80000 && zipcode <= 81999) {
          st = 'CO';
          state = 'Colorado';
      } else if ((zipcode >= 6000 && zipcode <= 6389) || (zipcode >= 6391 && zipcode <= 6999)) {
          st = 'CT';
          state = 'Connecticut';
      } else if (zipcode >= 19700 && zipcode <= 19999) {
          st = 'DE';
          state = 'Delaware';
      } else if (zipcode >= 32000 && zipcode <= 34999) {
          st = 'FL';
          state = 'Florida';
      } else if ( (zipcode >= 30000 && zipcode <= 31999) || (zipcode >= 39800 && zipcode <= 39999) ) {
          st = 'GA';
          state = 'Georgia';
      } else if (zipcode >= 96700 && zipcode <= 96999) {
          st = 'HI';
          state = 'Hawaii';
      } else if (zipcode >= 83200 && zipcode <= 83999) {
          st = 'ID';
          state = 'Idaho';
      } else if (zipcode >= 60000 && zipcode <= 62999) {
          st = 'IL';
          state = 'Illinois';
      } else if (zipcode >= 46000 && zipcode <= 47999) {
          st = 'IN';
          state = 'Indiana';
      } else if (zipcode >= 50000 && zipcode <= 52999) {
          st = 'IA';
          state = 'Iowa';
      } else if (zipcode >= 66000 && zipcode <= 67999) {
          st = 'KS';
          state = 'Kansas';
      } else if (zipcode >= 40000 && zipcode <= 42999) {
          st = 'KY';
          state = 'Kentucky';
      } else if (zipcode >= 70000 && zipcode <= 71599) {
          st = 'LA';
          state = 'Louisiana';
      } else if (zipcode >= 3900 && zipcode <= 4999) {
          st = 'ME';
          state = 'Maine';
      } else if (zipcode >= 20600 && zipcode <= 21999) {
          st = 'MD';
          state = 'Maryland';
      } else if ((zipcode >= 1000 && zipcode <= 2799) || (zipcode == 5501) || (zipcode == 5544) ){
          st = 'MA';
          state = 'Massachusetts';
      } else if (zipcode >= 48000 && zipcode <= 49999) {
          st = 'MI';
          state = 'Michigan';
      } else if (zipcode >= 55000 && zipcode <= 56899) {
          st = 'MN';
          state = 'Minnesota';
      } else if (zipcode >= 38600 && zipcode <= 39999) {
          st = 'MS';
          state = 'Mississippi';
      } else if (zipcode >= 63000 && zipcode <= 65999) {
          st = 'MO';
          state = 'Missouri';
      } else if (zipcode >= 59000 && zipcode <= 59999) {
          st = 'MT';
          state = 'Montana';
      } else if (zipcode >= 27000 && zipcode <= 28999) {
          st = 'NC';
          state = 'North Carolina';
      } else if (zipcode >= 58000 && zipcode <= 58999) {
          st = 'ND';
          state = 'North Dakota';
      } else if (zipcode >= 68000 && zipcode <= 69999) {
          st = 'NE';
          state = 'Nebraska';
      } else if (zipcode >= 88900 && zipcode <= 89999) {
          st = 'NV';
          state = 'Nevada';
      } else if (zipcode >= 3000 && zipcode <= 3899) {
          st = 'NH';
          state = 'New Hampshire';
      } else if (zipcode >= 7000 && zipcode <= 8999) {
          st = 'NJ';
          state = 'New Jersey';
      } else if (zipcode >= 87000 && zipcode <= 88499) {
          st = 'NM';
          state = 'New Mexico';
      } else if ( (zipcode >= 10000 && zipcode <= 14999) || (zipcode == 6390) || (zipcode == 501) || (zipcode == 544) ) {
          st = 'NY';
          state = 'New York';
      } else if (zipcode >= 43000 && zipcode <= 45999) {
          st = 'OH';
          state = 'Ohio';
      } else if ((zipcode >= 73000 && zipcode <= 73199) || (zipcode >= 73400 && zipcode <= 74999) ) {
          st = 'OK';
          state = 'Oklahoma';
      } else if (zipcode >= 97000 && zipcode <= 97999) {
          st = 'OR';
          state = 'Oregon';
      } else if (zipcode >= 15000 && zipcode <= 19699) {
          st = 'PA';
          state = 'Pennsylvania';
      } else if (zipcode >= 300 && zipcode <= 999) {
          st = 'PR';
          state = 'Puerto Rico';
      } else if (zipcode >= 2800 && zipcode <= 2999) {
          st = 'RI';
          state = 'Rhode Island';
      } else if (zipcode >= 29000 && zipcode <= 29999) {
          st = 'SC';
          state = 'South Carolina';
      } else if (zipcode >= 57000 && zipcode <= 57999) {
          st = 'SD';
          state = 'South Dakota';
      } else if (zipcode >= 37000 && zipcode <= 38599) {
          st = 'TN';
          state = 'Tennessee';
      } else if ( (zipcode >= 75000 && zipcode <= 79999) || (zipcode >= 73301 && zipcode <= 73399) ||  (zipcode >= 88500 && zipcode <= 88599) ) {
          st = 'TX';
          state = 'Texas';
      } else if (zipcode >= 84000 && zipcode <= 84999) {
          st = 'UT';
          state = 'Utah';
      } else if (zipcode >= 5000 && zipcode <= 5999) {
          st = 'VT';
          state = 'Vermont';
      } else if ( (zipcode >= 20100 && zipcode <= 20199) || (zipcode >= 22000 && zipcode <= 24699) || (zipcode == 20598) ) {
          st = 'VA';
          state = 'Virginia';
      } else if ( (zipcode >= 20000 && zipcode <= 20099) || (zipcode >= 20200 && zipcode <= 20599) || (zipcode >= 56900 && zipcode <= 56999) ) {
          st = 'DC';
          state = 'Washington DC';
      } else if (zipcode >= 98000 && zipcode <= 99499) {
          st = 'WA';
          state = 'Washington';
      } else if (zipcode >= 24700 && zipcode <= 26999) {
          st = 'WV';
          state = 'West Virginia';
      } else if (zipcode >= 53000 && zipcode <= 54999) {
          st = 'WI';
          state = 'Wisconsin';
      } else if (zipcode >= 82000 && zipcode <= 83199) {
          st = 'WY';
          state = 'Wyoming';
      } else {
          st = 'none';
          state = 'none';
          console.log('No state found matching', zipcode);
      }

      return st
    }
  }
}
</script>

  <!-- STYLING BLOCK -->

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
  /* <!-- Style for the Second Section of Project --> */
  

.simpleInput {
  display:flex;
  height: 300px;
  width: 100%;
  border-style: solid;
  border-color:darkgreen; 
  align-content: center;
  justify-content: space-around;
}

.inputBox {
  display: flex;
  width: 30%;
  height: 100%;
  flex-basis: 1fr;
  border-style: solid;
  border-color:hotpink; 
  align-items: center;
  justify-content: center;

}

.stateBox {
  display: flex;
  width: 30%;
  height: 100%;
  flex-basis: 1fr;
  border-style: solid;
  border-color:hotpink; 
  align-items: center;
 justify-content: center;
}

#zipEntry {
  border-style: ridge;
  border-color: honeydew;
  height: 2rem;
  margin: 1rem;
}

.state {
  text-align: start;
}
#stateResult {
  font-size: 3rem;
}
</style>