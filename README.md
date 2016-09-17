# Polymer SVG Template poly-fill

Templates inside SVG won't work in polymer-1.0 without this poly-fill, include this script on top of your element's <script> tag,
 it must be evaluated before call to Polymer.
 
## Usage 
 
 ```!html
 <dom-module id="my-svg-template">
	 <template>
	 	<svg>
	 		<template is="dom-if" if="[[_condition]]">
	 			...
	 		</template>
	 	</svg>
	 </template>
</dom-module>
 <script src="../polymer-svg-template/index.js"></script>
 <script>
 	Polymer({...})
 </script>
 ```
