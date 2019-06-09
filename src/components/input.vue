<template>
    <span>
        <label v-if="data.label" :for="data.id">{{ data.label }} </label>
        <input type="text" :value="data.value" :id="data.id">
    </span>
</template>

<script>
export default {
    name: 'baseInput',
    props: {
        data: {
            type: Object,
        }
    }
}
</script>
