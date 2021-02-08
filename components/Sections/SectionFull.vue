<template>
    <section :class="['flex flex-col md:flex-row w-full h-full', ...classes]">
        <slot></slot>
    </section> 
</template>

<script>
export default {
    props: ['classes'],
}
</script>

<style>
    section {
        min-width: 100vw; 
        min-height: 100vh; 
    }
</style>
