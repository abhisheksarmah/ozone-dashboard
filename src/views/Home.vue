<template>
	<div class="md:max-w-6xl md:mx-auto px-4 py-8">
		<div class="flex items-center justify-between mb-4">
			<h2 class="text-xl font-bold text-gray-800">Dashboard</h2>
		</div>

		<div class="flex flex-wrap -mx-2 md:-mx-4 mb-6">
			<template
				v-for="menu in menus"
				:key="menu"
			>
				<div class="w-1/2 md:w-1/4 px-2 md:px-4 mb-4">
					<Widget :detail="menu" />
				</div>
			</template>
		</div>

		<div class="flex items-start justify-between mb-4">
			<div>
				<p class="text-xl font-bold text-gray-800">
					Invoice Details
				</p>
				<p class="text-base text-gray-600 leading-normal">
					on Wed 23 Sep, 2020
				</p>
			</div>

			<button class="shadow inline-flex items-center bg-blue-500 hover:bg-blue-600 focus:outline-none focus:shadow-outline text-white font-semibold py-2 px-4 rounded-lg">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="mr-2 w-5 h-5"
					viewBox="0 0 24 24"
					stroke-width="2"
					stroke="currentColor"
					fill="none"
					stroke-linecap="round"
					stroke-linejoin="round"
				>
					<rect
						x="0"
						y="0"
						width="24"
						height="24"
						stroke="none"
					></rect>
					<line
						x1="12"
						y1="5"
						x2="12"
						y2="19"
					/>
					<line
						x1="5"
						y1="12"
						x2="19"
						y2="12"
					/>
				</svg>
				Create Invoice
			</button>
		</div>
		<div class="flex flex-wrap -mx-4 mb-6">
			<div class="w-full md:w-1/3 px-4 flex-grow mb-5 md:mb-0">
				<div class="shadow w-full rounded-lg bg-white overflow-hidden w-full block">
					<div class="px-8 py-6">
						<div class="flex flex-wrap items-center md:block md:mt-5">
							<div class="overflow-hidden relative w-32 h-32 md:w-40 md:h-40 rounded-full bg-blue-100 mx-auto md:mb-6">
								<div
									class="mb-8 md:mb-12 absolute left-0 right-0 mx-auto bottom-0"
									style="z-index: 1"
								>
									<div class="bg-blue-600 mx-auto rounded-lg relative w-20 py-2 border-2 border-blue-100">
										<div
											class="h-8 bg-orange-500 w-8 rounded absolute left-0 top-0 -mt-3 ml-4"
											style="transform: rotate(-45deg); z-index: -1;"
										></div>
										<div
											class="h-8 bg-orange-600 w-8 rounded absolute left-0 top-0 -mt-3 ml-8"
											style="transform: rotate(-12deg); z-index: -2;"
										></div>

										<div class="flex items-center justify-center h-6 bg-blue-600 w-6 rounded-l-lg ml-auto border-4 border-blue-100 -mr-1">
											<div class="h-2 w-2 rounded-full bg-blue-600 border-2 border-blue-100"></div>
										</div>

										<div class="w-8 h-8 bg-orange-500 border-4 border-blue-100 rounded-full -ml-3 -mb-5"></div>
									</div>
								</div>
							</div>
							<div class="flex-1">
								<p class="text-4xl md:text-6xl text-gray-700 leading-none font-bold tracking-tight font-sans mb-3 md:hidden text-center">
									₹123.00
								</p>
								<p class="text-2xl md:text-3xl text-gray-700 font-bold leading-tight font-sans mb-3 hidden md:block text-center tracking-tight">
									₹123.00
								</p>
								<p class="text-gray-500 text-sm font-bold tracking-wider uppercase text-center">
									Total Invoice Amount
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="w-full md:w-2/3 px-4 flex-grow">
				<div class="overflow-x-auto bg-white rounded-lg shadow">
					<table class="w-full whitespace-no-wrap bg-white overflow-hidden table-striped">
						<thead>
							<tr class="text-left">
								<th class="px-6 py-3 text-gray-500 font-bold tracking-wider uppercase text-xs">
									Invoice
								</th>
								<th class="px-6 py-3 text-gray-500 font-bold tracking-wider uppercase text-xs">
									Name
								</th>
								<th class="px-6 py-3 text-gray-500 font-bold tracking-wider uppercase text-xs">
									Date
								</th>
								<th class="px-6 py-3 text-gray-500 font-bold tracking-wider uppercase text-xs text-right">
									Amount
								</th>
								<th class="px-6 py-3 text-gray-500 font-bold tracking-wider uppercase text-xs">
									Status
								</th>
							</tr>
						</thead>
						<tbody>
							<tr class="focus-within:bg-gray-200 overflow-hidden">
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">#IN12345</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">ABC Company</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">10 Sep 2018</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center justify-end">₹12,000.00</span>
								</td>
								<td class="border-t">
									<span class="px-6 py-4 flex items-center">
										<span class="px-2 rounded-full text-sm uppercase tracking-wide font-semibold bg-green-200 text-green-800">Completed</span>
									</span>
								</td>
							</tr>

							<tr class="focus-within:bg-gray-200 overflow-hidden">
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">#IN12344</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">XYZ Company</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">8 Sep 2018</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center justify-end">₹10,000.00</span>
								</td>
								<td class="border-t">
									<span class="px-6 py-4 flex items-center">
										<span class="px-2 rounded-full text-sm uppercase tracking-wide font-semibold bg-orange-200 text-orange-800">Pending</span>
									</span>
								</td>
							</tr>

							<tr class="focus-within:bg-gray-200 overflow-hidden">
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">#IN12343</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">CAC Company</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">7 Sep 2018</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center justify-end">₹10,000.00</span>
								</td>
								<td class="border-t">
									<span class="px-6 py-4 flex items-center">
										<span class="px-2 rounded-full text-sm uppercase tracking-wide font-semibold bg-blue-200 text-blue-800">Processing</span>
									</span>
								</td>
							</tr>

							<tr class="focus-within:bg-gray-200 overflow-hidden">
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">#IN12345</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">ABC Company</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">10 Sep 2018</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center justify-end">₹12,000.00</span>
								</td>
								<td class="border-t">
									<span class="px-6 py-4 flex items-center">
										<span class="px-2 rounded-full text-sm uppercase tracking-wide font-semibold bg-green-200 text-green-800">Completed</span>
									</span>
								</td>
							</tr>

							<tr class="focus-within:bg-gray-200 overflow-hidden">
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">#IN12344</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">XYZ Company</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center">8 Sep 2018</span>
								</td>
								<td class="border-t">
									<span class="text-gray-700 px-6 py-4 flex items-center justify-end">₹10,000.00</span>
								</td>
								<td class="border-t">
									<span class="px-6 py-4 flex items-center">
										<span class="px-2 rounded-full text-sm uppercase tracking-wide font-semibold bg-orange-200 text-orange-800">Pending</span>
									</span>
								</td>
							</tr>
						</tbody>
					</table>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Widget from "@/components/Widget";
import { menu_items } from "../services.js";
export default {
	name: "Home",
	components: {
		Widget
	},
	data() {
		return {
			menus: menu_items.filter(menu =>
				["analytics", "invoice", "tracking", "history"].includes(
					menu.icon
				)
			)
		};
	}
};
</script>
