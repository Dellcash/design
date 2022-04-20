<script setup>
import Navigation from "./components/Navigation.vue";
</script>

<template>
	<Navigation />
	<main lg="flex items-center justify-between px-35">
		<img
			src="./assets/images/image-hero-mobile.png"
			alt=""
			w-full
			h-full
			lg:hidden
		/>
		<div lg="mr-30 mt-20">
			<div mt-8 text="center lg:left">
				<h2 text="1.8rem Black lg:5rem">Make remote work</h2>
				<p
					text="Gray sm lg:16px"
					p="x-5 lg:x-0 lg:r-20"
					m="t-3 lg:t-10 lg:b-10"
					tracking-tight
				>
					Get your team in sync, no matter your location. Streamline processes,
					create team rituals, and watch productivity soar.
				</p>
				<div mt-5 flex items-center justify="center lg:start">
					<button
						text="White lg:16px"
						p="3 lg:y-4 lg:x-6"
						hover="bg-transparent text-Black "
						bg-Black
						rounded-xl
						border
					>
						Learn More
					</button>
				</div>
			</div>
			<div
				class="flex items-center justify-between"
				m="t-8 x-2 b-5 md:x-5 md:t-10 lg:t-20 lg:x-0"
			>
				<img src="./assets/images/client-databiz.svg" alt="" w="17 md:26" />
				<img src="./assets/images/client-audiophile.svg" alt="" w="10 md:16" />
				<img src="./assets/images/client-maker.svg" alt="" w="14 md:26" />
				<img src="./assets/images/client-meet.svg" alt="" w="14 md:26" />
			</div>
		</div>
		<img
			src="./assets/images/image-hero-desktop.png"
			alt=""
			hidden
			lg:block
			w="2/5"
		/>
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
