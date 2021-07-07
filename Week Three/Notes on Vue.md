<h1>Notes on Vue.js from Documentation</h1> 

<h2>Notes</h2>

* Basic Vue Component: 
 ```
 Vue.component('button-counter', {
  data: function () {
    return {
      count: 0
    }
  },
  template: '<button v-on:click="count++">You clicked me {{ count }} times.</button>'
  })
  ```
* We can display components as a custom elements (e.g. `<button-counter></button-counter>` inside a root Vue by using `new Vue`. For example:
 ```
 <div id="components-demo">
  <button-counter></button-counter>
  </div>
  
  new Vue({ el: '#components-demo' }) 
  ``` 
* `#` allows us to mount to the id


