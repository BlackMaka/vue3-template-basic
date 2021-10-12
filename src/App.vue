<template>
  <button @click="add">
    ADD
  </button>
  <h1>{{ revesedMessage }}</h1>
  <h1>{{ revesedMessage }}</h1>
  <h1>{{ revesedMessage }}</h1>
</template>

<script>
export default {
  data(){
    return {
      //getter, setter
      msg : 'Hello Computed'
    }
  },
  methods:{
    add(){ 
      //getter
      //readonly 읽기 전용이라 바뀌지 않는다. 
      //this.revesedMessage += '!?'
      
      //getter, setter 값이 바뀐다.
      this.revesedMessage2 += '!?'
    }
  },
  computed:{
    revesedMessage(){
      return this.msg.split('').reverse().join('');
    },
    //getter, setter
    revesedMessage2:{
      get(){
        return this.msg.split('').reverse().join('');
      },
      set(value){
        this.msg = value;
      }
    }
  }
}
</script>

<style>

</style>