<template>
  <div>
    <button>
        {{buttonName}}
    </button>
  </div>
</template>

<script>
export default {
    name: 'GreenBtnComponent',
    props: {
        buttonName: String
    }
}
</script>

<style scoped lang="scss">
    @import '../style/global_variables.scss';

    button {
        text-transform: uppercase;
        background-color: $main-green;
        border: none;
        color: $header-links-color;
        padding: 1rem 2rem;
        border-radius: 5px;
        font-size: 1rem;
        cursor: pointer;
    }
</style>