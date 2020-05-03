<template>
    <ul class="developers">
        <li class="developers__item">
            <co-developer></co-developer>
        </li>
    </ul>
</template>
<script>
import CoDeveloper from '@/components/CoDeveloper'

export default {
     name: 'CoDevelopers',
     components: {
         CoDeveloper,
     },
     data() {
         return {
             user: [], 
         } 
     },
     mounted () {
         console.log('CoDeveloper mounted')
     }
}
</script>
<style lang="css" scoped>

</style>