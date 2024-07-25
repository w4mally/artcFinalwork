<script setup lang="ts">

defineProps<{
    msg: string
}>()

</script>

<template>
    <div class="button">{{ msg }}</div>
</template>

<style scoped>
    .button {
        font-size: 2rem;
        position: relative;
        left : -500px;
        bottom: -100px;
        padding-left: 2px;
        padding-right: 2px;
        display: inline-block;
        border: 2px solid rgb(0, 0, 0);
        background: linear-gradient(to bottom, rgb(241, 163, 201), rgb(241,163,201)); 
        }
</style>