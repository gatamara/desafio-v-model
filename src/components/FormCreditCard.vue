<template>
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
</template>

<script>
export default {
    setup() {

    }
}

</script>