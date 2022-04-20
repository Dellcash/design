<script setup>
import { ref } from "vue";
import Todo from "../assets/images/icon-todo.svg";
import Calendar from "../assets/images/icon-calendar.svg";
import Reminders from "../assets/images/icon-reminders.svg";
import Planning from "../assets/images/icon-planning.svg";

const menu = ref(true);

const features = ref([
	{
		title: "Todo List",
		img: Todo,
	},
	{
		title: "Calendar",
		img: Calendar,
	},
	{
		title: "Reminders",
		img: Reminders,
	},
	{
		title: "Planning",
		img: Planning,
	},
]);
const feature = ref(false);
const company = ref(false);
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
	<div>
		<div v-if="!menu" bg="#000" h-screen absolute top-0 opacity-50 w-full />
		<div v-if="!menu" absolute w="[60%]" h-screen bg-white top-0 right-0>
			<div flex justify-end p-5>
				<button @click="menu = !menu">
					<img src="../assets/images/icon-close-menu.svg" alt="" />
				</button>
			</div>
			<div p-5>
				<ul text="sm Gray">
					<li mb-3>
						<button @click="feature = !feature">
							<span text-Gray pr-2>Features</span>
							<img
								v-if="!feature"
								src="../assets/images/icon-arrow-down.svg"
								alt=""
							/>
							<img v-else src="../assets/images/icon-arrow-up.svg" alt="" />
						</button>
						<ul v-if="feature" pl-5 my-5 space-y-5>
							<li v-for="feature in features" :key="feature" flex items-center>
								<img :src="feature.img" alt="" pr-3 />
								{{ feature.title }}
							</li>
						</ul>
					</li>

					<li mb-3>
						<button @click="company = !company">
							<span text-Gray pr-2>Company</span>
							<img
								v-if="!company"
								src="../assets/images/icon-arrow-down.svg"
								alt=""
							/>
							<img v-else src="../assets/images/icon-arrow-up.svg" alt="" />
						</button>
						<ul v-if="company" pl-5 my-5 space-y-5>
							<li>History</li>
							<li>Our Team</li>
							<li>Blog</li>
						</ul>
					</li>

					<li mb-3>Careers</li>
					<li>About</li>
				</ul>
			</div>
		</div>
	</div>
</template>
