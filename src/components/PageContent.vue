<template>
  <div>
    <ul>
        <li v-for="item in attractions" v-bind:key="item.name">

            <h2>{{item.name}}</h2>
            <img v-bind:src="item.image" v-show="item.show"/>
            <counter></counter>
            
        </li>
    </ul>
  </div>
</template>


<script>
import CounterBtn from './CounterBtn.vue'

export default {
  props: {
      attractions: {
          type: Array,
          required: true,
      }
  },

  components: {
    //Registering with a name
    'counter':CounterBtn,
  },

  data(){
    return{
        /*
        itemsList: [{name:'Esplanade',image: 'https://images.squarespace-cdn.com/content/v1/59ef81176957da411cb2b71e/1554453972183-7P5CD48RJIOA9FY22MV5/ke17ZwdGBToddI8pDm48kPqQfq0L3n3wpHIsRapTfg8UqsxRUqqbr1mOJYKfIPR7LoDQ9mXPOjoJoqy81S2I8N_N4V1vUb5AoIIIbLZhVYxCRW4BPu10St3TBAUQYVKczo5Zn4xktlpMsMj-QlHXeMfNK6GwvtVkYEWiR8XAPyD3GfLCe_DXOSC_YcAacWL_/Esplanade.jpg',show:true},
                    {name:'Gardens by the Bay',image:'https://res.klook.com/image/upload/c_fill,w_750,h_500,f_auto/w_80,x_15,y_15,g_south_west,l_klook_water/activities/mcegxphankqeujwbhpjp.webp',show:true},
                    {name:'Sentosa',image:'https://res.klook.com/image/upload/c_fill,w_750,h_500,f_auto/w_80,x_15,y_15,g_south_west,l_klook_water/activities/yo1aqaam6wlfbvauscvk.webp',show:true},
                    {name:'Merlion',image:'https://media.thefinder.com.sg/2018/08/singapore-merlion-park-popular-attraction-marina-bay-750x500.jpg',show:true},
                    {name:'Singapore Zoo',image:'https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Singapore_Zoo_entrance-15Feb2010.jpg/300px-Singapore_Zoo_entrance-15Feb2010.jpg',show:true},
                    {name:'Orchard Road',image:'https://lh3.googleusercontent.com/proxy/pFot1pqUylRkM_kYAl-AHz7kUfSUmf-xBxLvNB2_ZGDbXXOgl8bqodhU6_-w0HAnf7XdqlkoIjkHsFVoh8oBogR-0ekNaOdovOwEMpOBV_Nt52YfSCYLOsF-8LW3_WvX6dyGn7n_ch7iT7mjRazUP285i9zwjDVuFtR91kwedngp=w592-h404-n-k-no',show:true}] */
        }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    background:rgb(122, 63, 100);
    padding:10px;
    border-style: solid;
    border-color:black;
    border-width: 2px;
}
h1{
    color:ivory
}
h2{
  text-align: center
}
#itemsList{
    width: 100%;
    max-width: 1200px;
    margin: 30px auto;
    padding: 0 5px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 10px;
    border: 1px solid #222;
    margin: 10px;
}

img {
    width: 100%;
}

</style>