<template>
  <div>
    <input type="text" v-bind:value="userId" readonly/>
    <input type="text" :value="userId" readonly/>
    <br>

    <img :src="imgSrc" alt="" style="width:300px; height: auto;">
    <br>

    <input type="search"  v-model="txt1"/>
    <!-- 빈값이면 true, 아니면 false -->
    <button :disabled="txt1 === ''">조회</button>
  </div>
</template>
<script>

export default{ 
  name: '',
  components:{},
  data(){
    return {
      userId: 'HELLo',
      imgSrc: 'https://contents.sixshop.com/uploadedFiles/56785/blogPost/image_1606197480517.png',
      txt1: '',
    };
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>