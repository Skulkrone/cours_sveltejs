<script>
  export let titreA = "Valeur par défaut";
  export let age;
  export let poids;
  export let couleur;
  export let race;
</script>

<h2>{titreA}</h2>
<ul>
  <li>{race}</li>
  <li>{age} ans</li>
  <li>{poids}KG</li>
  <li>{couleur}</li>
  <li>Lorem</li>
</ul>

<style>
  h2 {
    color: rgb(42, 121, 211);
  }
</style>