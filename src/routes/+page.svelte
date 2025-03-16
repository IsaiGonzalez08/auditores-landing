<script lang="ts">
	import PrimaryButton from '$lib/components/PrimaryButton.svelte';
	import SecondaryButton from '$lib/components/SecondaryButton.svelte';
	import Section from '$lib/components/Section.svelte';

	let information = [
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' },
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' },
		{ title: '20', subtitle: 'Años de', details: 'Experiencia' }
	];
</script>

<main>
	<div class="flex flex-row items-center">
		<div class="pl-15">
			<h1 class="flex flex-col text-5xl leading-14 text-[#A1ADAF]">
				Despacho <span class="font-semibold text-[#397A80]">Gonzalez Ruiz Auditores, S.C.</span>
			</h1>
			<p class="my-10 text-justify text-base tracking-widest">
				Somos un despacho de auditores con más de 20 años de experiencia en la prestación de
				servicios de auditoría, consultoría y asesoramiento fiscal.
			</p>
			<SecondaryButton title="Quienes somos" />
			<div class="mt-10 flex flex-row items-end justify-center gap-4">
				{#each information as item, index}
					<div class="flex flex-col items-center">
						<h2 class="text-5xl font-semibold text-[#397A80]">{item?.title}</h2>
						<span class="flex flex-col items-center font-semibold text-[#A1ADAF]"
							>{item?.subtitle} <span class="text-[#397A80]">{item?.details}</span>
						</span>
					</div>
					{#if index < information.length - 1}
						<div class="bg-primary h-20 w-[1px]"></div>
					{/if}
				{/each}
			</div>
		</div>
		<img class="max-h-[700px] max-w-[700px]" src="/images/init-image.png" alt="init" />
	</div>
	<div class="bg-secondary px-20">
		<Section
			image="auditories_image"
			title="Auditorias"
			showLabel={true}
			details="Servicio para empresas o entidades gubernamentales que opten o estén obligados a dictaminar sus estados financieros, procesos administrativos, políticas y procedimientos, impuestos, obligaciones fiscales y patronales, etc."
			button="Categorías"
		/>
	</div>
	<div class="w-full bg-white px-20">
		<Section
			image="contribution"
			title="Contribución"
			showLabel={true}
			details="Consiste en el análisis de los objetivos de la empresa, para verificar que los procesos que se realizan para alcanzarlos son los más adecuados. Estos proyectos son de un largo alcance, y se realizan conjuntamente con el personal de las empresas."
			button="Categorías"
			reverseRow={true}
		/>
	</div>
	<div class="bg-sidebar flex w-full flex-row items-center pr-20">
		<div class="basis-1/2">
			<img src="/images/asesories.png" alt="asesorias" />
		</div>
		<div class="flex basis-1/2 flex-col items-center">
			<h2 class="font-semibold text-[#397A80] text-4xl">Hablar con un Especialista</h2>
			<p class="text-center tracking-widest py-10">
				Si desea hablar con un especialista para encontrar la solución adecuada para su empresa,
				regístrese para una asesoría gratuita.
			</p>
			<PrimaryButton title="Contactar" />
		</div>
	</div>
</main>
