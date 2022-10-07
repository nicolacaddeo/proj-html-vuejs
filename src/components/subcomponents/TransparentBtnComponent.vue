<template>
  <div>
    <button>{{ buttonName }}</button>
  </div>
</template>

<script>
    

export default {
    name: 'TransparentBtnComponent',
    props: {
        buttonName: String
    }
}
</script>

<style scoped lang="scss">
    @import '../../style/global_variables.scss';
    button {
        text-transform: uppercase;
        background-color: transparent;
        border: 1px solid $main-green;
        color: $header-links-color;
        padding: 1rem 2rem;
        border-radius: 5px;
        font-size: 1rem;
        font-weight: 600;
        cursor: pointer;
    }

</style>