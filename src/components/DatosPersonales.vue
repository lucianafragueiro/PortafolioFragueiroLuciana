<script setup>
const title = "Luciana Fragueiro";
const descripcion = "Estudiante de Tecnicatura Universitaria en Programación - UTN";
const residencia = "Rosario, Santa Fe, Argentina";
const presentacion = "Me presento como una persona ordenada, empatica y positiva. Ademas, cuento con capacidad para el trabajo en equipo, la comunicación, el aprendizaje continuo y la gestión de los tiempos. Actualmente me encuentro en búsqueda de un nuevo desafío laboral relacionado a mi formación académica donde pueda aplicar mis conocimientos y poder crecer tanto a nivel personal, como profesional. Ofrezco amplia capacidad de aprendizaje, compromiso y disponibilidad horaria.";
const redesSociales = [
    { id: 1, name: "Linkedin", src: '/src/assets/linkedin_icon.svg', url:'https://www.linkedin.com/in/luciana-fragueiro-9492361a8/?originalSubdomain=ar'},
    { id: 2, name: "GitHub", src:'/src/assets/github_icon.svg', url:'https://github.com/lucianafragueiro'},
    { id: 3, name: "Instagram",src: 'src/assets/instagram_icon.svg', url:'https://www.instagram.com/lulafragueiro/'}
];
const telefono = '+54 3413440620';
</script>

<template>
<section class="datos personales"> 
    <div class="card">
        <h1>{{title}}</h1>
        <h2>{{descripcion}}</h2>
        <p>{{presentacion}}</p>
        <ul class="container-lista">
            <li v-for="red in redesSociales" :key="red.id">
                <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
            </li>
        </ul>
        <h3>Mi telefono personal: {{telefono}}</h3>
        <h4> {{residencia}}</h4>

    </div>
</section>
    

</template>

<style scoped>
h1 {
    font-size: 2.5rem;
}
p {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
}
.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    text-align: center; 
}
.container-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}
.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}
.icon-redsocial:hover {
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}
h3 {
    font-size: 1.2rem;
    font-weight: 600;
}
</style>


