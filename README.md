# vue-basic-autocomplete
A Vue.js autocomplete component. Compatible with Vue 2.x.

#### [Sandbox](https://jsfiddle.net/ovictorpereira/tk65ecL8/15/ "Sandbox")

![Alt Text](https://media.giphy.com/media/cmzpTVS8rLWsxOX90l/giphy.gif)

## Installation
NPM
```bash
$ npm install vue-basic-autocomplete --save
``` 
Register the component
```js
import Vue from 'vue'
import VueBasicAutocomplete from 'vue-basic-autocomplete'

Vue.use(VueBasicAutocomplete)
``` 

## Usage
```html
<vue-basic-autocomplete v-model="selected" :options="myArray" trackby="name" input-class="form-control" />
```
```js
new Vue({
    data: {
        myArray: [
            {name: 'Lion', id: 1},
            {name: 'Lion Two', id: 2}
        ],
        selected: ''
    }
})
```

## Available props

| Prop        | Type             | Default                | Description                                      |
|-------------|------------------|------------------------|--------------------------------------------------|
| options     | Array (required) |                        | Array of options to autocomplete                 |
| minlength   | Number           | 1                      | Min. length to start listing. If set to 0, all the array will be listed on focus   |
| noneFind    | String           | No matching results    | Default label when there are no matching results |
| trackby     | String           |                        | Required when you are using an array of objects  |
| placeholder | String           |                        | Placeholder                                      |
| list-max-height | String       |       300              | Max-heigth in px                                      |
| 'input-class'     | String           |                  | Custom CSS class for the input. Since I am using Bootstrap, I set it as 'form-control' |