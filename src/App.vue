<template>
  <div>
    <!-- 인라인 클래스 바인딩 --> 
    <h1 
      :class="{ active : isActive,  't-decoration' : hasClass }"
      @click="activate">
      Hello?! {{ isActive }}
    </h1>
    <!-- computed로 계산된 객체 바인딩도 가능--> 
    <h1 :class="classObject">객체 클래스 바인딩</h1>
    <h1 :class="[activeClass, tDecoClass]">배열클래스 바인딩</h1>
    <h2 :style="{color, fontSize}">스타일 인라인 바인딩</h2>
    <h2 :style="fontStyle">스타일 객체 바인딩</h2>
    <h2 :style="[fontStyle, backgroundColor]">스타일 배열 바인딩</h2>
  </div>
</template>

<script>
export default {
  data(){
    return {
      isActive:false,
      hasClass : true,
      classObject:{
        active : true,
        't-decotation' : false
      },
      activeClass : 'active',
      tDecoClass : 't-decoration',
      // 스타일 바인딩
      color : 'red',
      fontSize: '30px',
      fontStyle:{
        color : 'orange',
        fontSize: '40px',
      },
      backgroundColor:{
        backgroundColor : 'royalblue'
      }
    }
  },
  methods:{
    activate(){
      this.isActive = !this.isActive;
      this.hasClass = !this.hasClass;
      this.classObject.active =  !this.classObject.active;
      this.classObject['t-decoration'] =  !this.classObject['t-decoration'];
    }
  }
}
</script>

<style scoped>
  .active {
    color:red;
    font-weight: bold;
  }
  .t-decoration { 
    text-decoration: underline;
  }
</style>