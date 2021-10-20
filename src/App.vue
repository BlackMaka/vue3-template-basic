<template>
  <div>
    <MyBtn 
      @clickEvent="clickMsg"
      @change-msg="inputMsg">
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
  methods:{
    clickMsg(event){
      console.log('click');
      //emit 반환데이터 업승면 undefiend뜬다.
      console.log(event);
    },
    inputMsg(msg){
      console.log(msg);
    }
  }
}
</script>

<style  >
  
</style>