<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
	import FormField from '$lib/components/contact-us/FormField.svelte';

	let address = [
		'2A Avenida Sur Poniente 1055',
		'Colonia Centro, Tuxtla Gutiérrez Chiapas,',
		'C.P. 29000',
		'+52 961-613-6831',
		'administración@auditoresgz.com'
	];

	let formData = {
		nombre: '',
		apellidos: '',
		servicio: '',
		telefono: '',
		email: '',
		mensaje: ''
	};

	let options = [{ value: 'Auditoría' }, { value: 'Consultoría' }, { value: 'Asesoría' }];
</script>

<SectionHeader title="Contáctanos" image="contact-header" />

<div class="p-20">
	<p class="text-3xl font-semibold text-[#397A80]">Contacto</p>
	<p class="font-light text-[#A1ADAF]">González Ruiz Auditores</p>
	<hr class="bg-primary mt-4 h-0.5 w-full max-w-[500px] border-none" />

	<div class="mt-6 flex flex-col gap-8 sm:flex-row sm:gap-0">
		<div class="flex basis-1/2 flex-col">
			{#each address as item}
				<p class="poppins">{item}</p>
			{/each}
		</div>

		<form class="basis-1/2">
			<div class="flex flex-col sm:flex-row gap-4">
				<FormField label="Nombre(s)" bind:value={formData.nombre} type="text" />
				<FormField label="Apellidos" bind:value={formData.apellidos} type="text" />
			</div>
			<div class="mt-4 flex flex-col sm:flex-row gap-4">
				<div class="flex w-full flex-col gap-2">
					<label class="text-sm font-medium text-[#397A80]" for="">Tipo de servicio</label>
					<select
						bind:value={formData.servicio}
						class="min-h-12 rounded-xl border-none bg-[#F3F3F3]"
					>
						<option class="" value="" disabled selected>Seleccionar</option>
						{#each options as item}
							<option value={item.value}>{item.value}</option>
						{/each}
					</select>
				</div>
				<FormField label="Teléfono" bind:value={formData.telefono} type="tel" />
			</div>
			<div class="mt-4">
				<FormField label="Correo Electrónico" bind:value={formData.email} type="email" />
			</div>
			<div class="mt-4">
				<FormField label="Mensaje" bind:value={formData.mensaje} type="text" textarea={true} />
			</div>
		</form>
	</div>
</div>
