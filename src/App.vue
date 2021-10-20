<template>
  <div>
    <input
      type="text"
      @keydown.enter="handler" />
    <input
      type="text"
      @keydown.a="handlerAkey" />
    <input
      type="text"
      @keydown.ctrl.shift.a="handlerCtrlShiftA" />
  </div>
</template>

<script>
export default {
  methods:{
    handler(){
      console.log('Enter');
    },
    handlerAkey(){
      console.log('a');
    },
    handlerCtrlShiftA(){
      console.log('ctrl + shift + a');
    }
  }
}
</script>

<style>

</style>