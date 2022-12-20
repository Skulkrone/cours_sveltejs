<script>
	import Liste1 from "./Liste1.svelte";
	import Liste2 from "./Liste2.svelte";
	let titre = "Hello World";
	let titreA = "Hello World !!!";

	const myObj = {
		race: 'Persan',
		poids: 2,
		age: 4,
		couleur: 'gris'
	}
  // let prenom = "John";
  let compteur = 0;
  function incremente() {
    compteur++;
  }
  function decremente() {
    compteur--;
  }
	function reset(){
		compteur = 0;
	}
</script>

<!-- <h1>Mon titre {prenom}</h1>
<h2>{2+2} {prenom.toUpperCase()}</h2> -->

<h1>{compteur}</h1>
<button on:click={incremente}>+1</button>
<button on:click={decremente}>-1</button>
<button on:click={reset}>reset</button>
<Liste1 {titreA} {...myObj}/>
<Liste1 titreA={titre}/>
<Liste1 />
<Liste2 />

<style>
</style>
