<template>
	<div class="d-flex justify-content-center p-md-5 p-3">
		<form action="" class="col-12 col-md-10 col-lg-9 d-flex justify-content-center">
			<div class="d-flex row form-container justify-content-between col-xl-9 col-lg-10 col-md-11 col-12">
				<input class="input full-input" type="text" placeholder="Nome completo" name="nome">
				<input class="input full-input" type="text" placeholder="E-mail" email="email">
				<input class="input full-input" type="text" placeholder="Celular" name="celular">
				<input class="input full-input" type="text" placeholder="CPF" name="cpf">

				<div class="half-content d-flex justify-content-between">
					<input class="input half-input" type="text" placeholder="Nascimento" name="nascimento">
					<input class="input half-input" type="text" placeholder="CEP" name="cep">
				</div>
				
				<select name="planos" class="input full-input">
					<option value="plano" selected>Plano</option>
				</select>

				<div class="submit d-flex justify-content-center col-12">
					<input type="submit" class="button-primary col-12 col-md-6 col-lg-7 col-xl-6" placeholder="ENVIAR">
				</div>
			</div>


		</form>
	</div>
</template>

<script>
export default {

}
</script>

<style>

</style>