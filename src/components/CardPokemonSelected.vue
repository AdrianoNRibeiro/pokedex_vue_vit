<script setup>
    const pokemon = defineProps(["name", "xp", "height", "img", "loading"]);
</script>


<template>
  <div class="card card-pokemonSelected" :class="loading? '': 'animate__animated animate__flipInY'">
    <img v-if="pokemon.name" :src="pokemon.img" height="300" class="card-img-top pt-2" :alt="pokemon.name">
    <img v-else src="../assets/egg_pokemon.svg" height="300" class="card-img-top pt-2" alt="Egg Pokemon">
    <div class="card-body">
        <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
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
    height: 75vh;
    background: rgb(72,63,251);
    background: radial-gradient(circle, rgba(72,63,251,0.8) 0%, rgba(72,252,244, 0.8) 100%);
 }
</style>