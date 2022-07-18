<template>
    <div>
        <h1 class="letra-cont">{{ cont[num].nombre }}</h1>
    </div>
</template>
<script>
export default {
    props:{
        num: Number,
        cont: Array,
    },
 }
</script>