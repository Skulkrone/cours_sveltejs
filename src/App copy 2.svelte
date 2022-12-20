<script>
  let toggle = false;
  function toggleClasse() {
    toggle = !toggle;
  }

  let compteur = 0;
  function incremente() {
    compteur = compteur + 10;
  }

  let tabPays = ["Danemark", "Canada", "Mexique", "Argentine"];

	let tabPaysKeys = [

		{
			id: Math.random(),
			pays: 'Norvège'
		},
		{
			id: Math.random(),
			pays: 'USA'
		},
		{
			id: Math.random(),
			pays: 'Costa Rica'
		},
		{
			id: Math.random(),
			pays: 'Brésil'
		},

	]
</script>

<button on:click={toggleClasse}>Toggle le contenu !</button><br /><br />

<!-- <div class={toggle ? 'visible' : 'invisible'}> -->
<!-- Les conditions -->
{#if toggle}
  <div class="visible">
    <h2>Voici le contenu</h2>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Harum
      consequuntur mollitia voluptates perspiciatis eum rerum. Provident
      repellendus dolor tempora nostrum?
    </p>
  </div>
{/if}

<button class="btn btn-primary" on:click={incremente}>Incremente</button>
<h1>{compteur}</h1>

{#if compteur < 30}
  <p>Le compteur est inférieur à 30 !</p>
{:else if compteur >= 30 && compteur <= 50}
  <p>Le compteur est entre 30 & 50</p>
{:else}
  <p>Le compteur est au-dessus de 50 !</p>
{/if}

<ul>
  {#each tabPays as pays, index}
    <li>#{index + 1} : {pays}</li>
  {/each}
</ul>

<ul>
  {#each tabPaysKeys as obj, index (obj.id)}
    <li>#{index + 1} : {obj.pays}</li>
  {/each}
</ul>

<style>
  .visible {
    width: 250px;
    height: auto;
    padding: 10px;
    background: lightblue;
    text-align: center;
    margin-bottom: 20px;
  }
  /* .invisible {
		display: none;
	} */
</style>
