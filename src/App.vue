<template>
  <div id="app" class="row centro">
    <ImageWorld :title="title"/>
    <div class="col-3">
      <TitleCont :cont="continentes" :num="0"/>
      <TablasPais :listado="europa" :clase="clase_uno"/>
    </div>
    <div class="col-3">
      <TitleCont :cont="continentes" :num="1"/>
      <TablasPais :listado="asia"/>
    </div>
    <div class="col-3">
      <TitleCont :cont="continentes" :num="2"/>
      <TablasPais :listado="latinoamerica"/>
    </div>
  </div>
</template>

<script>
import TablasPais from './components/TablasPais.vue'
import ImageWorld from './components/ImageWorld.vue'
import TitleCont from './components/TitleCont.vue'

export default {
  name: 'App',
  components: {
    TablasPais,
    ImageWorld,
    TitleCont,
  },

  data: () => ({
        
        europa: [{"id":1,"nombre":"ALEMANIA"},
        {"id":2,"nombre":"ITALIA"},
        {"id":3,"nombre":"FRANCIA"},
        {"id":4,"nombre":"UCRANIA"},
        {"id":5,"nombre":"SUIZA"}],

        asia: [{"id":1,"nombre":"JAPÓN"},
        {"id":2,"nombre":"CHINA"},
        {"id":3,"nombre":"INDONESIA"},
        {"id":4,"nombre":"INDIA"},
        {"id":5,"nombre":"TAILANDIA"}],

        latinoamerica: [{"id":1,"nombre":"ARGENTINA"},
        {"id":2,"nombre":"COLOMBIA"},
        {"id":3,"nombre":"BRASIL"},
        {"id":4,"nombre":"CHILE"},
        {"id":5,"nombre":"PERÚ"}],

        continentes: [{"nombre":"EUROPA"},
                {"nombre":"ASIA"},
                {"nombre":"LATINOAMERICA"},],

        title: "WORLD",
        
    })
}
</script>
<style>
    .centro{
      justify-content: center;
      background-color: black;
    }

    .image{
      width: 1200px;
    }

    .letra-tab { 
        color: rgb(64, 222, 233);
    }
    .letra-tab2 { 
        color: rgb(0, 243, 223);
    }
    .letra-titulo { 
        color: rgb(255, 255, 255);
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        margin-top: 20px;
        text-align: center;
        font-size:10ch;
        color: rgb(4, 193, 240);
    }
    .letra-cont { 
        color: rgb(223, 247, 11);
        font-size: 2em;
        font-style: oblique;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }

    /*Estilo general de tabla*/
    table {
        font-family: arial, sans-serif;
        border-collapse: collapse;
        width: 100%;
      }
      
      td, th {
        text-align: left;
        padding: 8px;
      }
</style>