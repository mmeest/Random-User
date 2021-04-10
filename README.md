<p align="center"><img src="VS.png" width="350px"></p>

<h1 align="center">
    <strong>Random-User</strong>
</h1>
<h3 align="center">
    <p>Random user generator written in Vue JS</p>
</h3>

<p align="center"><img src="screenshot.png" width="200px"></p>

### Contents
- [Vue JS](#vue-js)

### Vue JS
Vue JS - https://vuejs.org/ \
Initial release - February 2014 \
Written in - TypeScript \
Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable.

**Why Use Vue?**
* Create dynamic frontend apps & websites
* Easy learning curve
* Easy to integrate with other projects
* Fast & lightweight
* Virtual DOM
* Extremely popular (and rising)
* Great community

**Basic Layout of a Vue consist 3 Components**
* Output or HTML view
* JavaScript - logic with props, data and methods
* Style
```
<template>
  <header>
    <h1>{{title}}</h1>
  </header>
</template>

<srcipt>
export default{
  props: {
    title: String,
  },
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
```

**Vue.js Directives**
* Vue.js uses double braces {{ }} as place-holders for data.
* Vue.js directives are HTML attributes with the prefix v-

**Creating new Vue object**
* In the example below, a new Vue object is created with new Vue().
* The property el: binds the new Vue object to the HTML element with id="app".
```

<div id="app">
<h1>{{ message }}</h1>
</div>

<script>
var myObject = new Vue({
    el: '#app',
    data: {message: 'Hello Vue!'}
})
</script>
```

**Vue.js Binding**
* When a Vue object is bound to an HTML element, the HTML element will change when the Vue object changes:
```

<div id="app">
{{ message }}
</div>

<script>
var myObject = new Vue({
    el: '#app',
    data: {message: 'Hello Vue!'}
})

function myFunction() {
    myObject.message = "John Doe";
}
</script>
```

**Two-way binding**
* The v-model directive binds the value of HTML elements to application data.
* This is called two-way binding:
```

<div id="app">
  <p>{{ message }}</p>
  <p><input v-model="message"></p>
</div>

<script>
var myObject = new Vue({
    el: '#app',
    data: {message: 'Hello Vue!'}
})
</script>
```

**Loop binding**
* Using the v-for directive to bind an array of Vue objects to an "array" of HTML element:
```

<div id="app">
 <ul>
   <li v-for="x in todos">
   {{ x.text }}
   </li>
  </ul>
</div>

<script>
myObject = new Vue({
    el: '#app',
    data: {
    todos: [
        { text: 'Learn JavaScript' },
        { text: 'Learn Vue.js' },
        { text: 'Build Something Awesome' }
        ]
    }
})
</script>
```

### Creating Vue project
We have 3 files in our single page application project: 'app.js', 'index.html' and 'style.css'\
Add 'div' with id="app", Vue source link and your app script link to index.html 'body' tag
```
<body>
    <div id="app"></div>
    
    <script src="https://unpkg.com/vue@next"></script>
    <spcipt src="app.js"></spcipt>
</body>
```

In our script file 'app.js' we create variable for Vue with basic template and pass it to our html
```
const app = Vue.createApp({
    template: '<h1>Hello World</h1>',
})

app.mount('#app')       // mounting app to our HTML tag
```

This will dislay HTML page with 'Hello World' text

# `HAPPY CODING !!! :)`
