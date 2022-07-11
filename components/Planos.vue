<template>
	<section id="planos" class="d-flex flex-column align-items-center">
		<h1>NOSSOS PLANOS</h1>
		<div class="col-9 d-flex justify-content-around">
			<div class="card d-flex flex-column align-items-center " v-for="plano in listPlanos" :key="plano.velocidade">
				<h3>
					<span>{{ plano.velocidade }}</span> 
					<br>
					MEGAS
				</h3>
				
				<div class="d-flex flex-column content-card">
					<span>Instalação gratuita</span>
					<hr>
					<span>Equipamento 5G</span>
					<hr>
					<p>R$ <span>{{ plano.valor.split(',')[0] }}</span>,{{ plano.valor.split(',')[1] }} / MÊS</p>
				</div>

				<a class="link" href="/contato" >
					ASSINAR
				</a>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	data() {
		return {
			listPlanos: [
				{
					velocidade: 100,
					valor: '69,99'
				},
				{
					velocidade: 200,
					valor: '79,90'
				},
				{
					velocidade: 300,
					valor: '89,90'
				}
			]
		}
	}
}
</script>

<style>

</style>