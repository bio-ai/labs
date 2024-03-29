# Vue

Aug 1, 2019
-----------

notes from Udemy Course:
https://www.udemy.com/vuejs-2-the-complete-guide/

## VueJS interacting with the DOM

- v-once - just one rendering
```vue
<h1 v-once>{{ title }}</h1>
```

- v-html - to render html code
```vue
<p v-html="finishedLink"></p>
```

- v-on:click="methodToCallOnClick"

- Event object holds the event props: eg. onClick holds the coordinates where the click happened
```vue
<p v-on:mousemove="updateCoordinates">{{ x }} / {{ y }}</p>

...
data: {
    x: 0,
    y: 0
},
methods: {
    updateCoordiantes: function(event) {
        this.x = event.clientX;
        this.y = event.clientY;
    }
}
...
```

### ToDo: To read the content of the current cell and insert into formula string
### ToDo: Recalculate current cell formulas/API, etc on click
- Passing own and event arguments:

```vue
<button v-on:click="increase(2, $event)"></button>

methods: {
    increase: function(step, event) {
        this.counter += step;
    }
}
```

- Modifying  an Event with Event Modifiers: v-on:mousemove.stop=""
https://www.udemy.com/vuejs-2-the-complete-guide/learn/lecture/5941028#overview
- also prevent default modifier, event.stopPropagation()
- also works as chained: v-on:mousemove.stop.prevent=""
```vue
<span v-on:mousemove.stop="">DEAD SPOT</span>
```

- Listening to Keyboard Events
https://vuejs.org/v2/guide/events.html#Key-Modifiers
https://www.udemy.com/vuejs-2-the-complete-guide/learn/lecture/5941032#overview
```vue
<input type="text" v-on:keyup.enter="alertMe">
```
- also works with chaining: v-on:keyup.enter.space="alertMe"

### Vue links / Interacting with the DOM 

Official Docs - Getting Started: http://vuejs.org/guide/

Official Docs - Template Syntax: http://vuejs.org/guide/syntax.html

Official Docs - Events: http://vuejs.org/guide/events.html

Official Docs - Computed Properties & Watchers: http://vuejs.org/guide/computed.html

Official Docs - Class & Style Binding: http://vuejs.org/guide/class-and-style.html


## Conditionals v-if, v-show and Rendering lists v-for

- v-else-if - New in 2.1.0+
- Similar to v-else, a v-else-if element must immediately follow a v-if or a v-else-if element.
```vue
<div v-if="type === 'A'">
  A
</div>
<div v-else-if="type === 'B'">
  B
</div>
<div v-else-if="type === 'C'">
  C
</div>
<div v-else>
  Not A/B/C
</div>
```
### Links for vue Conditionals and list rendering
JSFiddle:

Conditionals (v-if and v-show): https://jsfiddle.net/smax/hoc719j5/
Lists: https://jsfiddle.net/smax/o7uy2g0u/
Useful Links:

Official Docs - Conditionals: http://vuejs.org/guide/conditional.html
Official Docs - Lists: http://vuejs.org/guide/list.html

## Animations and Transitions

- add transition class eg: fade
- then vue will attach fade-enter, fade-enter-active, fade-leave, fade-leave-active

- initial animation with: appear

- transition between multiple elements with: mode="out-in" or mode="in-out"

- transition JS hooks:
![](img/screen.png)


## Vue CLI 3

- install on mac with
```bash
sudo npm install -g @vue/cli
```
- create new app project with
```bash
vue create new-app
```

