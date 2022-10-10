<template>
  <div class="green-label flex">
   <span>{{ labelName }}</span>
  </div>
</template>

<script>
export default {
    name: 'GreenLabelComponent',
    props: {
        labelName: String
    }
}
</script>

<style scoped lang="scss">
    @import '../../style/global_variables.scss';

    .green-label {
        background-color: rgba(4, 131, 131, 0.2);
        color: #088181;
        text-align: center;
        text-transform: capitalize;
        width: calc(100% / 3);
        padding: .6rem .8rem;
        border-radius: 5px;
        display: inline-block;
    }
</style>