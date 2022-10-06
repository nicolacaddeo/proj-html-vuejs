<template>
  <div>
    <h1>
        <span id="nex">Nex</span>
        <span>gen</span>
    </h1>
  </div>
</template>

<script>
export default {
    name: 'NexGenComponent'
}
</script>

<style scoped lang="scss">
    @import '../style/global_variables.scss';

    h1 {
        color: $header-font-color;
        font-size: 1.3rem;
        text-transform: uppercase;
        letter-spacing: .25rem;
        #nex {
            color: #00a6a6;
            background-color: rgba(4, 131, 131, 0.3);
            padding: .7rem 0 .7rem 1.5rem;
            border-top-left-radius: 20px;
            border-bottom-left-radius: 20px;
            margin-right: .3rem;
        }
    }
</style>