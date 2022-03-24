<template>
  <div>
    <section class="cardlist">
<div class="cardlist-dropdown">
        <label for="dropdown" class="cardlist-dropdown-container">
            <span class="cardlist-dropdown-container-span">По умолчанию<img src="../assets/img/arrow.svg" alt="arrow"
                    class="cardlist-dropdown-container-span-arrow"></span>
        </label>
        <input class="open" type="checkbox" id="dropdown">
        <div class="dropdown">  
    </div>
</div>
<div class="cardlist-container">
   <CardItem/>
   <CardItem/>
   <CardItem/>
   <CardItem/>
   <CardItem/>
   <CardItem/>
</div>
</section>
      
  </div>
</template>

<script>
import CardItem from './card.vue';
export default {
  name: 'CardList',
    components: {
    CardItem
  },
  props: {
    msg: String
  }
}
</script>
<style lang="scss" scoped>
.cardlist {
    .cardlist-dropdown {
        height: 36px;
        max-width: 122px;
        width: 100%;
        box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
        background: white;
        border-radius: 4px;
        display: flex;
        justify-content: center;
        margin-left: auto;
        align-items: center;
        margin-bottom: 16px;
        cursor: pointer;
        .cardlist-dropdown-container {
            color: #b4b4b4;
            font-size: 12px;
            margin-left: 16px;
            .cardlist-dropdown-container-span-arrow{
                margin-left:5px;
            }
        }
        #dropdown {
            visibility: hidden;
        }
    }
    .cardlist-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

    }
    }
</style>