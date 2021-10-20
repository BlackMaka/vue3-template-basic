<template>
  <div>
    <button @click="handler">
      btn
    </button>
    <ul>
      <li
        v-for="{name, id} in newFruits"
        :key="id">
        {{ name }} - {{ id }}
      </li>
    </ul>
  </div>
</template>

<script>
//npm i -D shortid
import shortid from 'shortid'
export default {
  data (){
    return {
      fruits:['apple', 'banana', 'cherry']
    }
  },
  computed:{
    newFruits(){
      return this.fruits.map(fruit =>({
          id: shortid.generate(),
          name:fruit
        }))
    }
  },
  methods:{
    handler(){
      this.fruits.push('orange');
    }
  }
}
</script>

<style>

</style>