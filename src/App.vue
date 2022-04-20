<script setup>
import Navigation from "./components/Navigation.vue";
</script>

<template>
	<Navigation />
	<main lg:flex lg:items-center lg:justify-between lg:px-35>
		<img
			src="./assets/images/image-hero-mobile.png"
			alt=""
			w-full
			h-full
			lg:hidden
		/>
		<div lg:mr-30 lg:mt-20>
			<div mt-8 text-center lg:text-left>
				<h2 text=" 1.8rem Black" lg:text-5rem>Make remote work</h2>
				<p
					text="Gray sm"
					mt-3
					px-5
					tracking-tight
					lg:px-0
					lg:text-16px
					lg:pr-20
					lg:mt-10
					lg:mb-10
				>
					Get your team in sync, no matter your location. Streamline processes,
					create team rituals, and watch productivity soar.
				</p>
				<div flex items-center justify-center mt-5 lg:justify-start>
					<button
						text-White
						bg-Black
						rounded-xl
						p-3
						px-18px
						lg:text-16px
						lg:py-4
						lg:px-6
						border
						hover="bg-transparent text-Black "
					>
						Learn More
					</button>
				</div>
			</div>
			<div
				flex
				items-center
				justify-between
				mt-8
				mx-2
				mb-5
				md:mx-5
				md:mt-10
				lg:mt-20
				lg:mx-0
			>
				<img src="./assets/images/client-databiz.svg" alt="" w-17 md:w-26 />
				<img src="./assets/images/client-audiophile.svg" alt="" w-10 md:w-16 />
				<img src="./assets/images/client-maker.svg" alt="" w-14 md:w-26 />
				<img src="./assets/images/client-meet.svg" alt="" w-14 md:w-26 />
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
