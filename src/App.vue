<template>
  <div>
    <h1 id="hello1">
      hello1
    </h1>
    <h1 ref="hello2">
      hello2
    </h1>
    <Hello ref="hello3" />
  </div>
</template>

<script>
import Hello from '~/components/Hello'
export default {
  components:{
    Hello
  },
  mounted(){
    console.log('mounted');
    const hello1 = document.querySelector('#hello1');
    console.log(hello1.textContent); // hello1
    console.log(this.$refs.hello2.textContent); // hello2
    //console.log(this.$refs.hello3.$el.textContent); // hello3 상위 루트가 하나일때만 가능
    console.log(this.$refs.hello3.$refs.hello32.textContent); 
  },
  
}
</script>

<style>

</style>