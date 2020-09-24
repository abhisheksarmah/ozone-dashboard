<template>
	<a
		role="button"
		@click="$router.push(detail.url)"
		class="shadow rounded-lg bg-white overflow-hidden block"
	>
		<div class="px-8 py-6">
			<p class="mb-3 text-center text-gray-500">
				<Icon :name="detail.icon" />
			</p>
			<p class="text-gray-500 text-sm font-bold tracking-wider uppercase ">
				{{ detail.name }}
			</p>
		</div>
	</a>
</template>

<script>
import Icon from "@/components/Icon";
export default {
	components: {
		Icon
	},
	props: ["detail"]
};
</script>

<style lang="scss" scoped></style>
