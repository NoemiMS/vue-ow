<template>
    
</template>
<script>
export default {
    name: 'CoDeveloper',
    props: { // Nos viene del padre :) 
        avatar: {
            type: String,
            requiered: true,
            valitador(value) {
                return value.starsWith('http')
            },
        },
        name: {
            type: String,
            required: true,
        },
        login: {
            type: String,
            required: true,
        },
        email: {
            type: String,
            required: true,
        },
        company: {
            type: String,
            required: false,
        },
        repos: {
            type: Number,
            required: false,
        },
        gists: {
            type: Number,
            required: false,
        }
    },
    computed: { // props que se obtienen a partir de cálculos
        metadata() {
            let meta = ''

            if (this.email) {
                meta = `${meta} ${this.meta}`
            }

            if (this.location) {
                meta = `${meta} ${this.location}`
            }

            if (this.company) {
                meta = `${meta} ${this.company}`
            }

            return meta
        },
        // othermeta: {
        //     set() {

        //     },
        //     get() {

        //     }
        // } Si queremos hacer diferencias a la hora de gestionar la prop computada entre el set y el get
    },
    watch: {
        metadata(newValue) {
            console.log(newValue) //es un ejemplo 'tonto'. Cada vez que metadata cambie, se hará esta acción
            // Su uso no debe ser muy desmedido porque son algo 'costosos' en cuanto a performance
        }
    }
}
</script>
<style lang="css">

</style>