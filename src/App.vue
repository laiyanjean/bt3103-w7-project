<template>
  <div id="app">
    <app-header></app-header>
    <router-view :attractions="attractions"></router-view>
    <!-- <PageContent :attractions="attractions"></PageContent> -->
    <app-footer></app-footer>
  </div>
</template>

<script>
//Registering components Locally
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
//import PageContent from './components/PageContent.vue'

export default {
  name: 'App',
  components: {
    //Registering with a name
    'app-header':Header,
    'app-footer':Footer,
    //Registering without a name
    //PageContent
  },

  data() {
    return {
      attractions: [{name:'Esplanade',image: 'https://images.squarespace-cdn.com/content/v1/59ef81176957da411cb2b71e/1554453972183-7P5CD48RJIOA9FY22MV5/ke17ZwdGBToddI8pDm48kPqQfq0L3n3wpHIsRapTfg8UqsxRUqqbr1mOJYKfIPR7LoDQ9mXPOjoJoqy81S2I8N_N4V1vUb5AoIIIbLZhVYxCRW4BPu10St3TBAUQYVKczo5Zn4xktlpMsMj-QlHXeMfNK6GwvtVkYEWiR8XAPyD3GfLCe_DXOSC_YcAacWL_/Esplanade.jpg',show:true},
                  {name:'Gardens by the Bay',image:'https://res.klook.com/image/upload/c_fill,w_750,h_500,f_auto/w_80,x_15,y_15,g_south_west,l_klook_water/activities/mcegxphankqeujwbhpjp.webp',show:true},
                  {name:'Sentosa',image:'https://res.klook.com/image/upload/c_fill,w_750,h_500,f_auto/w_80,x_15,y_15,g_south_west,l_klook_water/activities/yo1aqaam6wlfbvauscvk.webp',show:true},
                  {name:'Merlion',image:'https://media.thefinder.com.sg/2018/08/singapore-merlion-park-popular-attraction-marina-bay-750x500.jpg',show:true},
                  {name:'Singapore Zoo',image:'https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Singapore_Zoo_entrance-15Feb2010.jpg/300px-Singapore_Zoo_entrance-15Feb2010.jpg',show:true},
                  {name:'Orchard Road',image:'https://lh3.googleusercontent.com/proxy/pFot1pqUylRkM_kYAl-AHz7kUfSUmf-xBxLvNB2_ZGDbXXOgl8bqodhU6_-w0HAnf7XdqlkoIjkHsFVoh8oBogR-0ekNaOdovOwEMpOBV_Nt52YfSCYLOsF-8LW3_WvX6dyGn7n_ch7iT7mjRazUP285i9zwjDVuFtR91kwedngp=w592-h404-n-k-no',show:true}]
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
