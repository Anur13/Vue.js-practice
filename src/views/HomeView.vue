<template>
  <div>
    <h1>{{ test }}</h1>
    <h2>{{increment}}</h2>
    <Input v-model="test"  v-on:increment-btn="increment += $event" />
  </div>
</template>

<script>
import Input from '@/components/Input'
export default {
  name: 'homepage',
  components: {
    Input
  },
  data() {
    return {
      test: ' ',
      increment: 1
    }
  },
  methods: {
    // modelValue(event) {
    //   console.log(event.target.value)
    //   this.value = event.target.value
    // },
    emailHandler (){

    }
  }
}
</script>
