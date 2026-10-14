# vue-form-generator

A small Vue 3 + TypeScript playground that renders an HTML form from a plain JSON-style object.

Describe a form once as data (name, action, method, fields). `BaseForm` loops over the fields and renders the matching component for each field `type`.

> Status: early-stage experiment, not a published library. Values are not bound back to state yet and form submission is the native browser submit.

## How it works

```
App.vue            holds the form definition (Form / Field types)
└─ BaseForm.vue    renders <form>, picks a component per field.type
   ├─ BaseInput.vue     type: 'input'    -> <input type="text">
   └─ BaseCheckbox.vue  type: 'checkbox' -> <input type="checkbox">
```

## Form definition

```ts
interface Field {
  id: string;
  type: 'input' | 'checkbox';
  value: string;
  placeholder?: string;
  label?: string;
}

interface Form {
  name: string;
  action: string;
  method: 'GET' | 'POST';
  fields: Field[];
}
```

### Example

```ts
const myForm: Form = {
  name: 'myForm',
  action: '/submit',
  method: 'POST',
  fields: [
    {
      id: 'name',
      type: 'input',
      placeholder: 'Your name',
      value: '',
      label: 'Name',
    },
    {
      id: 'newsletter',
      type: 'checkbox',
      value: '',
      label: 'Subscribe to newsletter',
    },
  ],
};
```

```vue
<BaseForm v-bind="myForm" />
```

## Supported field types

| type       | renders                | notes                          |
| ---------- | ---------------------- | ------------------------------ |
| `input`    | text input             | optional `label`, `placeholder` |
| `checkbox` | checkbox with label    | optional `label`               |

## Getting started

```
npm install
npm run dev        # dev server with hot reload
npm run build      # type-check + production build
npm run lint       # eslint --fix
```
