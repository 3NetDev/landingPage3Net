<template>
	<section id="planos" class="d-flex flex-column align-items-center">
		<h1>NOSSOS PLANOS</h1>

		<div class="content-planos d-flex row col-12 justify-content-center">
			<div class="d-flex align-items-center">
				<i v-on:click="backStep" class="fa-solid fa-angle-left"></i>
			</div>

			<div class="card-planos flex-column align-items-center" v-for="plano in listPlanos" :key="plano.velocidade">
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
					<div class="d-flex align-items-center">
						<span class="plus">+</span>
						<img src="./../static/media/pamontLogoDark.png"/>
					</div>
					<span>por R$ 9,90</span>
				</div>

				<a class="link d-flex flex-column" href="/contato" >
					<b>ASSINAR</b>
					<span>
						Fidelidade de 12 meses*
					</span>
				</a>
			</div>

			<div class="d-flex align-items-center">
				<i v-on:click="nextStep" class="fa-solid fa-angle-right"></i>
			</div>
		</div>

		<div class="justify-content-between content-step">
			<div class="step active"></div>
			<div class="step"></div>
			<div class="step"></div>
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
					valor: '69,90'
				},
				{
					velocidade: 200,
					valor: '79,90'
				},
				{
					velocidade: 300,
					valor: '89,90'
				}
			],
			step: 0
		}
	},
	methods: {
		nextStep() {
			this.step += 1;

			if (this.step < 3) {
				let dataCards = document.querySelectorAll('.card-planos');
				dataCards.forEach((doc, index) => {
					doc.style.display = this.step === index 
					? 'flex'
					: 'none';
	
					document.querySelectorAll('.step')[index].className = this.step === index ? 'step active' : 'step';
				});
			}
			if (this.step === 2) document.querySelector('.fa-angle-right').style.visibility = 'hidden';

			if (this.step > 0) document.querySelector('.fa-angle-left').style.visibility = 'visible';
		},
		backStep() {
			this.step -= 1;

			let dataCards = document.querySelectorAll('.card-planos');
			dataCards.forEach((doc, index) => {
				doc.style.display = this.step === index 
				? 'flex'
				: 'none';

				document.querySelectorAll('.step')[index].className = this.step === index ? 'step active' : 'step';
			});

			if (this.step === 0) document.querySelector('.fa-angle-left').style.visibility = 'hidden';

			if (this.step < 2) document.querySelector('.fa-angle-right').style.visibility = 'visible';

		}
	}
}
</script>

<style>

</style>