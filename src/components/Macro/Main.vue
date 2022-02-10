<template>
    <div>
        <div @click="scrollToTop(), goToPricing()" class="sticky"><i class="fas fa-angle-up"></i><p>top</p></div>
        <MainSezione1/>
        <MainSezione2/>
        <MainSezione3/>
    </div>
    
</template>

<script>
import MainSezione1 from "../commons/MainSezione1.vue"
import MainSezione2 from "../commons/MainSezione2.vue"
import MainSezione3 from "../commons/MainSezione3.vue"
export default {
    name:"Main",
    components: {
    MainSezione1,
    MainSezione2,
    MainSezione3
    },
    methods: {
        scrollToTop() {
            window.scrollTo(0, 0);
        },  goToPricing() {
            this.$router.push('/pricing');
        }
        }
}
</script>

<style scoped lang="scss">
@import "../../assets/style/vars.scss";
.sticky {
        position: -webkit-sticky;
        position: sticky;
        text-align: center;
        top: 500px;
        left: 100%;
        background-color:$main-color;
        padding: 5px;
        width: 50px;
        color: $color-white;
    }

</style>