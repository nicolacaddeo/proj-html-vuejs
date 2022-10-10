<template>
  <div>
    <section id="business-area" class="flex align-center">
      <div class="container flex">
        <div class="card">
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

export default {
  name: "MainComponent",
  components: { GreenLabelComponent, GreenBtnComponent },
  data() {
    return {
      greenLabelData,
      greenBtnName
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
    .card {
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
    
