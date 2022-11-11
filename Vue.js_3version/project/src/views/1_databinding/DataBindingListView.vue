<template>
  <div>
    <select name="" id="">
      <option value="">선택해주세요</option>
      <option :value="city.code" :key="city.code" v-for="city in cities">
        {{city.title}}
      </option>
    </select>
    <br>

    <table style="margin: 100px auto 0">
      <thead>
        <tr>
          <th>제품번호</th>
          <th>제품명</th>
          <th>가격</th>
          <th>주문수량</th>
          <th>합계</th>
        </tr>
      </thead>
      <tbody>
        <!-- <tr v-for="{drink, idx} in drinkList" :key="idx"></tr> -->
        <tr  v-for="drink in drinkList" :key="drink.drinkId">
          <td>{{ drink.drinkId }}</td>
          <td>{{ drink.drinkName }}</td>
          <td>{{ drink.price }}</td>
          <td><input type="text"  v-model="drink.qty" /></td>
          <td>{{ drink.price * drink.qty }}</td>
        </tr>
      </tbody>
    </table>
  </div>


</template>
<script>

export default{ 
  data(){
    return {
      cities: [
        {title: '서울', code: '02'},
        {title: '부산', code: '051'},
        {title: '제주', code: '064'},
      ], 
      drinkList: [
        {
          drinkId: '1',
          drinkName:'코카콜라',
          price: '1200',
          qty: '1',
        },
        {
          drinkId: '1',
          drinkName:'펩시라임제로',
          price: '1000',
          qty: '1',
        },
        {
          drinkId: '1',
          drinkName:'나랑드사이다',
          price: '800',
          qty: '1',
        },
        {
          drinkId: '1',
          drinkName:'아이스아메리카노',
          price: '2000',
          qty: '1',
        }
      ]

    };
  },
  setup(){},
  created(){},
  mounted(){},
  unmounted(){},
  methods:{}
}
</script>