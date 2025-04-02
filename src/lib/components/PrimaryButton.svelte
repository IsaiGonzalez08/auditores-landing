<script lang="ts">
	let { title, onClick } = $props();
</script>

<button onclick={onClick} class="bg-primary rounded-xl px-6 py-2 font-semibold text-[#FCFEFE] cursor-pointer">
	{title}
</button>
