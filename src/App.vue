<script setup>
import { ref, watch } from 'vue';

const tituloTarjeta = ref('');
const chipSRC = ref('');
const numeroTarjeta = ref('');
const fechaExpiracion = ref('');
const propietario = ref('');
const tipoTarjetaSRC = ref('');
const chipImg = ref('');
const visaImg = ref('');

watch(chipSRC, (newValue) => {
  chipImg.value = newValue;
});
watch(tipoTarjetaSRC, (newValue) => {
  visaImg.value = newValue
})


</script>

<template>
  <div id="app">
    <form>
      <div>
        <label for="">Título de la tarjeta: </label>
        <input v-model="tituloTarjeta" placeholder="Visa Classic Credito" />
      </div>

      <div>
        <label for="">Chip SRC: </label>
        <input v-model="chipSRC" placeholder="/chip.png" />
      </div>

      <div>
        <label for="">Número:</label>
        <input v-model.number="numeroTarjeta" />
      </div>

      <div>
        <label for="">Fecha de expiración:</label>
        <input v-model="fechaExpiracion" />
      </div>

      <div>
        <label for="">Propietario: </label>
        <input v-model="propietario" />
      </div>

      <div>
        <label for="">Tipo de tarjeta SRC:</label>
        <input v-model="tipoTarjetaSRC" placeholder="/visa.png" />
      </div>

    </form>

    <div class="carnet">
      <h3>{{ tituloTarjeta }}</h3>
      <img width="40" :src="chipImg" alt="chip" />
      <div>
        <h2>{{ numeroTarjeta }}</h2>
        <span>Fecha Exp: <b>{{ fechaExpiracion }}</b></span>
      </div>
      <footer>
        <span>{{ propietario }}</span>
        <img :src="visaImg" width="60" />
      </footer>
    </div>
  </div>
</template>

<style scoped></style>
