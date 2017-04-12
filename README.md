# Polymer SVG Template poly-fill

When defining a custom element in Polymer, using any `<template>` element (dom-if/dom-repeat) in <svg> [won't work](https://github.com/Polymer/polymer/issues/1976) in some browsers, load this shim before calling Polymer factory, shall make it work properly cross-browsers.

This shim should work with polymer 2.0 as well.
 
## Usage 
 
 ```!html
<link rel="import" href="../bower_components/polymer-svg-template/polymer-svg-template.html"/>
 <dom-module id="my-svg-template">
	 <template>
	 	<svg>
	 		<template is="dom-if" if="[[_condition]]">
	 			...
	 		</template>
	 	</svg>
	 </template>
</dom-module>
<script>
	//  Polyfill all <template> elements inside of any <svg> container within
	PolymerSvgTemplate('my-svg-template');
 	Polymer({
 		is: 'my-svg-template'
 		...
 	})
 </script>
 ```
