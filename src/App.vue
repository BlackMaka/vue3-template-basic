<template>
  <div>
    <h1>{{ msg }}</h1>
    <input
      type="text"
      :value="msg"
      @chage="msg = $event.target.value" />
    <input
      type="text" 
      v-model.lazy="msg" />
    <!-- =========================================== -->
    <input
      type="text"
      v-model.number="num" />
    <!-- number type유지 -->
    <input
      type="text"
      v-model.trim="msg" />
  </div>
</template>

<script>
export default {
  data(){
    return{
      msg: 'Hello World!',
      num :123,
    }
  },
  watch:{
    msg(){
      console.log(typeof this.num);
    }
  }
}
</script>

<style>

</style>