<template>
    <div>
        <MainSezione1/>
        <MainSezione2/> 
    </div>
    
</template>

<script>
import MainSezione1 from "../commons/MainSezione1.vue"
import MainSezione2 from "../commons/MainSezione2.vue"
export default {
    name:"Main",
    components: {
    MainSezione1,
    MainSezione2
    }
}
</script>

<style>

</style>