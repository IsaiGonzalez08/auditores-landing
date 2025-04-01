<script lang="ts">
	import PrimaryButton from './PrimaryButton.svelte';
</script>

<header class="flex w-full items-center justify-between px-16 sm:h-32">
	<a href="/"><img src="/icons/logo.svg" alt="auditores-logo" /></a>
	<ul class="flex cursor-pointer gap-16 font-medium text-[#548BA5]">
		<a href="/">Inicio</a>
		<a href="about-us">Nosotros</a>
		<li>Servicios</li>
		<li>Contáctanos</li>
		<li>Software fiscal</li>
	</ul>
	<PrimaryButton title="Asesorías" />
</header>
