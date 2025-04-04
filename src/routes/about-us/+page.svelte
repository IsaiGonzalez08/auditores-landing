<script lang="ts">
	import SectionHeader from '$lib/components/SectionHeader.svelte';
</script>

<SectionHeader title="Sobre Nosotros" image="about-us" />
<main class="w-full p-10 lg:p-15">
	<div class="flex w-full flex-col-reverse sm:flex-row items-center justify-around gap-15">
		<div class="basis-1/2">
			<img class="rounded-2xl sm:rounded-none h-[400px]" src="/images/about-us-subsection.png" alt="subsection-about" />
		</div>
		<div class="w-full sm:basis-1/2">
			<h2 class="text-3xl font-semibold text-[#397A80]">Sobre Nosotros</h2>
			<p class="font-light text-[#A1ADAF]">González Ruiz Auditores</p>
			<hr class="bg-primary mt-6 h-0.5 w-full border-none" />
			<p class="mt-6 text-justify tracking-widest">
				Nuestra organización se fundó en el año 2002 dando servicios de contabilidad, auditoria,
				impuestos e implementación de soluciones informáticas, que través de una capacitación
				constante hemos logrado ampliar nuestra gama de servicios. <br /> <br /> El equipo de trabajo
				se conforma con profesionales de la contaduría pública con título profesional, egresados de las
				instituciones mas prestigiadas del estado de Chiapas quienes ponemos a su disposición todas nuestras
				capacidades con la mayor ética de nuestra profesión.
			</p>
		</div>
	</div>
	<p class="mt-12 text-justify tracking-widest">
		En el ámbito de la implementación de software estamos asociados con expertos especialistas en
		informática administrativa quienes tienen mas de 25 años de experiencia generando aplicativos
		tecnológicos respetando en todo tiempo la legislación de nuestro país y otorgando la seguridad a
		nuestros clientes del cumplimiento correcto de sus obligaciones en materia fiscal y de seguridad
		social.
	</p>
	<div class="mt-20 flex flex-col lg:flex-row w-full justify-around gap-15">
		<div class="flex w-full flex-col">
			<h2 class="text-2xl font-semibold text-[#397A80]">Misión</h2>
			<hr class="bg-primary h-0.5 w-full border-none" />
			<p class="mt-6 text-justify tracking-widest">
				Nuestra misión es aportar valor a las empresas y personas a través de la prestación de
				nuestros servicios profesionales de alta calidad, con integridad, objetividad e
				independencia, para ayudar a nuestros clientes a mejorar su desempeño y alcanzar sus
				objetivos, manteniendo la confianza y satisfacción.
			</p>
			<div class="flex justify-center items-end">
				<img class="w-48 h-48 mt-12" src="/images/mision.png" alt="mision">
			</div>
		</div>
		<div class="flex w-full flex-col">
			<h2 class="text-2xl font-semibold text-[#397A80]">Visión</h2>
			<hr class="bg-primary h-0.5 w-full border-none" />
			<p class="mt-6 text-justify tracking-widest">
				Ser una firma de profesionales que sea un referente en los servicios de auditoría y
				consultoría proporcionando soluciones innovadoras que ayuden a nuestros clientes en su
				entorno fiscal, así como en la implementación de herramientas tecnológicas para la gestión
				de negocios a través de compartir nuestra experiencia en las diversas áreas de operación de
				las empresas.
			</p>
			<div class="flex justify-center">
				<img class="w-48 h-48 mt-4" src="/images/vision.png" alt="vision">
			</div>
		</div>
	</div>
</main>
