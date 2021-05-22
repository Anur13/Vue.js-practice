<template>
  <div class="search">
    <label
      >Search contact by name
      <input type="text" @input="event => $emit('input', event.target.value)" />
    </label>
  </div>
</template>

<script>
export default {}
</script>

<style lang="css" scoped>
.search {
  margin-top: 100px;
  text-align: right;
}
</style>
