<template>
  <div>
    <div
      class="btn">
      <slot>Apple</slot>
      <slot name="name">
      </slot>
      <slot name="icon">
      </slot>
    </div>
  </div>
</template>

<script>
export default {
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