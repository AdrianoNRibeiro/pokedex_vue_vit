<script setup>
    const pokemon = defineProps(["name", "xp", "height", "img"]);
</script>


<template>
  <div class="card card-pokemonSelected">
    <img :src="pokemon.img" height="300" class="card-img-top pt-2" :alt="pokemon.name">
    <div class="card-body">
        <h5 class="card-title text-center">{{ pokemon.name }}</h5>
        <hr>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        <div class="row">
            <section class="col">
                <strong>XP:</strong>
                <span>{{ pokemon.xp }}</span>
            </section>
            <section class="col">
                <strong>Altura:</strong>
                <span>{{ pokemon.height }}</span>
            </section>
        </div>
    </div>
  </div>
</template>

<style scoped> 
 .card-pokemonSelected {
    height: 500px;
    background: rgb(72,63,251);
    background: radial-gradient(circle, rgba(72,63,251,0.6) 0%, rgba(72,252,244, 0.2) 100%);
 }
</style>