<template>
  <div class="card">
        <div id="centered-container">
            <img :src="`card_assets/${imgUrl}`">
            <h2>{{ title }}</h2>
            <p>{{ text }}</p>
        </div>
  </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: {
        imgUrl: String,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    $titles-color: #21333e;
    $paragraph-color: #606d75;
    .card {
        width: 40%;
        border-radius: 15px;
        background-color: #fff;
        padding: 3rem;
        #centered-container {
            width: 90%;
            margin: 0 auto;
        }
        img {
            width: 100%;
        }
        h2 {
            color: $titles-color;
            text-transform: capitalize;
            padding: 1.8rem 0 2rem 0;
        }
        p {
            color: $paragraph-color;
        }
    }
</style>
        

        
        