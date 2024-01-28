<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue" // you need this to use ref()


</script>



<!-- the template is where the html code goes -->
<template>

<div id="navbar" class="container">  
        <div id="title">Christopher Mina  Website</div>
        
        <div id="logo">
            <img src="./cow.jpg">

        </div>
        

    </div>

    <div id="flex">

        <div id="sidebar" class="container"> Sidebar </div>

        <div id="main" class="container"> Text input </div>
    </div>
	<div id="navbar">
		<button id="myButton">Click me!</button>
	</div>
	
	<div id="flex">
		<div id="sidebar">Sidebar</div>
		<div id="main">Text input</div>
	</div>
</template>

<button id="img-btn">Display Image</button>


<!-- style is where the css code goes -->
<style scoped>
	html {
			background-color: aqua;
		}
		
		body {
			margin: 0;
		}
		
		div {
			/* put the borders in the inside of container */
			box-sizing: border-box;
		}
		
		img {
			height: 100%;
			width: auto;
		}
		
		#flex {
			display: flex;
			height: calc(100vh - 50px);
		}
		
		#sidebar {
			width: 40%;
			border-color: blue;
		}
		
		#main {
			width: 70%;
			background-color: green;
		}
		
		#title {
			width: 80%;
			float: left;
		}
		
		#logo {
			width: 30%;
			height: 100%;
			float: right;
			text-align: right;
		}
		
		.container {
			border-style: dotted;
			border-width: 1px;
		}

</style>