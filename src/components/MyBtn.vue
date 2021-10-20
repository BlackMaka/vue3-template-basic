<template>
  <!-- 상위 컴포넌트 클래스가 기본 상속됨 (최상위로트 1개 있을때만) -->
  <div
    class="btn"> 
    <slot></slot>
  </div>
  <h1 :class="$attrs.class">
    ㅎㅇ
  </h1>
  <h1 :style="$attrs.style">
    ㅎㅇ
  </h1>
  <!-- 상위 컴포넌트 속성 한번에 적용 -->
  <h1 v-bind="$attrs">
    ㅎㅇ
  </h1>
</template>

<script>
export default {
  inheritAttrs : false, // 상위 컴포넌트 속성 상속 false
  created(){
      console.log(this.$attrs);
      console.log(this.$attrs.style);
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