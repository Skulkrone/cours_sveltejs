<script>
	let objDataForm = {
		pays: ""
	}
	let pays = "";
	// function inpFunc(e){
	// 	// console.log(e.target.value);
	// 	pays = e.target.value;
	// 	// console.log(pays);
	// }

	function handleData(e){
		e.preventDefault();
		pays = objDataForm.pays;
		objDataForm.pays = "";
	}
</script>


<div class="container">

	<form on:submit={handleData}>

		<div class="mb-3">
			<label for="pays">Votre pays</label>
			<!-- <input 
			id="pays" 
			type="text" 
			class="form-control" 
			bind:value={pays}
			> -->
			<input 
			id="pays" 
			type="text" 
			class="form-control" 
			bind:value={objDataForm.pays}
			>
		</div>
		<button type="submit" class="btn btn-primary">Envoyer les données</button>
	</form>
	<br>
	<h1>Votre pays : {pays}</h1>

</div>


<ul>

</ul>

<ul>

</ul>

<style>

</style>
