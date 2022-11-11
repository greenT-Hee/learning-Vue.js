<template>
  <div>
    <!-- 케밥케이스인경우는 꼭 따옴표로 감싸야함 -->
    <div :class="{'text-red': hasError, 'active': isActive}">클래스 바인딩</div>
    <div :class="class2">클래스 바인딩2</div>
  </div>
</template>
<script>

export default{ 
  name:'',
  components:{},
  data(){
    return{
      isActive: false,
      hasError: true,
      class2: ['active', 'text-red']
    };
  },
  setup(){},
  created(){},
  mounted(){},
  unmounted(){},
  methods:{}
}
</script>
<style scoped>
  .active {
    background: greenyellow;
    font-weight: 900;
  }

  .text-red{
    color: red;
  }
</style>