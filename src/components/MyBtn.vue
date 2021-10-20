<template>
  <div>
    <div
      class="btn"
      @dblclick="$emit('clickEvent', $event)"> 
      <!-- @dblclick="$emit('clickEvent', 'clickMsg')">  -->
      <slot></slot>
    </div>
    <input
      type="text"
      v-model="msg" />
  </div>
</template>

<script>
export default {
    emits:[
        'clickEvent',
        'changeMsg'
    ],
    data(){
        return {
            msg:''
        }
    },
    watch:{
        msg(){
            this.$emit('changeMsg', this.msg);
        }
    }
}
</script>

<style lang=scss>
    .btn{
        border-radius: 5px;
        display: inline-block;
        color: white;
        background-color: gray;
        padding: 10px;
        margin: 3px;
    }
</style>