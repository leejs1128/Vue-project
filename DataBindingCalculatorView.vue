<template>
  <div id="container">
    <header id="header">
      <span class="accent">
        <h1>
          <p>{{ ans }}</p>
        </h1></span
      >
    </header>
    <div id="grid">
      <button type="button" class="boxAC" @click="AC(set)">
        <h1>AC</h1>
      </button>
      <button type="button" class="boxPnm" @click="pnm()">
        <h1>+/-</h1>
      </button>
      <button type="button" class="boxpcnt" @click="pcnt()">
        <h1>%</h1>
      </button>
      <button type="button" class="boxdivied" @click="divied()">
        <h1>÷</h1>
      </button>
      <button type="button" class="box7" @click="attachNumber(7)">
        <h1>7</h1>
      </button>
      <button type="button" class="box8" @click="attachNumber(8)">
        <h1>8</h1>
      </button>
      <button type="button" class="box9" @click="attachNumber(9)">
        <h1>9</h1>
      </button>
      <button type="button" class="boxX" @click="multiply()">
        <h1>X</h1>
      </button>
      <button type="button" class="box4" @click="attachNumber(4)">
        <h1>4</h1>
      </button>
      <button type="button" class="box5" @click="attachNumber(5)">
        <h1>5</h1>
      </button>
      <button type="button" class="box6" @click="attachNumber(6)">
        <h1>6</h1>
      </button>
      <button type="button" class="boxminus" @click="minus()">
        <h1>-</h1>
      </button>
      <button type="button" class="box1" @click="attachNumber(1)">
        <h1>1</h1>
      </button>
      <button type="button" class="box2" @click="attachNumber(2)">
        <h1>2</h1>
      </button>
      <button type="button" class="box3" @click="attachNumber(3)">
        <h1>3</h1>
      </button>
      <button type="button" class="boxPlus" @click="plus()">
        <h1>+</h1>
      </button>
      <button type="button" class="box0" @click="attachNumber(0)">
        <h1>0</h1>
      </button>
      <button type="button" class="boxdot" @click="dot()">
        <h1>.</h1>
      </button>
      <button type="button" class="boxanswer" @click="calculate()">
        <h1>=</h1>
      </button>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      ans: 0,
      beforeValue: 0,
      op: '',
      beforeOp: false,
      afterOp: false
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    attachNumber(number) {
      if (this.beforeOp) {
        this.ans = 0
        this.beforeOp = false
      }
      console.log('click')
      const val = this.ans.toString() + number.toString()
      this.ans = Number.parseFloat(val)
    },
    dot() {
      console.log('.')
      const val = this.ans.toString() + '.'
      this.ans = val
    },
    pcnt() {
      console.log('%')
      const val = this.ans.toString() / 100
      this.ans = val
    },
    pnm() {
      console.log('plus n minus')
      this.ans *= -1
    },
    AC() {
      console.log('clear')
      this.beforeValue = this.ans
      this.ans = 0
    },
    plus() {
      console.log('plus')
      this.calculate()
      this.beforeValue = this.ans
      this.beforeOp = true
      this.op = 'plus'
    },
    minus() {
      console.log('minus')
      this.calculate()
      this.beforeValue = this.ans
      this.beforeOp = true
      this.op = 'minus'
    },
    multiply() {
      console.log('multiply')
      this.calculate()
      this.beforeValue = this.ans
      this.beforeOp = true
      this.op = 'multiply'
    },
    divied() {
      console.log('divied')
      this.calculate()
      this.beforeValue = this.ans
      this.beforeOp = true
      this.op = 'divied'
    },
    calculate() {
      console.log('answer')
      if (this.op === 'plus') {
        this.ans = Number(this.beforeValue) + Number(this.ans)
      } else if (this.op === 'minus') {
        this.ans = Number(this.beforeValue) - Number(this.ans)
      } else if (this.op === 'multiply') {
        this.ans = Number(this.beforeValue) * Number(this.ans)
      } else if (this.op === 'divied') {
        this.ans = Number(this.beforeValue) / Number(this.ans)
      }
    }
  }
}
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#container {
  width: 463px;
  height: 520px;
  margin: 30px auto;
  border-style: solid;
  border-top-left-radius: 15px;
  border-top-right-radius: 15px;
  border-bottom-left-radius: 15px;
  border-bottom-right-radius: 15px;
}
#header {
  width: 460px;
  height: 120px;
  background-color: rgb(87, 87, 87);
  border-style: solid;
  border-top-left-radius: 13px;
  border-top-right-radius: 13px;
  text-align: right;
  padding: 30px 43px 0 0;
}
.box7 {
  width: 115px;
  height: 81px;
}
.box8 {
  width: 115px;
  height: 81px;
}
.boxAC {
  width: 115px;
  height: 81px;
}
.boxPnm {
  width: 115px;
  height: 81px;
}
.boxpcnt {
  width: 115px;
  height: 81px;
}
.boxdivied {
  width: 115px;
  height: 81px;
  background-color: orange;
  color: white;
}
.box9 {
  width: 115px;
  height: 81px;
}
.boxX {
  width: 115px;
  height: 81px;
  background-color: orange;
  color: white;
}
.box4 {
  width: 115px;
  height: 81px;
}
.box5 {
  width: 115px;
  height: 81px;
}
.box6 {
  width: 115px;
  height: 81px;
}
.boxminus {
  width: 115px;
  height: 81px;
  background-color: orange;
  color: white;
}
.box1 {
  width: 115px;
  height: 81px;
}
.box2 {
  width: 115px;
  height: 81px;
}
.box3 {
  width: 115px;
  height: 81px;
}
.boxPlus {
  width: 115px;
  height: 81px;
  background-color: orange;
  color: white;
}
.box0 {
  width: 230px;
  height: 74px;
  border-bottom-left-radius: 13px;
}
.boxdot {
  width: 115px;
  height: 75px;
}
.boxanswer {
  width: 115px;
  height: 75px;
  background-color: orange;
  color: white;
  border-bottom-right-radius: 13px;
}
.accent {
  color: rgb(255, 255, 255);
}
button {
  align-items: center;
}
.grid {
  width: 500px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, 100px);
}
</style>
