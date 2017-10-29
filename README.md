# learningVueJS

Vue.JS is a progressive javascript framework that focuses on building user interfaces:

* works in the view layer only
* incrementally adoptable
* easily integrated into other projects & libraries
* capable of powering advanced SPAs

## Vue.JS offers:

* reactive interfaces
* declarative rendering
* data binding
* directives
* template logic
* components & nesting
* event handling
* computed properties
* CSS transitions & animations
* custom filters

## Using Vue.JS:

There are a number of ways to implement Vue.JS:

* include in the `<script>` tag in an HTML file
* install using NPM
* use the vue-cli tool along with Webpack
* install using bower client side package manager

## vue-cli tool

This is the recommended way to build Vue.JS apps

	$ npm install -g vue-cli		// install vue-cli globally
	$ vue init webpack myapp		// create new project with webpack template
	$ cd myapp
	$ npm install					// install dependencies
	$ npm run dev					// run development server
	$ npm run build 				// build application to production

## Simple example

Rendering data to the DOM and using interpolation

	<div id="app">
		{{msg}}
	</div>

	Var app = new Vue({
		el: '#app',
		data: {
			msg: 'Hello World!'
		}
	});

## Directives

Special attribute with the `v-` prefix that does something to the DOM. Reactively applies side effects to the DOM when the value of its expression changes.

	<element v-directiveId="[argument:] expression [| filters...]">
	</element>

## Simple directive example

	<span>{{msg}}</span>			// basic interpolation

	<span v-text="msg"></span>		// using v-directive
	
	<span v-html="msg"></span>		// parses html
	
	<span v-once>{{msg}}</span>		// one-time interpolation

## Conditionals & loops

Given this data:

	data: {
		show: true,
		users: [
			{ name: 'Bob' },
			{ name: 'Kathy' }
		]
	}

We can see this happen in the view layer:

	// if statement

	<p v-if="show">This is shown</p>
	<p v-else>This is not</p>

	// show

	<p v-show="show">This is shown</p>

	// for loop

	<li v-for="user in users">{{user.name}}</li>
