<script setup>
import { ref } from "vue";
import Todo from "../assets/images/icon-todo.svg";
import Calendar from "../assets/images/icon-calendar.svg";
import Reminders from "../assets/images/icon-reminders.svg";
import Planning from "../assets/images/icon-planning.svg";
import { onClickOutside } from "@vueuse/core";

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
const outSide = ref();
onClickOutside(outSide, () => {
	feature.value = false;
	company.value = false;
});
</script>

<template>
	<header p-5 lg:p-10 lg:flex lg:items-center lg:justify-between>
		<div flex items-center justify-between lg:justify-start>
			<h2 text-2rem tracking-tighter lg:text-3rem>snap</h2>

			<button @click="menu = !menu" lg:hidden>
				<img v-if="menu" src="../assets/images/icon-menu.svg" alt="" />
			</button>

			<div ml-13 hidden lg:block>
				<ul flex text="xl Gray" space-x-13>
					<li relative>
						<button @click="feature = !feature">
							<span pr-2 text="xl Gray" hover:text-Black>Features</span>
							<img
								v-if="!feature"
								src="../assets/images/icon-arrow-down.svg"
								alt=""
							/>
							<img v-else src="../assets/images/icon-arrow-up.svg" alt="" />
						</button>
						<ul
							ref="outSide"
							v-if="feature"
							text="sm Gray"
							p-8
							my-5
							space-y-2
							absolute
							right-0
							rounded-xl
							shadow-xl
							bg="[#fff]"
						>
							<li
								v-for="feature in features"
								:key="feature"
								flex
								items-center
								cursor-pointer
								hover:text-Black
							>
								<img :src="feature.img" alt="" pr-3 />
								{{ feature.title }}
							</li>
						</ul>
					</li>

					<li relative>
						<button @click="company = !company">
							<span pr-2 text="xl Gray" hover:text-Black>Company</span>
							<img
								v-if="!company"
								src="../assets/images/icon-arrow-down.svg"
								alt=""
							/>
							<img v-else src="../assets/images/icon-arrow-up.svg" alt="" />
						</button>
						<ul
							ref="outSide"
							v-if="company"
							p-5
							my-5
							space-y-2
							absolute
							left-0
							rounded-xl
							shadow-xl
							bg="[#fff]"
							text="sm Gray"
						>
							<li>History</li>
							<li>Our Team</li>
							<li>Blog</li>
						</ul>
					</li>

					<li cursor-pointer hover:text-Black>Careers</li>

					<li cursor-pointer hover:text-Black>About</li>
				</ul>
			</div>
		</div>
		<div hidden lg:block space-x-5>
			<button text="base Gray" p-4 hover:text-Black>Login</button>
			<button
				text="base White"
				rounded-5
				px-5
				py-3
				bg-Black
				hover="bg-transparent border text-Black"
			>
				Register
			</button>
		</div>
	</header>
	<nav>
		<div>
			<div v-if="!menu" bg="#000" h-full fixed top-0 opacity-50 w-full />
			<Transition name="slide">
				<div
					v-if="!menu"
					fixed
					w="[60%]"
					md="w-[40%]"
					h-full
					bg-white
					top-0
					right-0
				>
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
									<li
										v-for="feature in features"
										:key="feature"
										flex
										items-center
									>
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
			</Transition>
		</div>
	</nav>
</template>

<style>
.slide-enter-active {
	transition: all 0.3s ease-out;
}

.slide-leave-active {
	transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-enter-from,
.slide-leave-to {
	transform: translateX(20px);
	opacity: 0;
}
</style>
