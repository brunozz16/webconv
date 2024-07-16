<template>
    <div class="cont-busqueda">
        <input class="input-busqueda" type="text" id="nombre" name="nombre" placeholder="Buscador">
        <button class="button-busqueda">Buscar</button>
    </div>
</template>

<script setup>

</script>

<style scoped>
.cont-busqueda{
    width: 50%;
    background-color: #1c2632;
    color:white;
    border-radius: 5px;
    padding: 15px;
    margin: 10px 10px 10px 10px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.input-busqueda{
    margin-right: 10px;
    width: 50%;
    font: inter 90% cursive;
    padding: 2px;
}
.button-busqueda{
    all: unset;
    background-color: green;
    color: white;
    border-radius: 5px;
    padding: 5px 15px 5px 15px;
    font: inter 90% cursive;
    box-shadow: none;
    background-image: linear-gradient(to right, green, rgb(28, 216, 28));
}
.button-busqueda:hover{
    background-color: black;
    color: green;
    background-image: linear-gradient(to right, rgb(134, 134, 134), rgb(255, 255, 255));
}
</style>