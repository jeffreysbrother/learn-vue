To enable Vue Devtools, start a SimpleHTTPServer:

`python -m SimpleHTTPServer 8000`

This will create a new Vue instance, set the desired scope, and create a data object.

```vue
new Vue({
	el: '#root',
	data: {
		message: 'Hello'
	}
})
```

We will then have access to this data here (`v-model` is used specifically for forms): 

```vue
<div id="root">
	<input type="text" id="input" v-model="message">
	<p>the value of the input is {{ message }}</p>
</div>
```

We can also specify an array:

```vue
new Vue({
	el: '#root',
	data: {
		names: ['james', 'kevin', 'hung', 'hillary clinton']
	}
})
```

And then use the `v-for` directive to iterate over the array, and the `v-text` directive to insert that value.

```vue
<div id="root">
	<ul>
		<li v-for="name in names" v-text="name"></li>
	</ul>
</div>
```