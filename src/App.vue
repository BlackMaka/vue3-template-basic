<template>
  <!-- <h1>{{ msg + '??' }}</h1> -->
  
  <!-- 
    로직이 너무 많이 실행된다
  <h1>{{ msg.split('').reverse().join('') }}</h1>
  <h1>{{ msg.split('').reverse().join('') }}</h1>
  <h1>{{ msg.split('').reverse().join('') }}</h1> 
  -->
  <!-- 
    로직이 너무 많이 실행된다
  <h1>{{ reveseMessage() }}</h1>
  <h1>{{ reveseMessage() }}</h1>
  <h1>{{ reveseMessage() }}</h1>
  -->

  <!-- 이미 계산되서 한번만 연산하고 나머지 [캐싱] 처리한다. -->
  <h1>{{ computedMessage }}</h1>
  <h1>{{ computedMessage }}</h1>
  <h1>{{ computedMessage }}</h1>
</template>

<script>
export default {
  data(){
    return {
      msg : 'Hello Computed'
    }
  },
  methods:{
    reveseMessage(){
      return this.msg.split('').reverse().join('');
    }
  },
  computed:{
    revesedMessage(){
      return this.msg.split('').reverse().join('');
    }
  }
}
</script>

<style>

</style>