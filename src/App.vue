<script setup>
import Navigation from "./components/Navigation.vue";
</script>

<template>
	<Navigation />
	<main>
		<img src="./assets/images/image-hero-mobile.png" alt="" w-full h-full />
		<div mt-8>
			<h2 text="center 1.8rem Black">Make remote work</h2>
		</div>
	</main>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Epilogue:wght@500;700&display=swap");

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: "Epilogue", sans-serif;
}

button {
	border: none;
	background-color: transparent;
	outline: none;
}

li {
	list-style: none;
}
</style>
