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
* data in a component must always be a function and displayed as follows: 
```
data () {
  return {
    count: 0,
    required: true
  }
}
```
* To pass data to our components we can use Props: 
```
Vue.component('blog-post', {
  props: ['title'],
  template: '<h3>{{ title }}</h3>'
})
```
* the `{{}}` syntax here allows us to pass through a value e.g. `<blog-post title="My journey with Vue"></blog-post>`
* Here is an example of passing props: 
```
new Vue({
  el: '#blog-post-demo',
  data: {
    posts: [
      { id: 1, title: 'My journey with Vue' },
      { id: 2, title: 'Blogging with Vue' },
      { id: 3, title: 'Why Vue is so fun' }
    ]
  }
})

<blog-post
  v-for="post in posts"
  v-bind:key="post.id"
  v-bind:title="post.title"
></blog-post>
```
* Here the `v-bind` allows us pass props it can be shortened to using just `:` e.g. `:title="post.title"
* Event Listeners in Vue. We can use shorthand `@` but otherwise: 
```
<button v-on:click="$emit('enlarge-text', 0.1)">
  Enlarge text
</button>
```
* In the example above we could shorten to `@click="` but the `$emit` property allows us to carry out a specific event. In the parent... we can use `$listen` to listen out for the event: 
```
<blog-post
  ...
  v-on:enlarge-text="postFontSize += $event"
></blog-post>
```
* Using methods: 
```
<blog-post
  ...
  v-on:enlarge-text="onEnlargeText"
></blog-post>

methods: {
  onEnlargeText: function (enlargeAmount) {
    this.postFontSize += enlargeAmount
  }
}
```
* we call the method (function) in the template to carry out the event. 


