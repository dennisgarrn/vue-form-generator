<template>
    <form :name="form.name" :action="form.action" :method="form.method">
        <div v-for="(field, index) in form.fields" :key="index">
            <baseInput v-if="field.type == 'input'" :data="field" />
            <baseCheckbox v-if="field.type == 'checkbox'" :data="field" />
        </div>
        <input type="submit" value="submit" />
    </form>
</template>

<script>
import baseInput from '@/components/input.vue'
import baseCheckbox from '@/components/checkbox.vue'

export default {
    name: 'baseForm',
    props: {
        form: {
            type: Object,
        }
    },
    components: {
        baseInput,
        baseCheckbox,
    }
}
</script>