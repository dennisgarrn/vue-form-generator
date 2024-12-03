<template>
    <span>
        <input type="checkbox" :value="value" :id="id">
        <label v-if="label" :for="id"> {{ label }}</label>
    </span>
</template>

<script setup lang="ts">
import type { Field } from '@/App.vue'

defineProps<Field>();
</script>
