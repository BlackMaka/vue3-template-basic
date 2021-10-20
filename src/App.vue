<template>
  <div>
    <MyBtn />
    <MyBtn>
      Banana
    </MyBtn>
    
    <MyBtn>
      <!-- <template v-slot:name> -->
      <template #name>
        <span>Banana</span>
      </template>
      <!-- <template v-slot:icon> -->
      <template #icon>
        <span>(B)</span>
      </template>
    </MyBtn>
  </div>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
  components:{
    MyBtn
  },
}
</script>

<style  >
  
</style>