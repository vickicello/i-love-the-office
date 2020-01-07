<template>
<div :class="['card', 'img-', 'rounded-0']">
    <img
        :src="imgSrc"
        class="card-img rounded-0"
        :alt="imgAlt"
    />
    <div class="card-body">
      <slot />
    </div>
</div>
</template>

<script>
    export default {
      name: 'Card',
      props: ['imgDirection', 'imgSrc', 'imgAlt']
    }
</script>

<style lang="scss">

</style>
