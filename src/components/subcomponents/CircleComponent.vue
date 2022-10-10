<template>
  <div id="component" class="flex">
    <div class="circle">
        <span class="number">{{ percentage }}<span class="percentage">%</span></span>
    </div>
    <div class="info column space-around">
        <h2>{{ title }}</h2>
        <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
    name: 'CircleComponent',
    props: {
        percentage: Number,
        title: String,
        text: String
    }
}
</script>

<style scoped lang="scss">
    @import '../../style/global_variables.scss';
    
    #component {
        width: 25vw;
        .circle {
        border: 10px solid #232328;
        border-radius: 50%;
        width: 100px;
        height: 100px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 3rem;
        .number{
            font-size: 2rem;
            color: $header-font-color;
            .percentage {
                font-size: 1rem;
            }
        }
    }
    .info {
        padding-left: 2.5rem;
        h2 {
            color: #fff;
        }
        p {
            color: $header-font-color;
            line-height: 1.5rem;
        }
    }
    }
</style>
        