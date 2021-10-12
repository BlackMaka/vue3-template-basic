<template>
  <!-- v-once, {{}} -->
  <h1 
    v-once
    @click="add">
    {{ msg }}
  </h1>
  <!-- v-html -->
  <span v-html="html"></span>
  <!-- v-bind: -->
  <h1 :class="active">
    {{ active }}
  </h1>
  <h1 
    :[attr]="active"
    @[event]="add">
    {{ msg }}
  </h1>
</template>

<script>
export default {
  data(){
    return{
      msg:'Hello world!',
      html:'<div style="color:red;">hihi</div>',
      active : 'active',
      attr : 'class',
      event: 'click'
    }
  },
  methods:{
    add(){
      this.msg += '!'
    }
  }
}
</script>

<style>
  .active{
    color:royalblue;
    font-size: 100px;
  }
</style>