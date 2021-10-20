<template>
  <div>
    {{ msg }}
    <input 
      type="text" 
      :value="msg"
      @input="handler" />
    <input 
      type="text" 
      :value="msg"
      @input="msg = $event.target.value" />
    <!-- 한글은 한박자 느리기때문에 두번째걸 사용 -->
    <input 
      type="text" 
      v-model="msg" />
    <br />
    {{ isChecked }}
    <input
      type="checkbox" 
      v-model="isChecked" />
  </div>
</template>

<script>
export default {
  data(){
    return{
      msg : 'Hello World!',
      isChecked:false
    }
  },
  methods:{
    handler(event){
      this.msg = event.target.value;
    }
  }
}
</script>

<style>

</style>