<template>
    <div>
        <h2 class="invisible">Hover over the page to find the hidden clue.</h2>
        <p v-for="number in 249" :key="number">
            <span class="d-none">{{ lorem }}</span>
        </p>
        <p>
            <span class="answer display-1 font-weight-bold text-white">/helheim</span>
        </p>
        <p v-for="number in 158" :key="-number">
            <span class="d-none">{{ lorem }}</span>
        </p>
    </div>
</template>

<script>
    import lorem from '@/assets/lorem'
  export default {
    name: 'Midhgardhsormr',
    data () {
      return {
        lorem
      }
    },
    components: {},
    methods: {},
    computed: {},
    watch: {},
  }
</script>

<style scoped lang="scss">
    .answer {
        position: absolute;
        left: 12vw;
        top: 74vh;
        opacity: 0;
        transition: $transition-base;
        z-index: 10000000;
        &:hover {
            opacity: 1;
        }
    }
</style>
