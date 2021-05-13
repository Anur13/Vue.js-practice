<template>
  <ul>
    <ContactListItem @deleteContact="deleteContact" v-for="contact in filteredContacts" :contact="contact" :key="contact.id" />
  </ul>
</template>

<script>
import ContactListItem from '@/components/List/ContactListItem'
export default {
  name: 'ContactList',
  components: { ContactListItem },
  props: {
    contacts: {
      type: Array
    },
    query: {
      type: String
    }
  },
  methods: {
    deleteContact(id) {
      this.$emit('deleteContact', id)
    }
  },
  computed: {
    filteredContacts: function() {
      return this.contacts.filter(item => item.name.includes(this.query))
    }
  }
}
</script>

<style lang="css" scoped>
ul {
  list-style: none;
  text-align: left;
}
</style>
