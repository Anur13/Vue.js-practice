<template>
  <li>
    <div>
      <p>Name: {{contact.name}}</p>
      <p>Age: {{contact.age}}</p>
      <p>Phone: {{contact.phone}}</p>
      <button @click="deleteContact" type="button">Delele contact</button>
    </div>
  </li>
</template>

<script>
export default {
 props: {contact : {
  type : Object
 }},
  name: 'ContactListItem',
  methods: {
deleteContact () {
 this.$emit('deleteContact', this.contact.id)
}
  }
}
</script>

<style lang="scss" scoped></style>
