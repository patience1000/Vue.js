<script>
export default {
    props: ['modelValue'],
    emits: ['update:modelValue'],
    computed: {
        value: {
            get(value){
                return this.modelValue
            },
            set(){
                this.$emit('update:modelValue', value)
            }
        }
    }
}

</script>

<template>
    <input v-model="value"/>
</template>