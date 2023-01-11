<!-- La réactivité avec Svelte -->
<script>
  let val1 = 100;
  let val2 = 300;
  let val3 = 50;

  // Variable non réactive :
  let totalNonReactif = val1 + val2 + val3;

  // Variable réactive : $:
  $: total = val1 + val2 + val3;

  $: console.log("Vous avez modifié vos dépenses", val3, val2, val1);

  $: if(total > 1000) {
    console.log("Attention, dépenses supérieures à 1000!");
  }

	let array = [1,2,3,4];

  function depenseSup() {
    // val3 = 800;
		// array.push(5);
		array = [...array, 5];
		console.log(array);
  }
</script>

<h1> {array} </h1>

<h1>Réactif : {total}</h1>
<h1>Non-Réactif : {totalNonReactif}</h1>
<h3>{val3}</h3>

<button on:click={depenseSup}>Changer une dépense</button>

<style>
</style>
