<template>
	<div class="md:max-w-6xl md:mx-auto px-4 py-8">
		<div class="mb-4">
			<p class="text-xl font-bold text-gray-800">
				Settings
			</p>
		</div>

		<div class="bg-white shadow rounded-lg p-5">
			<div class="flex flex-wrap -mx-4">
				<div class="w-full md:w-1/3 px-4">
					<h2 class="font-bold text-xl text-gray-800">Application Settings</h2>
					<p class="text-muted mb-4 text-sm">
						Settings for ozone admin panel.
					</p>
				</div>
				<div class="w-full md:w-1/2 px-4">
					<div class="mb-5 flex justify-between items-center">
						<label
							for="sidemenu"
							class="flex items-start justify-between cursor-pointer w-full"
						>
							<!-- label -->
							<div>
								<div class="mb-1 font-semibold text-gray-700">
									Side Menu
								</div>
								<p class="text-muted mb-4 text-sm">
									show or hide the side menu
								</p>
							</div>
							<!-- toggle -->
							<div class="relative">
								<!-- input -->
								<input
									id="sidemenu"
									type="checkbox"
									class="hidden"
									v-model="$root.sidemenu"
								/>
								<!-- line -->
								<div class="toggle__line w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
								<!-- dot -->
								<div class="toggle__dot absolute w-6 h-6 bg-white rounded-full shadow inset-y-0 left-0"></div>
							</div>
						</label>
					</div>

					<div class="mb-5 flex justify-between items-center">
						<label
							for="sidemenulogo"
							class="flex items-start justify-between cursor-pointer w-full"
						>
							<!-- label -->
							<div>
								<div class="mb-1 font-semibold text-gray-700">
									Side Menu Logo
								</div>
								<p class="text-muted mb-4 text-sm">
									show or hide the sidemenu logo
								</p>
							</div>
							<!-- toggle -->
							<div class="relative">
								<!-- input -->
								<input
									id="sidemenulogo"
									type="checkbox"
									class="hidden"
									v-model="$root.sideMenuLogo"
								/>
								<!-- line -->
								<div class="toggle__line w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
								<!-- dot -->
								<div class="toggle__dot absolute w-6 h-6 bg-white rounded-full shadow inset-y-0 left-0"></div>
							</div>
						</label>
					</div>

					<div class="mb-5 flex justify-between items-start w-full">
						<div>
							<div class="mb-1 font-semibold text-gray-700">
								Fixed Nav Bar
							</div>
							<p class="text-muted mb-4 text-sm">
								keep the navigation menu on top
							</p>
						</div>
						<label
							for="fixednavbar"
							class="cursor-pointer"
						>
							<!-- toggle -->
							<div class="relative">
								<!-- input -->
								<input
									id="fixednavbar"
									type="checkbox"
									class="hidden"
									v-model="$root.fixedNavBar"
								/>
								<!-- line -->
								<div class="toggle__line w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
								<!-- dot -->
								<div class="toggle__dot absolute w-6 h-6 bg-white rounded-full shadow inset-y-0 left-0"></div>
							</div>
						</label>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="css" scoped>
.toggle__dot {
	top: -0.25rem;
	left: -0.25rem;
	@apply transform ease-in-out duration-300;
}

input:checked ~ .toggle__dot {
	@apply bg-blue-600 translate-x-full;
}
</style>
