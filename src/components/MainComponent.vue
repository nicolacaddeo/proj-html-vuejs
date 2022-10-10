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
    <section></section>
    <section></section>
    <section></section>
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

export default {
  name: "MainComponent",
  components: { GreenLabelComponent, GreenBtnComponent, CardComponent },
  data() {
    return {
      greenLabelData,
      greenBtnName,
      cardsData
    }
  }
}
</script>

<style scoped lang="scss">
  @import '../style/global_variables.scss';
  
  /** 
  ** First section 
  */
  $titles-color: #21333e;
  $paragraph-color: #606d75;
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
</style>
      
      
    
