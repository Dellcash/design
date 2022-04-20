<script setup>
import Navigation from "./components/Navigation.vue";
</script>

<template>
	<Navigation />
	<main>
		<img
			src="./assets/images/image-hero-mobile.png"
			alt=""
			w-full
			h-full
			lg:hidden
		/>
		<div mt-8 text-center>
			<h2 text=" 1.8rem Black">Make remote work</h2>
			<p text="Gray sm" mt-3 px-5 tracking-tight>
				Get your team in sync, no matter your location. Streamline processes,
				create team rituals, and watch productivity soar.
			</p>
			<div flex items-center justify-center mt-5>
				<button text-White bg-Black rounded-xl p-3 px-18px>Learn More</button>
			</div>
		</div>
		<div flex items-center justify-between mt-8 mx-2 mb-5 md:mx-5 md:mt-10>
			<img src="./assets/images/client-databiz.svg" alt="" w-17 md:w-30 />
			<img src="./assets/images/client-audiophile.svg" alt="" w-10 md:w-18 />
			<img src="./assets/images/client-maker.svg" alt="" w-14 md:w-30 />
			<img src="./assets/images/client-meet.svg" alt="" w-14 md:w-30 />
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

body {
	background-color: hsl(0, 0%, 98%);
}

button {
	border: none;
	background-color: transparent;
	outline: none;
	cursor: pointer;
}

li {
	list-style: none;
}
</style>
