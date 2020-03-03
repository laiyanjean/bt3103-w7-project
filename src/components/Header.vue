<template>
  <div class="headerStyle">
    <nav>
      <h1>{{ msg }}</h1>
        <router-link to="/" exact>List</router-link>
        <router-link to="/add" exact>Add Rating</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  
  data(){
    return{
        msg: 'Singapore Attractions List'
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

nav{
    background: rgb(122, 63, 100);
    padding: 14px 0;
    margin-bottom: 40px;
}

.router-link-active{
    background: ivory;
    color: #444;
}

h1{
    color:ivory
}
</style>