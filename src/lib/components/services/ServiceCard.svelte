<script lang="ts">
	import { goto } from '$app/navigation';

	let { image, title, details, tags } = $props();

	const navigateToContact = () => {
		goto('/contact-us');
	};
</script>

<div class="flex h-max w-80 flex-col rounded-2xl border-2 border-[#397a80]">
	<img class="max-h-44 rounded-t-[14px]" src="/images/{image}.png" alt="card" />
	<div class="flex flex-col gap-2 p-4">
		<h2 class="min-h-14 text-xl font-semibold text-[#397A80]">{title}</h2>
		<p class="min-h-20 text-sm font-light tracking-widest">{details}</p>
		<div class="flex flex-row gap-2">
			{#each tags as item}
				<div class="bg-primary flex w-28 justify-center rounded-[20px] py-1">
					<p class="text-xs font-medium text-white">{item}</p>
				</div>
			{/each}
		</div>
		<button
			onclick={navigateToContact}
			class="flex w-28 flex-row items-center justify-center gap-1 rounded-[20px] border-2 border-[#397a80] px-3 py-1"
		>
			<span class="text-xs font-bold text-[#397a80]">Contactar</span>
			<img src="/icons/Forward.svg" alt="forward" />
		</button>
	</div>
</div>
