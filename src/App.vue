<template>
  <site-header></site-header>
  <side-panel></side-panel>
  <div class="container">
    <promo-tabs>
      <promo-tab name="Фитнесс">
        <img src="@/assets/img/tabs/fitness.svg" alt="fitness.svg" class="tab_img">
        <div class="tab__descr">
          Меню "Фитнес" - это новый подход к приготовлению блюд: больше свежих овощей и фруктов. Для
          людей, которые интересуются спортом; активных и здоровых. Это абсолютно новый продукт с
          оптимальной ценой и высоким качеством!
        </div>
      </promo-tab>  

      <promo-tab name="Премиум">
        <img src="@/assets/img/tabs/premium.jpg" alt="premium.jpg" class="tab_img">
        <div class="tab__descr">
          Меню “Премиум” - мы используем не только красивый дизайн упаковки, но и качественное исполнение
          блюд. Качественная и самое главное, вкусная еда вам обеспечена Красная рыба, морепродукты, фрукты - ресторанное меню без похода в ресторан!
        </div>
      </promo-tab>

      <promo-tab name="Постное">
        <img src="@/assets/img/tabs/post.jpg" alt="post.jpg" class="tab_img">
        <div class="tab__descr">
          Наше специальное “Постное меню” - это тщательный подбор ингредиентов: полное отсутствие
          продуктов животного происхождения. Полная гармония с собой и природой в каждом элементе! Все
          будет Ом!
        </div>
      </promo-tab>
  
      <promo-tab name="Сбалансированное"> 
        <img src="@/assets/img/tabs/fitness.svg" alt="fitness.svg" class="tab_img">
        <div class="tab__descr">
          Меню "Сбалансированное" - это соответствие вашего рациона всем научным рекомендациям. Мы
          тщательно просчитываем вашу потребность в к/б/ж/у и создаем лучшие блюда для вас. Качество вашего питания это наша забота!
        </div>
      </promo-tab>
    </promo-tabs>
    <div class="promo__lifetext">Живи полной жизнью!</div>
    <hr class="line">
    <site-offer></site-offer>
    <slider-wrapper
      :carousel_data="SliderItem"
      :sliderCurrent="SliderCurrent"
    >
    </slider-wrapper>
    <hr class="line">
    <form-to-call></form-to-call>
    <hr class="line">
  </div>
</template>
<script>
  import SiteHeader from "./components/Header/SiteHeader.vue";
  import PromoTab from "./components/Promo/PromoTab.vue";
  import PromoTabs from "./components/Promo/PromoTabs.vue";
  import SiteOffer from "./components/Offer/SiteOffer.vue";
  import SliderWrapper from "./components/Slider/SliderWrapper.vue";
  import SidePanel from "./components/SidePanel/SidePanel.vue";
  import FormToCall from "./components/Form/FormToCall.vue"

export default {
  components: {
    SiteHeader,
    PromoTab,
    PromoTabs,
    SiteOffer,
    SliderWrapper,
    SidePanel,
    FormToCall
  },
  
  data() {
    return {
      SliderItem: [
        {id: 1, img: '1.jpg'},
        {id: 2, img: '2.jpg'},
        {id: 3, img: '3.jpg'},
        {id: 4, img: '4.jpg'}
      ],

      SliderCurrent: [
        {id: 1, current: 0},
        {id: 2, current: 1},
        {id: 3, current: 2},
        {id: 4, current: 3},      
      ]
    }
  }
}
</script>
<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Roboto";
    font-style: normal;
  }

  .container {
    width: 1200px;
    margin: 0 auto;
  }

  .line {
    width: 250px;
    margin: 0 auto;
    margin-top: 80px;
  }
</style>
