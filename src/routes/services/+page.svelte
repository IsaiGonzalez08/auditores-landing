<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import ServiceCard from '$lib/components/services/ServiceCard.svelte';

	let servicesCards = [
		{
			title: 'Auditorias',
			services: [
				{
					image: 'audit-card1',
					title: 'Auditoría financiera',
					details:
						'Revisamos los estados financieros y asi obtener un base sobre la cual emitiremos una opinión evaluando su razonabilidad.',
					tags: ['Auditoría', 'Finanzas']
				},
				{
					image: 'audit-card2',
					title: 'Auditoría fiscal',
					details:
						'Se realiza para empresas que opten a dictaminar sus estados financieros de acuerdo con el Código Fiscal.',
					tags: ['Auditoría']
				},
				{
					image: 'audit-card3',
					title: 'Auditoría de IMSS',
					details:
						'Se centra en analizar los procesos administrativos en empresas para verificar que lleven a cabo sus operaciones.',
					tags: ['Auditoría']
				}
			]
		},
		{
			title: 'Dictamenes',
			services: [
				{
					image: 'dicta-card1',
					title: 'Dictamen de enajenación de acciones',
					details: 'Realizamos servicios de valuación de empresas.',
					tags: ['Contribución', 'Finanzas']
				}
			]
		},
		{
			title: 'Otros Servicios',
			services: [
				{
					image: 'serv-card1',
					title: 'Contabilidad general',
					details:
						'Realizamos servicios de valuación de empresas o de activos, para diferentes objetivos.',
					tags: ['Contribución', 'Finanzas']
				},
				{
					image: 'serv-card2',
					title: 'Determinación de cuotas al IMSS',
					details:
						'Servicios en procesos de liquidación, incluyendo que nuestros socios funjan como liquidadores.',
					tags: ['Contribución', 'Finanzas']
				},
				{
					image: 'serv-card3',
					title: 'Determinación de impuestos locales',
					details: 'Soluciones en este aspecto, análisis de los objetivos de las empresas.',
					tags: ['Contribución']
				}
			]
		}
	];
</script>

<SectionHeader title="Servicios" image="services-header" />

<div class="p-5 md:p-8 xl:p-15">
	{#if servicesCards.length}
		<div class="flex flex-col">
			{#each servicesCards as item}
				<p class="text-3xl font-semibold text-[#397A80]">{item.title}</p>
				<p class="font-light text-[#A1ADAF]">González Ruiz Auditores</p>
				<hr class="bg-primary mt-4 h-0.5 w-full max-w-[500px] border-none" />
				{#if item.services.length}
					<div class="my-14 flex justify-center sm:justify-start">
						<div class="grid-rows grid grid-cols-1 gap-10 md:grid-cols-2 lg:grid-cols-3">
							{#each item.services as card}
								<ServiceCard
									image={card.image}
									title={card.title}
									details={card.details}
									tags={card.tags}
								/>
							{/each}
						</div>
					</div>
				{/if}
			{/each}
		</div>
	{/if}
</div>
