# Vue-Json-Edit-Modal

> A modified version of [Visual JSON Editor](https://github.com/jinkin1995/vue-json-edit) that opens a modal on edit.

</br>


## **[DEMO](http://melvinchng.github.io/vue-json-edit-modal)**

</br>


## Getting Started
```
npm install vue-json-edit-modal --save
```

</br>


## Usage

``` javascript
//import it in your project At your entry point

import vue from 'vue'
import JsonEditor from 'vue-json-edit'
  
Vue.use(JsonEditor)
```
### Props

* objData: json data
* options
    * confirmText: strings of the confirm button
    * cancelText: strings of the cancel button


</br>

## Example
Single file component
``` html

<template>
    <JsonEditor
        :options="{
            confirmText: 'confirm',
            cancelText: 'cancel',
        }"
        :objData="jsonData" 
        v-model="jsonData" >
    </JsonEditor>
</template>
<script>
export default {
    ...
    data: function() {
        return {
            jsonData: {
                name: 'mike',
                age: 23,
                phone: '18552129932',
                address: ['AAA C1', 'BBB C2']
            }
        }
    }
}
</script> 
```

</br>



