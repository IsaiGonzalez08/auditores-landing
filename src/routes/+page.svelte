<script lang="ts">
	import { goto } from '$app/navigation';
	import PrimaryButton from '$lib/components/PrimaryButton.svelte';
	import SecondaryButton from '$lib/components/SecondaryButton.svelte';
	import Section from '$lib/components/init/SectionDetails.svelte';

	let information = [
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' },
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' },
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' }
	];

	const navigateToContact = () => {
		goto('/contact-us');
	};

	const navigateToAbout = () => {
		goto('/about-us');
	};

	const navigateToServices = () => {
		goto('/services');
	};
</script>

<main>
	<div class="flex flex-row items-center p-7 lg:p-0">
		<div class="lg:pl-15">
			<h1
				class="flex flex-col text-center text-4xl leading-10 text-[#A1ADAF] sm:text-5xl sm:leading-14 lg:text-start"
			>
				Despacho <span class="font-semibold text-[#397A80]">Gonzalez Ruiz Auditores, S.C.</span>
			</h1>
			<p class="my-10 text-center text-sm tracking-widest sm:text-base lg:text-start">
				Somos un despacho de auditores con más de 20 años de experiencia en la prestación de
				servicios de auditoría, consultoría y asesoramiento fiscal.
			</p>
			<div class="flex justify-center lg:justify-start">
				<SecondaryButton title="Quienes somos" onClick={navigateToAbout} />
			</div>
			<div class="mt-10 flex flex-row items-end justify-center gap-4 lg:justify-start">
				{#each information as item, index}
					<div class="flex flex-col items-center">
						<h2 class="text-4xl font-semibold text-[#397A80] sm:text-5xl">{item?.title}</h2>
						<span
							class="flex flex-col items-center text-sm font-semibold text-[#A1ADAF] sm:text-base"
							>{item?.subtitle} <span class="text-[#397A80]">{item?.details}</span>
						</span>
					</div>
					{#if index < information.length - 1}
						<div class="bg-primary h-20 w-[1px]"></div>
					{/if}
				{/each}
			</div>
		</div>
		<img
			class="hidden h-[550px] w-[500px] lg:block xl:h-[700px] xl:w-[700px]"
			src="/images/init-image.png"
			alt="init"
		/>
	</div>
	<div class="bg-[#F3F3F3] xl:px-15">
		<Section
			image="auditories_image"
			title="Auditorias"
			showLabel={true}
			details="Servicio para empresas o entidades gubernamentales que opten o estén obligados a dictaminar sus estados financieros, procesos administrativos, políticas y procedimientos, impuestos, obligaciones fiscales y patronales, etc."
			button="Categorías"
			onClick={navigateToServices}
		/>
	</div>
	<div class="w-full bg-white xl:px-15">
		<Section
			image="contribution"
			title="Contribución"
			showLabel={true}
			details="Consiste en el análisis de los objetivos de la empresa, para verificar que los procesos que se realizan para alcanzarlos son los más adecuados. Estos proyectos son de un largo alcance, y se realizan conjuntamente con el personal de las empresas."
			button="Categorías"
			reverseRow={true}
			onClick={navigateToServices}
		/>
	</div>
	<div class="bg-sidebar flex w-full flex-row items-center justify-center p-7 lg:p-0 xl:pr-20">
		<div class="hidden basis-1/2 lg:block">
			<img src="/images/asesories.png" alt="asesorias" />
		</div>
		<div class="flex w-full flex-col items-center lg:basis-1/2">
			<h2 class="text-center text-4xl font-semibold text-[#397A80]">Hablar con un Especialista</h2>
			<p class="py-5 md:py-10 lg:py-5 text-center text-sm sm:text-base tracking-widest">
				Si desea hablar con un especialista para encontrar la solución adecuada para su empresa,
				regístrese para una asesoría gratuita.
			</p>
			<PrimaryButton onClick={navigateToContact} title="Contactar" />
		</div>
	</div>
</main>
