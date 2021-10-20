<template>
  <div>
    <MyBtn 
      class="sample"
      style="color:red">
      Banana
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

// scoped 쓰면 적용안됨
<style lang="scss" >
  .sample{
    background-color: orange;
  }
</style>