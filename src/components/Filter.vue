<template>
  <div>
    <section class="filter">
<span class="filter-h1 semibold">Добавление товара</span>
<div class="filter-container">
    <div class="tablet">
    <span class="filter-container-title">Наименование товара</span>
    <input type="text" name="name" id="title" placeholder="Введите наименование товара">
    <span class="filter-container-description">Описание товара</span>
    <input type="text" name="name" id="description" placeholder="Введите описание товара">
</div>
<div class="tablet">
    <span class="filter-container-img">Ссылка на изображение товара</span>
    <input type="text" name="name" id="img" placeholder="Введите ссылку">
    <span class="filter-container-price">Цена товара</span>
    <input type="text" name="name" id="price" placeholder="Введите цену">
<button class="filter-container-button">Добавить товар</button>
</div>
</div>
</section>
  </div>
</template>

<script>
export default {
  name: 'FilterList',
  props: {
    msg: String
  }
}
</script>
<style lang="scss" scoped>
.filter {
    max-width: 332px;
    min-width: 250px;
    width: 100%;
    .filter-h1 {
        font-size: 28px;
        color: #3f3f3f;
    }
    .filter-container {
        margin-top: 16px;
        padding: 24px;
        background: white;
        display: flex;
        flex-direction: column;
        box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
        border-radius: 4px;
        .filter-container-title,
        .filter-container-description,
        .filter-container-img,
        .filter-container-price {
            font-size: 10px;
            margin-bottom: 4px;
            color: #49485e;
            position: relative;
        }
        .filter-container-description,
        .filter-container-img,
        .filter-container-price {
            margin-top: 16px;
        }
        .filter-container-title::after,
        .filter-container-img::after,
        .filter-container-price::after {
            content:"\25CF";
            font-size: 8px;
            color:#FF8484;
            margin-bottom:5px;
            position: absolute;
    top: -3px;
        }
        #title,
        #description,
        #price,
        #img {
            border: none;
            height: 36px;
            max-width: 284px;
            width: 100%;
            box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
            border-radius: 4px;
            font-size: 12px;
            padding-left:16px;
            box-sizing: border-box;
            &::placeholder {
                font-size: 12px;
                color: #b4b4b4;
                padding-top: 10px;
          
            }
        }
        #description {
            height: 108px;
            margin-bottom: auto;
            &::placeholder {
                transform: translateY(-35px);
            }
        }
        .filter-container-button {
            background: #eeeeee;
            border-radius: 10px;
            border: none;
            color: #b4b4b4;
            font-size: 12px;
            margin-top: 24px;
            height: 36px;
            max-width: 284px;
            width:100%;
        }
    }
}
   @media (max-width:991px){
        .filter{
            max-width:100%;
            margin-bottom:16px;
        }
        .filter-h1{
            margin-left:26px;
        }
        .filter-container{
            flex-direction: row !important;
        }
        .tablet{
            display: flex;
    flex-direction: column;
    width: 100%;
    padding-left:10px;
    padding-right:10px;
        }
    }
     @media (max-width:576px){
        .filter-container{
            flex-direction: column !important;
        }
        .tablet{
            padding-left:0;
            padding-right:0;
        }
        #title,
        #description,
        #price,
        #img {
            max-width:100% !important;
        }
        .filter-container-button {
           max-width: 100% !important;
        }

    }
    @media (max-width:337px) {
    .filter-h1{
        font-size:20px !important;
    }
}
</style>