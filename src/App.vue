<template>
  <div>
    <!--v-if-->
    <h1 v-if="false">
    </h1>
    <!-- style="display:none" -->
    <h1 v-show="false">
    </h1>
  </div>
</template>

<script>
export default {
  //v-if 게으름 : false 구조적으로 렌더링 하지않음  
  //전환비용이 크다 DOM 구조가 리렌더링 되기 때문에
  //v-show : false DOM에 남아있음 /자주 쓰는건 v-show (구조적으로 이미 렌더링이 되어있음 초기 렌더링 비용이 크다 )
  // 전환비용이 낮음 disply none으로만 바꿔주면됨
}
</script>

<style>

</style>