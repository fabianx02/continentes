<template>
     <div class="row centro" style="estilo">
        <div class="col-10">
        <h1 class="letra-titulo">{{title}}</h1>
        <img src="../assets/wallpaperbetter.jpg" class="image">
        </div>
    </div>
</template>
<script>
export default {
    props:{
        title: String,
        estilo: Object,
    },
 }
</script>