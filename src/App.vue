<template>
  <div id="app" class="container">
    <BaseForm v-bind="myForm" />
  </div>
</template>

<script setup lang="ts">
import BaseForm from '@/components/BaseForm.vue';

export interface Field {
  id: string;
  type: 'input' | 'checkbox';
  value: string;
  placeholder?: string;
  label?: string;
}

export interface Form {
  name: string;
  action: string;
  method: 'GET' | 'POST';
  fields: Field[];
}

const myForm: Form = {
  name: 'myForm',
  action: '',
  method: 'POST',
  fields: [
    {
      id: 'name',
      type: 'input',
      placeholder: 'this is an inputfield',
      value: '',
      label: 'Name',
    },
    {
      id: 'address',
      type: 'input',
      placeholder: 'this is an inputfield 2',
      value: '',
    },
    {
      id: 'checkbox',
      type: 'checkbox',
      placeholder: 'this is a checkbox',
      value: '',
      label: 'my first checkbox'
    }
  ]
};
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
