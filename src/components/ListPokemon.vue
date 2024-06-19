<script setup>
const pokemon = defineProps(["name","urlBaseSvg"]);
</script>

<template>
    <div class="col-6 col-xs-4 col-sm-4 col-md-6 col-lg-4 col-xl-4">
        <div class="card mb-3 p-2 carListPokemon">
          <p class="text-center">{{ pokemon.name }}</p>
          <img :src="urlBaseSvg" class="card-img-top" alt="pokemon" height="85"/>
        </div>
    </div>
</template>

<style scoped>
    .carListPokemon {
        background: rgb(72,63,251);
        background: radial-gradient(circle, rgba(72,63,251,0.6) 0%, rgba(72,252,244, 0.2) 100%);
        cursor: pointer;
    }

    .carListPokemon:hover {
        background: rgb(72,63,251);
        background: radial-gradient(circle, rgba(72,63,251,0.6) 0%, rgba(72,252,244, 0.4) 100%);
    }

    .carListPokemon img:hover {
        padding: .1rem;
    }
</style>