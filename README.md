# vue-form-generator
Creates a vue form (really basic) out of an JSON object.

## Example form
```javascript
myForm: {
    name: 'myForm',
    action: 'myAction',
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
            id: 'checkbox',
            type: 'checkbox',
            placeholder: 'this is a checkbox',
            value: '',
            labelbel: 'my first checkbox',
        }
    ]
}
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run dev
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```
