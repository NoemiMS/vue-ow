<template>
    <input 
        name= 'search'
        type="text"
        placeholder='Write an user'
        class='Search'
        v-model='criteria' 
    >
    <!-- el input va a tener un modelo de datos asignado -->
</template>

<script>
export default {
    name: 'CoSearch',
    data() {
        return {
            criteria: ''
        }
    },
    watch: {
        criteria () {
            this.$emit('search', this.criteria)
        }
    }
}
</script>