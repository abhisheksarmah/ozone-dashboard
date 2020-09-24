<template>
	<div class="md:hidden">
		<div
			@click="$parent.sidemenu = false"
			class="fixed inset-0 z-30 bg-gray-600 opacity-0 pointer-events-none transition-opacity ease-linear duration-300"
			:class="{
				'opacity-75 pointer-events-auto': $parent.sidemenu,
				'opacity-0 pointer-events-none': !$parent.sidemenu,
			}"
		></div>

		<!-- Small Screen Menu -->
		<div
			class="fixed inset-y-0 left-0 flex flex-col z-40 max-w-xs w-full bg-white transform ease-in-out duration-300 translate-x-0"
			:class="{
				'translate-x-0': $parent.sidemenu,
				'-translate-x-full': !$parent.sidemenu,
			}"
		>
			<!-- Brand Logo / Name -->
			<div class="flex items-center px-6 py-3 h-16">
				<div class="text-2xl font-bold tracking-tight text-gray-800">
					Ozone Admin.
				</div>
			</div>
			<!-- @end Brand Logo / Name -->

			<div
				class="px-4 py-2 flex-1 h-0 overflow-y-auto"
				:class="{
					'mt-16':$parent.fixedNavBar,
					'mt-0':!$parent.fixedNavBar,
				}"
			>
				<ul>
					<li
						v-for="item in menus"
						:key="item"
					>
						<router-link
							v-if="item.url != '#'"
							:to="item.url"
							class="mb-1 px-2 py-2 rounded-lg flex items-center font-medium text-gray-600 hover:text-blue-600 hover:bg-gray-200"
						>
							<Icon
								:name="item.icon"
								class="mr-4"
							/>
							{{ item.name }}
						</router-link>
						<a
							href="#"
							v-else
							class="mb-1 px-2 py-2 rounded-lg flex items-center font-medium text-gray-600 hover:text-blue-600 hover:bg-gray-200"
						>
							<Icon
								:name="item.icon"
								class="mr-4"
							/>
							{{ item.name }}
						</a>
					</li>
				</ul>
			</div>
		</div>
		<!-- @end Small Screen Menu -->
	</div>
	<!-- Menu Above Medium Screen -->
	<div
		class="bg-white w-0 min-h-screen overflow-y-auto hidden md:block shadow relative z-30 transform ease-in-out duration-300 translate-x-0"
		:class="{
      'translate-x-0 w-64': $parent.sidemenu,
      '-translate-x-full w-0': !$parent.sidemenu,
    }"
	>
		<!-- Brand Logo / Name -->
		<div
			class="flex items-center px-6 py-3 h-16"
			v-if="$parent.sideMenuLogo"
		>
			<div class="text-2xl font-bold tracking-tight text-gray-800">
				Ozone Admin.
			</div>
		</div>
		<!-- @end Brand Logo / Name -->

		<div class="px-4 py-2">
			<ul>
				<li
					v-for="item in menus"
					:key="item"
				>
					<router-link
						v-if="item.url != '#'"
						:to="item.url"
						class="mb-1 px-2 py-2 rounded-lg flex items-center font-medium text-gray-600 hover:text-blue-600 hover:bg-gray-200"
					>
						<Icon
							:name="item.icon"
							class="mr-4"
						/>
						{{ item.name }}
					</router-link>
					<a
						href="#"
						v-else
						class="mb-1 px-2 py-2 rounded-lg flex items-center font-medium text-gray-600 hover:text-blue-600 hover:bg-gray-200"
					>
						<Icon
							:name="item.icon"
							class="mr-4"
						/>
						{{ item.name }}
					</a>
				</li>
			</ul>
		</div>
	</div>
	<!-- @end Menu Above Medium Screen -->
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
			menus: menu_items
		};
	}
};
</script>
