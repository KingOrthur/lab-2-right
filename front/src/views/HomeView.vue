<template>
  <main>
    <div class="container">
      <button type="button" class="btn btn-warning w-100 mt-4 mb-4">Охота на тренды: скидки до 60% с 6 по 12 марта ></button>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-xs-3 col-sm-3 col-md-3 col-lg-3">
          <ul class="list-unstyled mb-1">
            <li class="li-categ"><router-link to="catalog" class="nav-link"><h6>Категории ></h6></router-link></li>
            <li><a href=""><h6>Продукты</h6></a></li>
            <li><a href=""><h6>Бытовая техника</h6></a></li>
            <li><a href=""><h6>Компьютеры и офис</h6></a></li>
            <li><a href=""><h6>Строительство и ремни</h6></a></li>
            <li><a href=""><h6>Дом и сад</h6></a></li>
            <li><a href=""><h6>Спорт и развлечения</h6></a></li>
            <li><a href=""><h6>Канцтовары для офиса и дома</h6></a></li>
            <li><a href=""><h6>Игрушки и хобби</h6></a></li>
            <li><a href=""><h6>Безопасность и защита</h6></a></li>
            <li><a href=""><h6>Автомобили и мотоциклы</h6></a></li>
            <li><a href=""><h6>Освещение</h6></a></li>
            <li><a href=""><h6>Электроника</h6></a></li>
            <li><a href=""><h6>Красота и здоровье</h6></a></li>
            <li><a href=""><h6>Обувь</h6></a></li>
            <li><a href=""><h6>Электронные компоненты и принадлежности</h6></a></li>
            <li><a href=""><h6>Мобильные телефоны и аксессуары</h6></a></li>
            <li><a href=""><h6>Инструменты</h6></a></li>
            <li><a href=""><h6>Мать и ребенок</h6></a></li>
            <li><a href=""><h6>Мебель</h6></a></li>
            <li><a href=""><h6>Украшения и аксессуары</h6></a></li>
            <li><a href=""><h6>Наручные часы</h6></a></li>
            <li><a href=""><h6>Багаж и сумки</h6></a></li>
            <li><a href=""><h6>Мужская одежда</h6></a></li>
            <li><a href=""><h6>Женская одежда</h6></a></li>
            <li><a href=""><h6>Свадьбы и торжества</h6></a></li>
            <li><a href=""><h6>Тематическая одежда и униформа</h6></a></li>
            <li><a href=""><h6>Шиньоны и парики</h6></a></li>
            <li><a href=""><h6>Детсвкая одежда и обувь</h6></a></li>
            <li><a href=""><h6>Аксессуары для одежды</h6></a></li>
            <li><a href=""><h6>Цифровые товары</h6></a></li>
          </ul>
        </div>
        <div class="col-xs-9 col-sm-9 col-md-9 col-lg-9">
          <button type="button" class="col-xs-12 col-sm-12 col-md-12 col-lg-12 btn btn-danger high-btn w-100 mb-5">Товары из рекламы</button>
          <div class="products row">
            <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3 mb-3" v-for="item in items">
              <ProductItem :product="item"></ProductItem>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
// @ is an alias to /src


import ProductItem from "@/components/Product/ProductItem.vue";

export default {
  name: 'HomeView',
  components: {
    ProductItem
  },
  data() {
    return {
      items: [
        {id: 1, name: 'Часы 1', rating: '2.5', bought_times: 301, price: '432,65', inCart: false},
        {id: 2, name: 'Часы 2', rating: '4.6', bought_times: 302, price: '4320,65', inCart: false},
        {id: 3, name: 'Часы 3', rating: '3.2', bought_times: 403, price: '43,65', inCart: false},
        {id: 4, name: 'Часы 4', rating: '4.4', bought_times: 354, price: '6632,65', inCart: false},
        {id: 5, name: 'Часы 5', rating: '1.0', bought_times: 305, price: '5000', inCart: false},
        {id: 6, name: 'Часы 6', rating: '2.0', bought_times: 306, price: '6000,65', inCart: false},
        {id: 7, name: 'Часы 7', rating: '3.0', bought_times: 407, price: '7003,65', inCart: false},
        {id: 8, name: 'Часы 8', rating: '4.0', bought_times: 358, price: '8032,65', inCart: false},
      ]
    }
  }
}
</script>
