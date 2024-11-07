<script setup>
import {ref} from 'vue';
const titulo='Asesora de ventas y caja';
const fecha='2022 - Actualidad';
const experiencias = ref([
    {id:1, src:'src/assets/favicon.ico', parrafo: 'Facturación y manejo de cuentas corrientes.'},
    {id:2, src:'src/assets/favicon.ico', parrafo: 'Gestión de ventas mayoristas y minoristas.'},
    {id:3, src:'src/assets/favicon.ico', parrafo: 'Arqueo, manejo y cierre de caja diario.'},
    {id:4, src:'src/assets/favicon.ico', parrafo: 'Etiquetado, reposición y control de stock.'}
    
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{titulo.toLocaleUpperCase()}}</h3>
        <p class="fecha">{{fecha}}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
                <img class="imagen-svg" :src="experiencia.src" width="20px" :alt="experiencia.parrafo">
                <p>{{experiencia.parrafo}}</p>
            </li>
            
        </ul>
    </div>
</template>

<style scoped>
.card{
    display: flex;
    flex-direction: column;
    padding:2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}
.titulo{
    font-size:1.5rem;
    color: rgb(42, 78, 145);
}
.fecha{
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}
.listado{
    display: flex;
    flex-direction: column;
}
.item{
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>
