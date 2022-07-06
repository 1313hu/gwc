<template>
  <div>
    <h4>1. 动态dynamic组件使用</h4>
    
    <UseDynamic>
    </UseDynamic>
    <UserInfo></UserInfo>
  </div>
</template>

<script>
import UseDynamic from './components/01_UseDynamic.vue'
import UserInfo from './components/UserInfo.vue'
export default {
  name: 'ShopcarApp',
components: {
  UseDynamic,
  UserInfo
},
  data() {
    return {
      
    };
  },

  mounted() {
    
  },

  methods: {
    
  },
};
</script>

<style lang="scss" scoped>

</style>