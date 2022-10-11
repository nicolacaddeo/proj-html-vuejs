<template>
  <div>
    <section id="business-area" class="flex align-center">
      <div class="container flex">
        <div class="business-card">
          <h4>Our business areas</h4>
          <h2>Logistics Services</h2>
          <p>
            We are leaders in providing logistics services with a set of cutting edge technologies and a team of experienced and renowned professionals.
          </p>
          <div id="label-container">
            <GreenLabelComponent v-for="label in greenLabelData" :key="label.id" 
            :labelName = label.name />
          </div>
          <GreenBtnComponent :buttonName = greenBtnName.readMore />
        </div>
        <div class="cards-container">
          <CardComponent v-for="card in cardsData" :key="card.id" 
          :imgUrl = card.imgUrl
          :title = card.title
          :text = card.text  />
        </div>
      </div>
    </section>
    <section id="company-area">
      <div id="dark-area">
        <h4>About the network</h4>
        <h1><span class="bg-green">The</span> Company</h1>
        <p>With all of this expertise and capability comes an unrivalled commitment to customer service.</p>
        <div id="circle-container">
          <CircleComponent v-for="circle in circleData" :key="circle.id" 
          :percentage = circle.percentage 
          :title = circle.title 
          :text = circle.text />
        </div>
      </div>
      <div id="img-area"></div>
    </section>
    <section id="web-area">
      <div class="img-container">
        <img src="../assets/img/logo-5.png" alt="">
        <img src="../assets/img/logo-1.png" alt="">
        <img src="../assets/img/logo-2.png" alt="">
        <img src="../assets/img/logo-3.png" alt="">
        <img src="../assets/img/logo-4.png" alt="">
        <img src="../assets/img/logo-5.png" alt="">
      </div>
    </section>
    <section id="editorial-area">
      <div class="container">
        <h4>Our editorial content</h4>
        <h2>Latest <span class="bg-green">News</span></h2>
        <div class="p-btn-container">
          <p>Every week we publish content about what is best in the business world.</p>
          <GreenBtnComponent :buttonName = greenBtnName.seeAll />
        </div>
        <div class="cards-container">
          <ImageCardComponent v-for="imgCard in imgCardsData" :key="imgCard.id" 
          :imgUrl = imgCard.imgUrl 
          :text = imgCard.text />
        </div>
      </div>
    </section>
    <section></section>
    <section></section>
  </div>
</template>

<script>
import GreenLabelComponent from './subcomponents/GreenLabelComponent.vue';
import {greenLabelData} from '../data/green_label_data.js';
import GreenBtnComponent from './subcomponents/GreenBtnComponent.vue';
import {greenBtnName} from '../data/greenBtnData.js';
import CardComponent from './subcomponents/CardComponent.vue';
import {cardsData} from '../data/cards_data.js'
import CircleComponent from './subcomponents/CircleComponent.vue';
import {circleData} from '../data/circle_percentage-data';
import ImageCardComponent from './subcomponents/ImageCardComponent.vue';
import {imgCardsData} from '../data/img_cards_data.js'

export default {
  name: "MainComponent",
  components: { GreenLabelComponent, GreenBtnComponent, CardComponent, CircleComponent, ImageCardComponent },
  data() {
    return {
      greenLabelData,
      greenBtnName,
      cardsData,
      circleData,
      imgCardsData
    }
  }
}
</script>

<style scoped lang="scss">
  @import '../style/global_variables.scss';
  $titles-color: #21333e;
  $paragraph-color: #606d75;
  
  /** 
  ** First section 
  */
  #business-area{
    background-color: $section-bg;
    height: 70vh;
    .cards-container {
      display: flex;
      flex-grow: 1;
      column-gap: 2rem;
      padding: 2rem;
    }
    .business-card {
      width: 25%;
      padding: 1rem;
      h4 {
        color: #00a6a6;
        text-transform: uppercase;
      }
      h2 {
        color: $titles-color;
        font-size: 3.5rem;
        line-height: 4rem;
        padding: 2rem 0;
      }
      p {
        color: $paragraph-color;
        line-height: 1.5rem;
        width: 85%;
      }
      #label-container {
        margin: 1rem 0;
        display: flex;
        column-gap: .5vw;
      }
    }
  }
  /** 
  ** First section END
  */
  /** 
  ** Second section 
  */
  #company-area {
    height: 100vh;
    display: flex;
    #dark-area {
      width: 50%;
      height: 100vh;
      background-color: $light-black;
      padding: 5rem 0 0 20rem;
      h4 {
        color: #00a6a6;
        text-transform: uppercase;
        font-size: .9rem;
      }
      h1 {
        color: #fff;
        font-size: 3rem;
        padding: 3rem 0 3.5rem 0;
        .bg-green {
          background-color: rgba(4, 131, 131, 0.2);
          padding: 0 1rem;
          border-radius: 5px;
        }
      }
      p {
        color: $header-font-color;
        font-size: 1.1rem;
      }
      #circle-container {
        margin-top: 5rem;
        display: flex;
        flex-direction: column;
        row-gap: 4rem;
      }
    }
    #img-area {
      width: 50%;
      height: 100vh;
      background-image: url('../assets/img/about-5.jpg');
    }
  }
  /** 
  ** Second section END
  */
  /** 
  ** Third section 
  */
  #web-area {
    background-color: $section-bg;
    height: 25vh;
    .img-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 25vh;
      column-gap: 5rem;
    }}
  /** 
  ** Third section END
  */
  /** 
  ** Fourth section 
  */
    #editorial-area {
      height: 50vh;
      padding-top: 8rem;
      h4 {
        color: #00a6a6;
        font-size: .9rem;
        text-transform: uppercase;
      }
      h2 {
        color: $titles-color;
        font-size: 3rem;
        padding: 2rem 0;
        .bg-green {
          color: #058283;
          background-color: rgba(4, 131, 131, 0.2);
          border-radius: 5px;
          padding: 0 .5rem;
        }
      }
      .p-btn-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        p {
          color: $paragraph-color;
        }
      }
      .cards-container {
        padding-top: 2.5rem;
        padding-bottom: 10rem;
        display: flex;
        column-gap: 2rem;
      }
    }
  /** 
  ** Fourth section END
  */
</style>
      
    
      
      
    
