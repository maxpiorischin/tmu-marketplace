<script lang="ts">
	export let title: string;
	export let description: string;
	export let date: string;
	export let price: number;
	export let profile_image: string;
	export let images: string[];
	export let user: string;
</script>

<div class="w-[300px] place-self-center rounded-lg bg-white shadow-lg">
	<div class="relative h-[250px] w-[300px] rounded-t-lg">
		<img src={images[0]} alt={title} class="h-[250px] w-[300px] rounded-t-lg object-cover" />
		<div
			class="absolute bottom-3 left-3 flex items-center space-x-2 rounded-lg bg-white bg-opacity-70 p-2"
		>
			<img src={profile_image} alt={user} class="h-6 w-6" />
			<p class="pr-1 text-xs font-medium text-gray-900">{user}</p>
		</div>
	</div>

	<div class="p-5">
		<h2 class="mb-2 line-clamp-1 text-xl font-medium text-gray-900">
			{title}
		</h2>

		<p class="mb-4 line-clamp-2 min-h-10 text-sm font-normal text-gray-700">
			{description}
		</p>

		<div class="flex items-center justify-between">
			<p class="text-sm font-medium text-gray-700">${price.toFixed(2)}</p>

			<button
				class="rounded-lg bg-blue-600 px-3 py-1.5 text-sm font-normal text-white hover:bg-blue-700"
			>
				Contact
				<i class="fa-solid fa-message ml-2"></i>
			</button>
		</div>
	</div>
</div>