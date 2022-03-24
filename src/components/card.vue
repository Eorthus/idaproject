<template>
   <div class="cardlist-container-card">
        <div class="cardlist-container-card-img">
            <img src="../assets/img/cart.jpg" alt="card">
        </div>
        <div class="cardlist-container-card-info">
            <span class="cardlist-container-card-info-h">Наименование товара</span>
            <span class="cardlist-container-card-info-p">Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк</span>
            <span class="cardlist-container-card-info-price">10 000 руб.</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CardItem',
  props: {
    msg: String
  }
}
</script>
<style lang="scss" scoped>
        .cardlist-container-card {
            width: 32%;
  
            background: white;
            display: flex;
            flex-direction: column;
           min-height: 423px;
           height:100%;
            box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.02), 0px 6px 10px rgba(0, 0, 0, 0.02);
            border-radius: 4px;
            margin-left: 1%;
    margin-bottom: 1%;
    cursor: pointer;
    position: relative;
    .cardlist-container-card-mark{
        position: absolute;
        width:32px;
        height:32px;
        top: -10px;
    right: -10px;
    display: none;
    }
&:hover .cardlist-container-card-mark{
    display: block;
}
            .cardlist-container-card-img {
                width: 100%;
                height: 100%;
                flex: 1;
                img {
                    width: 100%;
                    object-fit: cover;
                }
            }
            .cardlist-container-card-info{
                padding: 16px;
    height: 100%;
    display: flex;
    flex-direction: column;
    flex: 1;
    .cardlist-container-card-info-h{
        margin-bottom: 16px;
        font-size: 20px;
    }
    .cardlist-container-card-info-p{
        font-size: 16px;
        margin-bottom: 32px;
        flex: 1;
    
    }
    .cardlist-container-card-info-price{
        margin-bottom: 8px;
    font-size: 24px;
    }
            }
        }
        @media (max-width:576px){
                    .cardlist-container-card{
            width:100% !important;
            margin-bottom: 16px !important;;
            margin-left:0;
        }
        }
</style>