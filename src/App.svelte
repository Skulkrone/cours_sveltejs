<script>
	let objDataForm = {
		prenom: "",
		age: "",
		taille:"",
		poids: "",
		txtData: ""
	}
	let prenom = "";
	let age = "";
	let taille = "";
	let poids = "";
	let txtData = "";
	// function inpFunc(e){
	// 	// console.log(e.target.value);
	// 	prenom = e.target.value;
	// 	// console.log(prenom);
	// }



	function handleData(e){
		e.preventDefault();
		prenom = objDataForm.prenom;
		age = objDataForm.age;
		taille = objDataForm.taille;
		poids = objDataForm.poids;
		txtData = objDataForm.txtData;

		objDataForm.prenom = "";
		objDataForm.age = "";
		objDataForm.taille = "";
		objDataForm.poids= "";
		objDataForm.txtData = "";
	}
</script>


<div class="container">

	<form on:submit={handleData}>

		<div class="mb-3">
			<label for="prenom" class="form-label">Votre Prénom</label>
			<!-- <input 
			id="prenom" 
			type="text" 
			class="form-control" 
			bind:value={prenom}
			> -->
			<input 
			id="prenom" 
			type="text" 
			class="form-control" 
			bind:value={objDataForm.prenom}
			>

			<label for="inpNumb" class="form-label">Votre Age</label>
			<input 
			type="number" 
			id="inpNumb" 
			class="form-control"
			bind:value={objDataForm.age}
			>

			<label for="inpTaille" class="form-label">Votre Taille</label>
			<input 
			type="number" 
			id="inpTaille" 
			class="form-control"
			bind:value={objDataForm.taille}
			>

			<label for="rangeNumb" class="form-label">Votre poids</label>
			<input
			type="range" 
			id="rangeNumb" 
			class="form-range"
			bind:value={objDataForm.poids}
			min="30" max="100">
			<span>Sélection : {objDataForm.poids}</span>

			<br><br>

			<label for="txt" class="form-label">Votre message</label>
			<textarea 
			id="txt" 
			class="form-control"
			bind:value={objDataForm.txtData}
			></textarea>
		</div>
		<button type="submit" class="btn btn-primary">Envoyer les données</button>
	</form>
	<br>
	<h1>Votre prenom : {prenom}</h1>
	<h2>Votre âge : {age} </h2>
	<h2>Votre âge : {taille} </h2>
	<h2>Votre poids : {poids} </h2>
	<h3>Votre IMC : {#if poids} {(poids / Math.pow(taille / 100, 2)).toFixed(1)} {/if}</h3>
	<hr>

	<p>{txtData}</p>

</div>

<style>

</style>
