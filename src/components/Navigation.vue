<script setup>
import { ref } from "vue";

const menu = ref(false);
</script>

<template>
	<header p-5>
		<div flex items-center justify-between>
			<h2 text-2rem tracking-tighter>snap</h2>
			<button @click="menu = !menu">
				<img v-if="menu" src="../assets/images/icon-menu.svg" alt="" />
			</button>
		</div>
	</header>
	<div bg="[rgba(0, 0, 0, 0.7)]" w-full>
		<div v-if="!menu" absolute w="[60%]" h-screen bg-White top-0 right-0>
			<div flex justify-end p-5>
				<button @click="menu = !menu">
					<img src="../assets/images/icon-close-menu.svg" alt="" />
				</button>
			</div>
		</div>
	</div>
</template>
