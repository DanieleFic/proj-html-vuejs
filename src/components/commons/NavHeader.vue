<template>
    <div class="header">
        <div class="ms_jumbo container-fluid">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-2">
                        <img class="ms_logo" src="../../assets/img/logo-light.png" alt="">
                    </div>
                    <div class="ms_nav col-8">
                        <div class="col" >
                        HOME
                        </div>
                        <div class="col">
                        COURSE
                        </div>
                        <div class="col">
                        INSTRUCTORS
                        </div>
                        <div class="col">
                        EVENTS
                        </div>
                        <div class="col">
                        PAGES
                        </div>
                        <div class="col">
                        ELEMENTS
                        </div>
                    </div>
                    <div class="col-2">
                        <div class="ms_icon">
                            <i class="icon fas fa-search"></i>
                            <i class="icon fas fa-shopping-basket"></i>
                            <i class="icon fas fa-bars"></i>
                        </div>
                    </div>
                </div>
            </div>
            <SlideTesto/>
        </div>
    </div>
</template>

<script>
import SlideTesto from "../commons/SlideTesto.vue"
export default {
    name:"NavHeader",
    components: {
    SlideTesto
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
@import url('https://fonts.googleapis.com/css2?family=Merriweather&family=PT+Serif&family=Roboto:wght@300&display=swap');
    .ms_jumbo{  
        height: 700px;
        background-image: url("../../assets/img/jumbo.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        text-align: center;
    }
    .row{
        height: 50px;
        display: flex;
        flex-direction: row;

        .col:hover{
            color:$main-color;
            cursor: pointer;
        }

        .ms_nav{
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            font-family: 'Roboto', sans-serif;
        }

        .ms_logo{
            display: flex;
            align-items: center;
            height: 30px;
            margin-top:10px
        }

        .ms_icon{
            padding-top: 15px;
            display: flex;
            flex-direction: row;
            color: white;
            .icon{
                margin-right: 13px;

                &:hover{
                color:$main-color;
                cursor: pointer;
                }
            }
        }
    }

</style>