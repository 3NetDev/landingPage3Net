<template>
	<header class="d-flex justify-content-between">
		<img src="@/static/media/logo.png" alt="Logo" class="col-1">
		<nav class="d-flex align-items-end p-0 m-0 col-7">
			<ul class="d-flex col-12 justify-content-between p-0 m-0">
				<li> <a href="/">Início</a> </li>
				<li @click="scrollTo"> Planos </li>
				<li> <a href="http://186.236.66.96:8000/accounts/central/login" target="_blank"> Central do cliente </a> </li>
				<li> <NuxtLink class="button-primary" to="/contato"> Assine Já ! </NuxtLink> </li>
			</ul>
		</nav>
	</header>
</template>

<script>
export default {
	methods: {
		scrollTo() {
			document.getElementById('planos').scrollIntoView({behavior: "smooth"});
		}
	}
}
</script>

<style>

</style>