<template>
    <ul class="developers">
        <li class="developers__item">
            <co-developer></co-developer>
        </li>
    </ul>
</template>
<script>
export default {
     name: 'CoDevelopers',
     data() {
         return {
             user: [], //nuestro componente va a tener un valor inicial users, que es un array que comienza vacío

         } 
     }
}
</script>
<style lang="scss" scoped>

</style>