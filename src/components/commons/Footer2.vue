<template>
    <div class="container-fluid">
        <div class="ms_container container">
            <div class="ms_row row">
                <div 
                v-for="(element, index) in dati"
                :key="index"
                class="col-3">
                    <img :src="element.src" alt="">
                    <h3>{{element.titolo}}</h3>
                    <ul>
                        <li class="my-3"
                        v-for="(element, index) in dati[index].lista"
                        :key="index">{{element}}</li>
                        
                    </ul>
                </div>
                <div class="col-3">
                    <img src="" alt="">
                    <h3>Flexible Learning</h3>
                    <img class="ms_footerimg" src="../../assets/img/footer-img-1.png" alt="">
                </div>
            </div>
        </div>
        <div class="my-3 container">
                <div class=" row">
                    <div class="col-6">
                        <p>
                        Copyrights 2017 @Mikado Themes
                        </p>
                    </div>
                    <div class="d-flex justify-content-end col-6">
                        <p class="mx-2">
                        CALL +44 300 303 0266 
                        </p>
                        <p class="mx-5">
                        FOLLOW US
                        </p>
                        <i class="ms_gray mx-2 fab fa-facebook"></i>
                        <i class="ms_gray mx-2 fab fa-instagram"></i>
                        <i class="ms_gray mx-2 fab fa-twitter"></i>
                        
                    </div>
                </div>
            </div>
    </div>
</template>

<script>
import dataFooter from "../../data/dataFooter";
export default {
    name:"Footer2",
    data(){
        return{
            dati: dataFooter,
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

    .container-fluid{
        height: 500px;
        background-color: $background-footer;

        .ms_container{
            border-bottom: 1px solid $color-borderbottom;
            height: 400px;

            img{
                width: 150px;
                padding-top: 30px;
            }
            h3{
                color: white;
                font-weight: 900;
            }
            .ms_row{
                padding-top: 70px;
                display: flex;
                justify-content: center;
            }
        }

        .ms_footerimg{
            padding-top: 30px;
            width: 200px!important;
        }
    }

    ul{
        padding: 0;
        li{
            color: $color-gray;
            list-style: none;
        };
    }

    .row{
        p{
            color: $color-borderbottom;
        }
    }
    .ms_gray{
        color: $color-gray;
        }

</style>