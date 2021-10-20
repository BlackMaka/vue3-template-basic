<template>
  <div>
    <button @click="handler('dd',$event)"></button>
    <button @click="handlerA">
      ()생략가능
    </button>
    <button @click="handlerA(), handlerB()">
      ()를 입력한다
    </button>
  </div>
</template>

<script>
export default {
  methods:{
    handler(msg, event){
      console.log(msg, event);
    },
    handlerA(){
      console.log('A');
    },
    handlerB(){
      console.log('B');
    }
  }
}
</script>

<style>

</style>