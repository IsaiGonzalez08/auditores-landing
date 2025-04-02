<script lang="ts">
	let { title, image } = $props();
</script>

<div class="flex w-full flex-row justify-center sm:justify-between bg-[#F3F3F3]">
	<div class="flex basis-1/2 items-center justify-center text-4xl font-semibold text-[#397A80]  min-h-40">
		{title}
	</div>
	<div class="hidden md:flex basis-1/2 justify-end">
		<img class="max-h-[400px]" src="/images/{image}.png" alt="{image}" />
	</div>
</div>
