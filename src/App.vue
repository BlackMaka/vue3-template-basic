<template>
  <div>
    <MyBtn>
      <span style="color:red">Apple</span>
    </MyBtn>
    <MyBtn color="royalblue">
      Banana
    </MyBtn>
    <MyBtn
      large
      :color="color">
      Cherry
    </MyBtn>
    <!-- :바인딩 차이점은 숫자로 타입까지 인식가능 -->
    
    <MyBtn>Orange</MyBtn>
  </div>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
  components:{
    MyBtn
  },
  data(){
    return {
      color:'#000'
    }
  }
}
</script>

<style>

</style>