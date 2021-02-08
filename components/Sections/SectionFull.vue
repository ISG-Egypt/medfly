<template>
    <section :class="['flex w-full h-full', ...classes]">
        <slot></slot>
    </section> 
</template>

<script>
export default {
    props: ['classes'],
}
</script>

<style scoped>
    section {
        min-width: 100vw; 
        min-height: 100vh; 
    }
</style>
