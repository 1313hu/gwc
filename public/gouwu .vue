<template>
  <div>
    <MyHeader title="购物车案例"></MyHeader>
    <div style="margin-top:45px">
      <MyGoods v-for="item in list" :key="item.id" :obj="item"></MyGoods>
    </div>
    <MyFooter></MyFooter>

  </div>
</template>
<script>
import MyFooter from "./components/MyFooter.vue"
import MyGoods from "./components/MyGoods.vue"
import MyHeader from "./components/MyHeader.vue"
export default {
  name: 'ShopcarApp',

  data() {
    return {
      list:[],
      
    };
  },
  
  components: {
    MyHeader,
    MyFooter,
    MyGoods,
  },
 
 created() {
  this.$axios({
    url: "/api/cart"
  }).then(res => {
    console.log(res.data.list);
    this.list = res.data.list;
    
  });
 },
  mounted() {
    
  },

  methods: {
    
  },
};
</script>

<style lang="scss" scoped>

</style>