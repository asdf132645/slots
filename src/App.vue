<template>
  <div>
    <!-- porps -->
    <ul>
      <item-props v-for="itemProps in itemsPropsd" :key="itemProps" :propsdata="itemProps" ></item-props>
    </ul>
    <div> 
      <h1>구분선</h1>  
    </div>
    <!-- 슬롯 -->
    <ul>
      <item-slots>
        <h3 slot="header">헤더</h3>
        아이템 1
      </item-slots>
      <item-slots>
        <h3 slot="header">헤더</h3>
        아이템 2 <button>click</button>
      </item-slots>
      <item-slots>
         <h3 slot="header">헤더</h3>
        <div>
          아이템 3
        </div>
      </item-slots>
      <item-slots>
        <div style="color: blue; font-size:24px;">
          아이템 4
        </div>
         <h3 slot="header">헤더</h3>
      </item-slots>
    </ul>
  </div>
</template>

<script>
import ItemProps from './ItemProps.vue'
import ItemSlots from './ItemSlots.vue'

export default {
  components:{
    ItemProps,
    ItemSlots
  },
  //props 쓰기 위해서 데이터 사용
  data(){
    return {
      itemsPropsd: ['아이템 1','아이템 2','아이템 3','아이템 4','아이템 5']
    }
  }
}

</script>

<style scoped>

</style>