<script lang>
	let { image, title, details } = $props();
</script>

<div class="flex flex-row w-full bg-[#FAFAFA] gap-16 p-5 rounded-3xl hover:scale-105 hover:duration-500 transition-all">
	<img class="w-36 h-36" src="/images/{image}.png" alt="software-card" />
	<div class="flex flex-col gap-6">
        <h2 class="font-semibold text-2xl">{title}</h2>
        <p class="tracking-widest">{details}</p>
    </div>
</div>
