<template>
  <div id="app" class="app">
    
      <FilterList/>
      <CardList/>
  </div>
</template>

<script>
import FilterList from './components/Filter.vue';
import CardList from './components/Cardlist.vue';

export default {
  name: 'App',
  components: {
    FilterList,
    CardList,
  }
}
</script>
<style>
*{
  margin:0;
  padding:0;
}
</style>
<style lang="scss" scoped>
.semibold{
    font-family: "OpenSans_bold";
    font-weight: 600;
}
.regular {
    font-family: "OpenSans_regular";
    font-weight: 400;
}
@font-face {
    font-family: "OpenSans_Regular";
    src: url("./assets/fonts/SourceSansPro-Regular.ttf") format("truetype");
    font-weight: normal;
    font-style: normal;
}
@font-face {
    font-family: "OpenSans_bold";
    src: url("./assets/fonts/SourceSansPro-SemiBold.ttf") format("truetype");
    font-weight: normal;
    font-style: normal;
}
.app {
    font-family: "OpenSans_regular";
    font-weight: 400;
    display: flex;
    padding: 32px;
    background: #e5e5e5;
}
   @media (max-width:991px){
        .app{
            flex-direction: column;
        }
    }
 

</style>
