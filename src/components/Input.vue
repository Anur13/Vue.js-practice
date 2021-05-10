<template>
  <div>
    <input @input="event => $emit('input', event.target.value)" />
    <button @click=" $emit('increment-btn', 1)">test</button>
  </div>
</template>

<script>
export default {
  // prop: ['value',],

  // methods: {
  //   handleInput(e) {
  //     this.$emit('input', e.target.value)
  //   }
  // }
}
</script>

<style lang="scss" scoped></style>
