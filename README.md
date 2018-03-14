[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/renfeng/css-flip)

## &lt;css-flip&gt;

`<css-flip>` displays a flip animation implemented with CSS animation. Inspired by, and code (with modification) copied from https://codepen.io/darkwing/pen/bCali

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="css-flip.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->

```html
<dom-bind>
	<template>
		<style>
			css-flip {
				width: 320px;
				height: 427px;
			}

			.front {
				/* Specify a background-image url to provide an image for the front side . */
				background: url(http://davidwalsh.name/demo/dwflip.jpg) 0 0 no-repeat;
				height: 100%;
			}

			.back {
				background: #f8f8f8;
				height: 100%;
			}
			
			.front .name {
				font-size: 2em;
				display: inline-block;
				background: rgba(33, 33, 33, 0.9);
				color: #f8f8f8;
				font-family: Courier;
				padding: 5px 10px;
				border-radius: 5px;
				bottom: 60px;
				left: 25%;
				position: absolute;
				text-shadow: 0.1em 0.1em 0.05em #333;
			
				-webkit-transform: rotate(-20deg);
				-moz-transform: rotate(-20deg);
				-o-transform: rotate(-20deg);
				transform: rotate(-20deg);
			}
			
			.back-logo {
				position: absolute;
				top: 40px;
				left: 90px;
				width: 160px;
				height: 117px;
				background: url(http://davidwalsh.name/demo/logo.png) 0 0 no-repeat;
			}
			
			.back-title {
				font-weight: bold;
				color: #00304a;
				position: absolute;
				top: 180px;
				left: 0;
				right: 0;
				text-align: center;
				text-shadow: 0.1em 0.1em 0.05em #acd7e5;
				font-family: Courier;
				font-size: 2em;
			}
			
			.back p {
				position: absolute;
				bottom: 40px;
				left: 0;
				right: 0;
				text-align: center;
				padding: 0 20px;
				font-family: arial;
				line-height: 2em;
			}
		</style>
		<css-flip flipped="{{flipped}}">
			<div class="front" slot="front">
				<span class="name">David Walsh</span>
			</div>
			<div class="back" slot="back">
				<div class="back-logo"></div>
				<div class="back-title">@davidwalshblog</div>
				<p>Mozilla Web Developer, MooTools & jQuery Consultant, MooTools Core Developer, Javascript Fanatic, CSS Tinkerer, PHP Hacker, and web lover.</p>
			</div>
		</css-flip>
		<p>Flipped: [[flipped]]</p>
	</template>
</dom-bind>
```
