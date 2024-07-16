<template>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
        
        <TituloConvenio />
    
        <center><ConvenioBusqueda /></center>
    
    <div class="conteiner_conv">

        <div class="conteiner_conv_one">
            <div class="row">
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="apagado" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
            </div>
            <div class="row">
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
            </div>
            <div class="row">
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="apagado" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
            </div>
            <div class="row">
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="prendido" />
                </div>
                <div class="col-lg-4">
                    <ConvenioCard convenioTitle="Mi Convenio" convenioContent="Detalle del convenio" state="apagado" />
                </div>
            </div>
        </div>

        <ConexionQSL />
        <StadisticsConvenio/>
       
    </div>
    
</template>

<script setup>
import ConvenioCard from "./main/ConvenioCard.vue"
//import StadisticsConvenio from "./stadistics/StadisticsConteiner.vue"
import ConvenioBusqueda from "./main/ConvenioBusqueda.vue"
import TituloConvenio from "./main/TituloConvenio.vue"
//import ConexionQSL from "./main/ConexionQSL.vue";
</script>

<style scoped>
.conteiner_conv {
    padding: 10px;
    background-color: #17202A;
    background-color: white;
    
    color: aliceblue;
    border-radius: 5px;
    border: 1px solid black;
    margin-left: 50px;
    margin-right: 50px;
    margin-top: 5px;
    margin-bottom: 5px;
}
</style>