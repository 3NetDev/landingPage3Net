<template>
	<div class="col-12 d-flex justify-content-center">
		<section id="autoAtendimento" class="col-12 content">
			<h1>AUTO ATENDIMENTO 3NET PARA CLIENTES</h1>
			<p>Resolva tudo o que você precisa e tire suas dúvidas sobre serviços 3NetTelecom de maneira fácil em poucos cliques.</p>
	
			<div class="d-flex content-cards row">
				<a 
					v-for="(card, index) in listCards"
					:key="index"
					class="d-flex"
					:href="card.link"
					target="_blank"
				>
					<div 
						class="card d-flex flex-column align-items-center p-4 col-auto" 
					>
						<i :class="card.class"></i>
						<h3>{{ card.title }}</h3>
						<div class="d-flex flex-column justify-content-start">
							<hr />
							<span>{{ card.description }}</span>
						</div>
					</div>
	
				</a>
			</div>
	
		</section>
	</div>
</template>

<script>
export default {
	data() {
		return {
			listCards: [
				{
					class: 'fa-solid fa-file-invoice-dollar',
					title: 'FATURA',
					description: '2º via da fatura',
					link: 'https://api.whatsapp.com/send?phone=5512974075710&text=Ol%C3%A1%2C%20preciso%20da%20segunda%20via%20da%20minha%20fatura'
				},
				{
					class: 'fa-solid fa-gauge',
					title: 'VELOCIDADE',
					description: 'Confira sua velocidade com o medidor de velocidade',
					link: 'https://www.speedtest.net/pt'
				},
				{
					class: 'fa-solid fa-headset',
					title: 'SUPORTE',
					description: 'Atendimento personalizado ao cliente',
					link: 'https://api.whatsapp.com/send?phone=5512974075710&text=Ola%2C%20estou%20precisando%20de%20ajuda'
				},
				{
					class: 'fa-solid fa-user',
					title: 'CENTRAL DO ASSINANTE',
					description: 'Acesse a central do assinante',
					link: 'http://186.236.66.96:8000/accounts/central/login'
				},

			]
		}
	},
	methods: {
		
	}
}
</script>

<style>

</style>