
<template>
      <div id="app">
        <hr>
        <table>
            <tbody>
                <div class="col-3">
                    <div>
                    <tr class="letra-tab2">
                      <td><strong>No</strong></td>
                      <td><strong>PAIS</strong></td>
                    </tr>
                    <tr v-for="lista in listado" :key="lista.id" class="letra-tab">
                            <td>{{ lista.id }}</td>
                            <td>{{ lista.nombre }}</td>
                        </tr>
                    </div>
                </div>
            </tbody>
        </table>
        <hr>
    </div>
</template>
<script>
export default {

       props:{
        listado: Array,
        cont: Array,
        estilo: Object,
    },
}
</script>
