<template>
	<div class="h-screen flex w-full">
		<TheSideMenu />
		<div class="flex-1 w-full">
			<TheNavigation />
			<div :class="{
				'mt-32':fixedNavBar,
				'mt-0':!fixedNavBar,
			}">
				<router-view />
			</div>
			<!-- <TheFooter /> -->
		</div>
	</div>
</template>

<script>
import TheNavigation from "@/components/TheNavigation";
import TheSideMenu from "@/components/TheSideMenu";
// import TheFooter from "@/components/TheFooter";

export default {
	components: {
		TheNavigation,
		TheSideMenu
		// TheFooter
	},
	data() {
		return {
			sidemenu: false,
			sideMenuLogo: true,
			sideMenuIcons: true,
			fixedNavBar: false
		};
	},
	methods: {
		toggleSideMenu() {
			this.sidemenu = !this.sidemenu;
		}
	}
};
</script>

<style lang="scss">
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	// text-align: center;
	// color: #2c3e50;
}
</style>
