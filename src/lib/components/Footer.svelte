<script lang="ts">
	let address = [
		'2A Avenida Sur Poniente 1055',
		'Colonia Centro, Tuxtla Gutiérrez Chiapas,',
		'C.P. 29000',
		'+52 961-613-6831',
		'administración@auditoresgz.com'
	];

	let services = [
		'Auditoria Fiscal',
		'Auditoría Financiera',
		'Auditoría IMSS',
		'Contabilidad General',
		'Preparación de estados financieros.',
		'Determinación de impuestos federales ante el SAT',
		'Determinación de impuestos locales',
		'Determinación de cuotas al IMSS'
	];

	let socialNetworks = ['Facebook', 'LinkedIn'];
</script>

<footer class="flex min-h-80 w-full flex-col bg-[#F3F3F3] px-5 py-10 sm:px-8">
	<div class="flex flex-col gap-10 xl:flex-row lg:gap-24">
		<div class="flex flex-col md:flex-row gap-10">
			<div class="flex flex-col">
				<div class="flex flex-row items-center gap-3.5">
					<img class="h-10 w-12" src="/icons/logo.svg" alt="logo" />
					<span class="text-xs font-semibold text-[#548BA5]">
						Auditores <span class="text-[#52ADB6]">GZ</span>
					</span>
				</div>
				<div class="mt-6">
					{#each address as item}
						<p class="poppins mt-3 text-xs">{item}</p>
					{/each}
				</div>
			</div>
			<div class="flex flex-grow flex-col">
				<h2 class="mb-5 font-semibold text-[#397A80]">Servicios</h2>
				<hr class="bg-primary h-0.5" />
				<ul
					class="font-poppins mt-6 grid list-outside list-disc grid-flow-col grid-rows-4 gap-x-8 gap-y-4 text-sm pl-5"
				>
					{#each services as item}
						<li>{item}</li>
					{/each}
				</ul>
			</div>
		</div>
		<div class="flex flex-grow flex-col">
			<h2 class="mb-5 font-semibold text-[#397A80]">Redes Sociales</h2>
			<hr class="bg-primary h-0.5" />
			<div class="mt-6 flex flex-col gap-3">
				{#each socialNetworks as item}
					<div class="flex flex-row items-center gap-2.5">
						<img class="h-8 w-8 object-cover" src="/icons/{item}.svg" alt={item} />
						<h2 class="font-normal">{item}</h2>
					</div>
				{/each}
			</div>
		</div>
	</div>
	<div class="mt-6.5">
		<hr class="bg-primary hidden h-0.5 lg:block" />
		<h4 class="font-poppins mt-4 text-xs text-[#777575]">©2025 Auditores GZ.</h4>
	</div>
</footer>
