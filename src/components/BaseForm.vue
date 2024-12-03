<template>
    <form :name="name" :action="action" :method="method">
        <div v-for="(field, index) in fields" :key="index">
            <BaseInput v-if="field.type == 'input'" v-bind="field" />
            <BaseCheckbox v-if="field.type == 'checkbox'" v-bind="field" />
        </div>
        <input type="submit" value="submit" />
    </form>
</template>

<script setup lang="ts">
import BaseInput from '@/components/BaseInput.vue'
import BaseCheckbox from '@/components/BaseCheckbox.vue'

import type { Form } from '@/App.vue'

defineProps<Form>();
</script>