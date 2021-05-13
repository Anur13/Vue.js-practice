<template>
  <div>
    <form @submit="submitContactForm">
      <label>
        Name
        <input v-model="name" type="text" />
      </label>
      <label>
        Age
        <input v-model="age" type="number" />
      </label>
      <label>
        Phone
        <input v-model="phone" type="text" />
      </label>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
  import { uuid } from 'vue-uuid' // Import uuid  
export default {
  name: 'ContactForm',
  data() {
    return {
      name: '',
      age: '',
      phone: ''
    }
  },
  methods: {
    submitContactForm(e) {
      e.preventDefault()
      const contact = {
        name: this.name,
        age: this.age,
        phone: this.phone,
        id : uuid.v1()
      }

      this.$emit('createNewContact', contact)
      ;(this.name = ''), (this.age = ''), (this.phone = '')
    }
  }
}
</script>

<style lang="scss" scoped></style>
