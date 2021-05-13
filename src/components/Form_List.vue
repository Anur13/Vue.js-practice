<template>
  <div>
    <ContactForm @createNewContact="addContact"  />
    <div class="flex-container">
      <SearchForm v-model="query" />
      <ContactList @deleteContact="deleteContact" :contacts="contacts" :query="query" />
    </div>
  </div>
</template>

<script>
import ContactForm from './ContactForm/ContactForm'
import ContactList from '@/components/List/ContactList'
import SearchForm from '@/components/ContactForm/SearchForm'
export default {
  name: 'Form_List',
  components: { ContactForm, ContactList, SearchForm },
  data() {
    return {
      contacts: [{ name: 'bla', age: 13, phone: '131231', id: '1' }],
      query: ''
    }
  },
  methods: {
    addContact(contact) {
      this.contacts = this.contacts.concat(contact)
    },
    deleteContact(id) {
        this.contacts = this.contacts.filter(item => item.id !== id)
    }
  }
}
</script>

<style lang="css" scoped>
.flex-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
</style>
