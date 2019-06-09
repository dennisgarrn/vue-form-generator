<template>
  <div id="app" class="container">
    <baseForm :form="myForm" />
  </div>
</template>

<script>
import baseForm from '@/components/form.vue'

export default {
  name: 'app',
  data() {
    return {
      myForm: {
        name: 'myForm',
        action: '',
        method: 'POST',
        fields: [
          {
            id: 'name',
            type: 'input',
            value: 'this is an inputfield',
            label: 'Name',
          },
          {
            id: 'address',
            type: 'input',
            value: 'this is an inputfield 2',
          },
          {
            id: 'checkbox',
            type: 'checkbox',
            value: 'this is an inputfield 2',
            label: 'my first checkbox'
          }
        ]
      }
    }
  },
  components: {
    baseForm,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
