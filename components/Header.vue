<template>
	<header class="d-flex justify-content-between">
		<img src="@/static/media/logo.png" alt="Logo">
		<nav class="nav-desktop align-items-center p-0 m-0">
			<ul class="d-flex col-12 justify-content-between p-0 m-0">
				<li> <a href="/">Início</a> </li>
				<li v-on:click="scrollTo"> Planos </li>
				<li> <a href="http://186.236.66.96:8000/accounts/central/login" target="_blank"> Central do cliente </a> </li>
				<li> <NuxtLink class="button-primary" to="/contato"> Assine Já ! </NuxtLink> </li>
			</ul>
		</nav>
		
		<nav class="nav-menu-mobile">
			<div class="d-flex col-12 justify-content-end">
				<i v-on:click="toggleMenu" class="fa-solid fa-xmark"></i>
			</div>
			<hr>
			<ul class="d-flex col-12 flex-column p-0 m-0">
				<li class="d-flex justify-content-center"> <a href="/">Início</a> </li>
				<li class="d-flex justify-content-center" v-on:click="scrollTo"> Planos </li>
				<li class="d-flex justify-content-center"> <a href="http://186.236.66.96:8000/accounts/central/login" target="_blank"> Central do cliente </a> </li>
				<li class="d-flex justify-content-center"> <NuxtLink class="button-primary col-12" to="/contato"> Assine Já ! </NuxtLink> </li>
			</ul>
		</nav>
		<div id="mobile-menu" >
			<i v-on:click="toggleMenu" class="fa-solid fa-bars"></i>
		</div>
	</header>
</template>

<script>
export default {
	data() {
		return {
			showMenu: false
		}
	},
	methods: {
		scrollTo() {
			document.getElementById('planos').scrollIntoView({behavior: "smooth"});
		},
		toggleMenu() {
			this.showMenu 
			? document.querySelector('.nav-menu-mobile').style.display = 'none'
			: document.querySelector('.nav-menu-mobile').style.display = 'block'

			this.showMenu = !this.showMenu;

		}
	}
}
</script>

<style>

</style>