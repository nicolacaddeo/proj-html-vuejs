<template>
  <div class="img-card">
    <img :src="`img_cards_data/${imgUrl}`">
    <div class="text-container">
        <h2>{{ text }}</h2>
    </div>
  </div>
</template>
    
<script>
export default {
    name: 'ImageCardComponent',
    props: {
        imgUrl: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    .img-card {
        width: calc(100% / 3);
        position: relative;
        img {
            width: 100%;
            border-radius: 10px;
            position: absolute;
            z-index: -1;
            filter: brightness(60%);
        }
        .text-container {
            height: 40vh;
            line-height: 2rem;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            text-align: center;
            h2 {
                color: #fff;
            }
        }
    }
</style>
        
        
        
        
