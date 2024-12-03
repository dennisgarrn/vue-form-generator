<template>
    <span>
        <label v-if="label" :for="id">{{ label }} </label>
        <input type="text" :value="value" :id="id" :placeholder="placeholder">
    </span>
</template>

<script setup lang="ts">
import type { Field } from '@/App.vue'

defineProps<Field>();
</script>
