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
            value: 'this is an inputfield',
            label: 'Name',
        },
        {
        id: 'checkbox',
        type: 'checkbox',
        value: 'this is a checkbox',
        labelbel: 'my first checkbox'
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
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
