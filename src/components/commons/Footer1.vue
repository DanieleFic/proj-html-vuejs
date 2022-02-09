<template>
    <div class="container-fluid">
        <div class="container">
            <div class="row">
                <div class="col-3">
                    <img src="../../assets/img/logo-school-1.png" alt="">
                </div>
                <div class="col-3">
                    <img src="../../assets/img/logo-school-2.png" alt="">
                </div>
                <div class="col-3">
                    <img src="../../assets/img/logo-school-3.png" alt="">
                </div>
                <div class="col-3">
                    <img src="../../assets/img/logo-school-4.png" alt="">
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
    name:"Footer1"
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

    .container-fluid{
        border-top: 1px solid $color-borderbottom;
    }

    .row{
        
    }
    
    .col-3{
        height: 200px;
        display: flex;
        align-items: center;
    }
    
</style>