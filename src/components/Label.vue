<template>
    <div id="label" :style="{backgroundColor: color}">
        {{ text }}
    </div>
</template>

<script setup lang="ts">
defineProps({
    text: { type: String, required: true },
    color: { type: String, required: true }
});
</script>

<style scoped>
#label {
    color: white;
    width: fit-content;
    padding: 0rem 0.25rem;
    border: solid 1px var(--color-text);
}
</style>