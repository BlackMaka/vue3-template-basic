<template>
  <h1 @click="changeMessage">
    {{ msg }}
  </h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data(){
    return{
      msg : 'Hello?'
    }
  },
  computed:{
    reversedMessage(){
      return this.msg.split('').reverse().join('');
    }
  },
  watch:{ 
    //msg 데이터 변경 감시
    msg(newValue, oldValue){
      console.log(newValue); //Good!
      console.log(oldValue); //Hello?
    },
    //계산된 값도 변경이 있으면 감지가 가능하다.
    reversedMessage(newValue, oldValue){
      console.log(newValue); //!dooG
      console.log(oldValue); //?olleH
    }
  },
  methods:{
    changeMessage(){
      this.msg = 'Good!';
    }
  }
}
</script>

<style>

</style>