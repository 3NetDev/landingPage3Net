<template>
	<div>
		<Header/>
		<Banner/>
		<Planos/>
		<img id="bannerPromocao" src="../static/media/banner_prime.png"/>
		<AutoAtendimento/>
		<Footer/>

		<div id="supportIcon" class="p-2 d-flex align-items-center justify-content-center">
			<a href="https://api.whatsapp.com/send?phone=12974075710" target="_blank">
				<i class="fa-brands fa-whatsapp"></i>
			</a>
		</div>
	</div>
</template>

<script>
import Header from '~/components/Header.vue';
import Banner from '~/components/Banner.vue';
import AutoAtendimento from '~/components/AutoAtendimento.vue';
import Footer from '~/components/Footer.vue';
export default {
    name: "IndexPage",
    components: { Header, Banner, AutoAtendimento, Footer }
}
</script>
