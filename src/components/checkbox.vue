<template>
    <span>
        <input type="checkbox" :value="data.value" :id="data.id">
        <label v-if="data.label" :for="data.id"> {{ data.label }}</label>
    </span>
</template>

<script>
export default {
    name: 'baseCheckbox',
    props: {
        data: {
            type: Object,
        }
    }
}
</script>
