<template>
  <div>
    <!-- v-model: input 값 바꾸면 바로 값이 바뀌어 있음/ console.log 확인 -->
    <input type="text" v-model="userId"/>
    <button @click="myFunction">클릭</button>
    <button @click="changeDate">변경</button>
    <br>

    <input type="text" v-model.number="num1"/> +
    <input type="text" v-model.number="num2"/> =
    <span>{{ num1 + num2 }}</span>
    <br>

    <input type="text" v-model="num3"/> +
    <input type="text" v-model="num4"/> =
    <span>{{ num3 + num4 }}</span>
  </div>
</template>

<script> 
export default { 
  components: {},
  data() {
    return {
      userId: '아이고 졸려라',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0,
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    myFunction () {
      console.log(this.userId)
    },
    changeDate () {
      this.userId = "TAEHEE"
    }
  }
}
</script>