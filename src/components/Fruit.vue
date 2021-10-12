<template>
  <!-- <section v-if="fruit.length > 0"> -->
  <section v-if="hasFruit">
    <h1>Fruits</h1>
    <ul>
      <li
        v-for="fruit in fruits"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
  <section>
    <h1>Reverse Fruit</h1>
    <ul>
      <li
        v-for="fruit in reverseFruits"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data(){
    return{
      fruits:['Apple','Banana','Cherry']
    }
  },
  computed:{
    hasFruit(){
      return this.fruits.length > 0;
    },
    reverseFruits(){
      return this.fruits.map(fruit=>{
        return fruit.split('').reverse().join('');
      })
    }
  }
}
</script>

<style>

</style>