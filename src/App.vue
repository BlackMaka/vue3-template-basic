<template>
  <div>
    <a
      href="https://www.naver.com"
      target="_blank"
      @click.prevent="handler">NAVER</a>
    <a @click.once="handler">NAVER</a> <!-- ABC 한번만 출력 -->
    <a @click.prevent.once="handler">NAVER</a> 

    <div
      class="parent"
      @wheel.passive="handlerWheel">
      <!-- 스크롤과 로직처리를 분리 -->

      <!-- @click.self="handlerA">
      정확히 자신만 클릭했을때 동작 -->
      <!-- @click.self="handlerA"> -->
      <!-- @click.capture="handlerA">
           @click.capture.stop="handlerA"> -->
      <div
        class="child"
        @click="handlerB">
        <!-- @click.stop="handlerB"> -->
        <!-- 이벤트 버블링 방지 -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods:{
    handler(){
      console.log('ABC');
    },
    handlerA(event){
      console.log(event.target); //실제 타겟
      console.log(event.currentTarget); //.self  => event.target === event.currentTarget
      console.log('A');
    },
    handlerB(){
      console.log('B');
    },
    handlerWheel(event){
      for(let i= 0; i <10000; i+=1){
        console.log(event);
      }
    }
  }
}
</script>

<style lang="scss">
  .parent{
    width: 200px;
    height: 100px;
    background-color: royalblue;
    margin: 10px;
    padding: 10px;
    .child{
      width: 100px;
      height: 100px;
      background-color: orange;
    }
  }

</style>