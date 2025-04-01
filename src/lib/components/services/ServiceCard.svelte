<script lang="ts">
	let { image, title, details, tags } = $props();
</script>

<div class="flex h-[420px] w-[378px] flex-col rounded-2xl border-2 border-[#397a80]">
	<img class="h-[180px] rounded-t-[14px]" src="/images/{image}.png" alt="card" />
	<div class="p-5">
		<h2 class="text-xl font-semibold text-[#397A80]">{title}</h2>
		<p class="mt-2 text-sm font-light tracking-widest">{details}</p>
		<div class="mt-3 flex flex-row gap-2">
			{#each tags as item}
				<div class="bg-primary flex w-28 justify-center rounded-[20px] py-1">
					<p class="text-xs font-medium text-white">{item}</p>
				</div>
			{/each}
		</div>
		<button
			class="mt-6 flex flex-row items-center justify-center gap-1 rounded-[20px] border-2 border-[#397a80] px-3 py-1"
		>
			<span class="text-xs font-bold text-[#397a80]">Contactar</span>
			<img src="/icons/Forward.svg" alt="forward" />
		</button>
	</div>
</div>
