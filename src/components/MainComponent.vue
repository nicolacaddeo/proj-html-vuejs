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
        </div>
        <div class="card"></div>
        <div class="card"></div>
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
export default {
    name: 'MainComponent'
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
      width: calc(100% / 3);
      border: 1px dashed blue;
      height: 50vh;
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
    }
  }
  /** 
  ** First section END
  */
</style>
    
