<template>
	<div
		class="flex-1 z-0 w-full"
		:class="{
			'fixed z-40':$parent.fixedNavBar,
			'relative':!$parent.fixedNavBar,
		}"
	>
		<div class="px-4 md:px-8 py-2 h-16 flex justify-between items-center border-b bg-white">
			<div class="flex items-center w-2/3">
				<button
					class="p-2 rounded-full hover:bg-gray-200 cursor-pointer md:hidden"
					@click="$parent.toggleSideMenu()"
				>
					<Icon name="hamburger" />
				</button>
				<div class="text-xl font-bold tracking-tight text-gray-800 ml-2">
					Ozone Admin.
				</div>
			</div>
			<div class="flex items-center">
				<a
					href="#"
					class="text-gray-500 p-2 rounded-full hover:text-blue-600 hover:bg-gray-200 cursor-pointer mr-4"
				>
					<Icon name="alert" />
				</a>

				<div class="relative">
					<button
						@click="toggle"
						class="cursor-pointer font-bold w-10 h-10 bg-blue-200 text-blue-600 flex items-center justify-center rounded-full"
					>
						DA
					</button>

					<div
						v-if="open"
						class="absolute top-0 mt-12 right-0 w-48 bg-white py-2 shadow-md border border-gray-100 rounded-lg z-50"
					>
						<a
							href="#"
							class="block px-4 py-2 text-gray-600 hover:bg-gray-100 hover:text-blue-600"
						>Edit Profile</a>
						<a
							href="#"
							class="block px-4 py-2 text-gray-600 hover:bg-gray-100 hover:text-blue-600"
						>Sign Out</a>
					</div>
				</div>
			</div>
		</div>
		<div class="bg-white shadow-sm h-16">
			<div class="md:max-w-6xl md:mx-auto flex justify-around md:justify-between items-center">
				<template
					v-for="menu in menus"
					:key="menu"
				>
					<router-link
						:to="menu.url"
						v-if="menu.url != '#'"
						class="px-4 py-5 flex items-center font-medium text-gray-500 hover:text-blue-600"
					>
						<Icon
							:name="menu.icon"
							class="mr-0 md:mr-2"
						/>
						<div class="hidden md:block">
							{{ menu.name }}
						</div>
					</router-link>
					<a
						href="#"
						v-else
						class="px-4 py-5 flex items-center font-medium text-gray-500 hover:text-blue-600"
					>
						<Icon
							:name="menu.icon"
							class="mr-0 md:mr-2"
						/>
						<div class="hidden md:block">
							{{ menu.name }}
						</div>
					</a>
				</template>
			</div>
		</div>
	</div>
</template>

<script>
import Icon from "@/components/Icon";
import { menu_items } from "../services.js";

export default {
	components: {
		Icon
	},
	data() {
		return {
			menus: menu_items,
			open: false
		};
	},
	methods: {
		toggle() {
			console.log("toggling");
			this.open = !this.open;
		}
	}
};
</script>

<style lang="css" scoped>
.active,
.active-left {
	position: relative;
}
.active:after {
	bottom: 0;
	position: absolute;
	left: 0;
	right: 0;
	display: block;
	margin-left: auto;
	margin-right: auto;
	content: "";
	height: 3px;
	width: 100%;
	border-radius: 1000px;
	border-bottom-left-radius: 0px;
	border-bottom-right-radius: 0px;
	background-color: #4299e1;
}
</style>
