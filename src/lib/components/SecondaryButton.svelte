<script lang="ts">
	let { title, onClick } = $props();
</script>

<button
	onclick={onClick}
	class="cursor-pointer rounded-xl border-2 border-[#397A80] px-10 py-3 font-semibold text-[#397A80]"
>
	{title}
</button>
