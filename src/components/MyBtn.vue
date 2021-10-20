<template>
  <div
    class="btn"
    :class="{large}"
    :style="{ backgroundColor: color}">
    <slot></slot>
  </div>
</template>

<script>
export default {
    props:{
        color:{
            type:String,
            default:'gray'
        },
        large:{
            type:Boolean,
            default:false
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
        &.large{
            padding: 30px;
        }
    }
</style>