<script lang="ts">
	import { goto } from '$app/navigation';
	import PrimaryButton from './PrimaryButton.svelte';

	const navigateToContact = () => {
		goto('/contact-us/');
	};
</script>

<header class="flex w-full items-center justify-between px-5 py-10 sm:py-0 sm:px-8 xl:px-16 sm:h-32">
	<a href="/"><img src="/icons/logo.svg" alt="auditores-logo" /></a>
	<ul class="hidden cursor-pointer gap-16 font-medium text-[#548BA5] xl:flex">
		<a href="/">Inicio</a>
		<a href="about-us">Nosotros</a>
		<a href="services">Servicios</a>
		<a href="contact-us">Contáctanos</a>
		<a href="softwares">Software fiscal</a>
	</ul>
	<div class="hidden xl:block">
		<PrimaryButton onClick={navigateToContact} title="Asesorías" />
	</div>
	<button class="sm:hidden">
		<img class="w-10" src="/icons/menu.svg" alt="menu" />
	</button>
</header>
