<template>
	<div class="d-flex justify-content-center p-5">
		<form action="" class="col-8 d-flex justify-content-center">
			<div class="d-flex row form-container justify-content-between col-10">
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
					<input type="submit" class="button-primary col-6" placeholder="ENVIAR">
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